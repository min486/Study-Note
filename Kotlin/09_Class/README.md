<div align="center">
  <p>
    <img src="../README.assets/kotlin-hero.png">
  </p>
  <br>
  <h2>Kotlin</h2>
  <p>코틀린 관련 내용 정리</p>
  <br>
  <br>
</div>








## 🔥 클래스 (Class)

### OOP

> Object Oriented Programming (객체 지향 프로그래밍)

<br>

### 객체

> 이름이 있는 모든 것, 생성된 실체

<br>

### 절차 / 객체 지향 프로그래밍 문제 해결 방법

- 절차지향 프로그래밍

코드를 위에서부터 아래로 실행하면 문제가 해결된다

- 객체지향 프로그래밍

객체를 만들어서, 객체에게 일을 시켜서 문제를 해결한다

ex) 선수, 심판, 경기장, 관중 -> 축구 게임

<br>

### 객체를 만드는 방법

> 클래스(설명서)를 통해서 인스턴스화 시키고 그 결과로 객체(인스턴스)를 얻게 된다

```kotlin
fun main(array: Array<String>) {
    
    // 클래스(설명서)를 통해서 실체를 만드는 방법
    // -> 인스턴스화 -> 인스턴스(객체)
    Car("v8 engine", "big")

    val bigCar = Car("v8 engine", "big")

    // 우리가 만든 클래스(설명서)는 자료형이 된다
    val bigCar1: Car = Car("v8 engine", "big")
    val superCar: SuperCar = SuperCar("good engine", "big", "white")
}

// 클래스(설명서) 만드는 방법(1)
class Car constructor(var engine: String, var body: String) {  // constructor 생략 가능

}

// 클래스(설명서) 만드는 방법(2)
class SuperCar {
    var engine: String
    var body: String
    var door: String

    constructor(engine: String, body: String, door: String) {
        this.engine = engine
        this.body = body
        this.door = door
    }
}

// 클래스(설명서) 만드는 방법 (3) 
// -> 1번 방법의 확장
class Car1 constructor(engine: String, body: String) {  // constructor 생략 가능
    var door: String = ""

    // 생성자
    constructor(engine: String, body: String, door: String) : this(engine, body) {
        this.door = door
    }
}

// 클래스(설명서) 만드는 방법 (4) 
// -> 2번 방법의 확장
class Car2 {
    var engine: String = ""
    var body: String = ""
    var door: String = ""

    constructor(engine: String, body: String) {
        this.engine = engine
        this.body = body
    }

    constructor(engine: String, body: String, door: String) {
        this.engine = engine
        this.body = body
        this.door = door
    }
}
```

<br>

### 객체(인스턴스) 기능 사용

```kotlin
fun main(array: Array<String>) {

    // 인스턴스가 가지고 있는 기능을 사용하는 방법
    val runableCar: RunableCar = RunableCar("simple engine", "short body")
    runableCar.ride()
    runableCar.drive()
    runableCar.navi("부산")

    // 인스턴스의 멤버변수에 접근하는 방법
    val runableCar2: RunableCar2 = RunableCar2("nice engine", "long body")
    println(runableCar2.engine)
    println(runableCar2.body)

    val testClass = TestClass()
    testClass.test(1)
    testClass.test(1, 2)
}

class RunableCar(engine: String, body: String) {

    fun ride() {
        println("탑승 하였습니다")
    }

    fun drive() {
        println("달립니다 !")
    }

    fun navi(destination: String) {
        println("$destination 으로 목적지가 설정되었습니다")
    }
}

// 위에 class와 동일한 class
class RunableCar2 {
    var engine: String
    var body: String

    constructor(engine: String, body: String) {
        this.engine = engine
        this.body = body
    }
	
    // 인스턴스화 될 때 가장 먼저 호출됨 (초기셋팅을 할 때 유용하다)
    init {
        println("RunableCar2가 만들어 졌습니다")
    }

    fun ride() {
        println("탑승 하였습니다")
    }

    fun drive() {
        println("달립니다 !")
    }

    fun navi(destination: String) {
        println("$destination 으로 목적지가 설정되었습니다")
    }
}

// 오버로딩
// -> 이름이 같지만 받는 매개변수가 다른 함수
class TestClass() {

    fun test(a: Int) {
        println("up")
    }

    fun test(a: Int, b: Int) {
        println("down")
    }
}
```


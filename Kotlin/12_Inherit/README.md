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








## 🔥 상속 (Inherit)

### 상속이란?

> 부모가 가지고 있는 기능을 물려받아서 사용할 수 있다

<br>

### 상속이 만들어낸 특징

- 자식 클래스는 부모 클래스의 타입이다
- 부모 클래스는 자식 클래의 타입이 아니다

```kotlin
fun main(args: Array<String>) {
    val superCar100: SuperCar100 = SuperCar100()
    
    // 상속 받아서 부모 기능 사용
    superCar100.drive()
	superCar100.stop()

	val bus100: Bus100 = Bus100()
	bus100.drive()  // error
    
    // override
    println(superCar100.drive())  // 빨리 달린다
}

// 부모 : Car100
// 자식 : SuperCar100, Bus100

// class, fun 접근제어자의 기본이 private이기 때문에
// 외부에서 사용하려면 open 키워드 사용
open class Car100() {
    open fun drive(): String {
        return "달린다"
    }

    fun stop() {

    }
}

// 상속 받은 경우
class SuperCar100() : Car100() {
    
    // override를 통해 부모의 기능을 수정해서 사용 가능
    override fun drive(): String {
        val run = super.drive()  // super는 부모(Car100)
        return "빨리 $run"
    }
}

// 상속 X
class Bus100() {

}

// 리펙토링
// -> 어떤 기능을 두번까지 사용하는건 괜찮지만 그 이상 넘어가면 리펙토링 하기
```

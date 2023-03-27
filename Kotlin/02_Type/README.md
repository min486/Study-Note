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









## 🔥 자료형 (Type)

- 정수형

  Long > Int > Short > Byte

- 실수형

  Double > Float

- 문자

  Char

- 문자열

  String

- 논리형 (참True / 거짓False)

  Boolean

<br>

### 변수 선언하는 방법 (1)

> var/val 변수명 = 값

```kotlin
var number = 10
```

<br>

### 변수 선언하는 방법 (2)

> var/val 변수 : 자료형 = 값

```kotlin
var number1: Int = 20
var hello1: String = "Hello"
var point1: Double = 3.4
```

### Variable & Type 예제

```kotlin
var a = 1 + 2 + 3 + 4 + 5  // 연산의 결과값을 변수에 넣어 줄 수 있다
var b = "1"
var c = b.toInt()  // 형변환
var d = b.toFloat()
var e = "John"
var f = "My name is $e Nice to meet you"  // $는 변수 나타냄

// Null
// - 존재 하지 않는다
// var abc : Int = null (error)
var abc1: Int? = null  // ?를 붙여주면 null을 가질 수 있는 자료형이 된다
var abc2: Double? = null

var g = a + 3

fun main(array: Array<String>) {
    println(a)
    println(b)
    println(c)
    println(d)
    println(f)
    println(abc1)

    println(g)
}
```


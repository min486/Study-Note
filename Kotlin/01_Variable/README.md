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









## 🔥 변수 (Variable)

### Variable

> 내 마음대로 원하는 것을 넣을 수 있는 상자

### Value

> 한번 넣으면 바꿀 수 없는 상자

<br>

### 변수 선언하는 방법

var/val 변수명(상자) = 값(넣고 싶은 것)

<br>

### Variable/Value 예제

```kotlin
var num = 10
var hello = "hello"
var point = 3.4

val fix = 20

fun main(args:Array<String>){
    
    println(num)
    println(hello)
    println(point)
    println(fix)

    num = 100
    hello = "Good Bye"
    point = 10.4
//  fix = 500

    println(num)
    println(hello)
    println(point)
    println(fix)
}
```

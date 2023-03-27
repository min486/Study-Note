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









## 🔥 제어 흐름 (Control flow)

### if, else

```kotlin
fun main(args: Array<String>) {
    val a: Int = 5
    val b: Int = 10

    // if/else 사용 하는 방법 (1)
    if (a > b) {
        println("a가 b 보다 크다")
    } else {
        println("a가 b 보다 작다")
    }
    
    // if/else 사용 하는 방법 (2)
    if (a > b) {
        println("a가 b 보다 크다")
    }
    
    // if/else/else if 사용 하는 방법 (3)
    if (a > b) {
        println("a가 b 보다 크다")
    } else if (a < b) {
        println("a가 b 보다 작다")
    } else if (a == b) {
        println("a와 b는 같다")
    } else {  // 생략가능

    }
}
```

<br>

### 값을 리턴하는 if 사용방법 (1)

```kotlin
val max = if (a > b) {
    a  // 5
} else {
    b  // 10
}
```

<br>

### 값을 리턴하는 if 사용방법 (2)

```kotlin
val max1 = if (a > b) a else b
```

<br>

### When

```kotlin
fun main(args: Array<String>) {

    val value: Int = 1

    when (value) {
        1 -> println("value is 1")
        2 -> println("value is 2")
        3 -> println("value is 3")
        else -> println("I do not know value")
    }
	
    // 위에 when과 아래 if문 같음
    if (value == 1) {
        println("value is 1")
    } else if (value == 2) {
        println("value is 2")
    } else if (value == 3) {
        println("value is 3")
    } else {
        println("I do not know value")
    }

    val value2 = when (value) {
        1 -> 10
        2 -> 20
        3 -> 30
        else -> 100
    }
    println(value2)
}
```


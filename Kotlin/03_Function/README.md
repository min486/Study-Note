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









## 🔥 함수 (Function)

### 함수란

> 어떤 input 을 넣어주면 어떤 output 나오는 것 
>
> ex) y = x + 2

<br>

### 함수 선언하는 방법

```kotlin
fun 함수명 (변수명: 타입, 변수명: 타입 ....) : 반환형 {
    함수 내용
    return 반환값
}
```

```kotlin
fun plus(first: Int, second: Int): Int {
    val result: Int = first + second
    return result
}
```

<br>

### 디폴트 값을 갖는 함수 만들기

```kotlin
fun plusFive(first: Int, second: Int = 5): Int {
    val result: Int = first + second
    return result
}
```

<br>

### 반환값이 없는 함수 만들기 (1)

```kotlin
fun printPlus(first: Int, second: Int): Unit {
    val result: Int = first + second
    println(result)
}
```

<br>

### 반환값이 없는 함수 만들기 (2)

```kotlin
fun printPlus2(first: Int, second: Int) {  // Unit 생략가능
    val result: Int = first + second
    println(result)
}
```

<br>

### 간단하게 함수를 선언하는 방법

```kotlin
fun plusShort(first: Int, second: Int) = first + second
```

<br>

### 가변인자를 갖는 함수 선언하는 방법

```kotlin
fun plusMany(vararg numbers: Int) {
    for (number in numbers) {
        println(number)
    }
}
```

<br>

### 예제

```kotlin
fun main(array: Array<String>) {
    
    // 함수를 호출 하는 방법
    val result = plus(5, 10)
    println(result)
    
    // 인수를 명시적으로 전달하는 방법
    val result2 = plus(first = 20, second = 30)
    println(result2)
    val result3 = plus(second = 100, first = 10)
    println(result3)

    // 디폴트 값을 갖는 함수
    val result4 = plusFive(10, 20)
    println(result4)
    val result5 = plusFive(10)
    println(result5)

    // 반환값이 없는 함수
    printPlus(10, 20)

    // 간단한 함수
    val result6 = plusShort(50, 50)
    println(result6)

    // 가변인자 갖는 함수
    plusMany(1, 2, 3)
    plusMany(100)
}
```

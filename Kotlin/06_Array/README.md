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









## 🔥 배열 (Array)

### 배열이 필요한 이유

> 그룹(모음집)이 필요할 때

<br>

### 배열을 생성하는 방법

```kotlin
fun main(array: Array<String>) {

    // 배열을 생성하는 방법(1)
    var number: Int = 10
    var group1 = arrayOf<Int>(1, 2, 3, 4, 5)
    println(group1 is Array)

    // 배열을 생성하는 방법(2)
    var number1 = 10
    var group2 = arrayOf(1, 2, 3.5, "Hello")
    
    // Array를 만드는 방법(3)
    val a1 = intArrayOf(1, 2, 3)
    val a2 = charArrayOf('b', 'c')  // char -> '', string -> ""
    val a3 = doubleArrayOf(1.2, 100.345)
    val a4 = booleanArrayOf(true, false, true)

    // Array를 만드는 방법(4) -> lambda를 활용한 방법
    var a5 = Array(10, { 0 })
    var a6 = Array(5, { 1;2;3;4;5 })

    // Index 란
    // -> 순서(번째)
    // [1, 2, 3, 4, 5]
    // "0"부터 시작
    // index 0 -> 1, index 1 ->2
}
```

<br>

### get, set

```kotlin
fun main(array: Array<String>) {
    
    // 배열의 값을 꺼내는 방법(1)
    val test1 = group1.get(0)
    val test2 = group1.get(4)
    println(test1)
    println(test2)

    // 배열의 값을 꺼내는 방법(2)
    val test3 = group1[0]
    println(test3)

    // 배열의 값을 바꾸는 방법(1)
    group1.set(0, 100)
    println(group1[0])

    // 배열의 값을 바꾸는 방법(2)
    group1[0] = 200
    println(group1[0])

    val array = arrayOf<Int>(1, 2, 3)

    // get, set
    val number = array.get(0)
    println(number)
	// val number1 = array.get(100)  // 해당 인덱스는 array 범주 밖이므로 error

    array.set(0, 100)
    val number2 = array.get(0)
    println(number2)

    array.set(100, 100)  // error

    // Array의 Bounds
    // - 처음 만들때 결정 된다
}
```

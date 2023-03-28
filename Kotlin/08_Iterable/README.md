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








## 🔥 반복문 (Iterable)

### for 구문

```kotlin
fun main(array: Array<String>) {

    val a = mutableListOf<Int>(1, 2, 3, 4, 5, 6, 7, 8, 9)

    // 반복하는 방법 (1)
    for (item in a) {
        if (item == 5) {
            println("item is Five")
        } else {
            println("item is not Five")
        }
    }

    // 반복하는 방법 (2)
    for ((index, item) in a.withIndex()) {
        println("index : " + index + " value : " + item)
        // 문자열 + Int(정수) = 문자열
        // 문자열 + 아무거나  = 문자열
    }

    // 반복하는 방법 (3)
    a.forEach {
        println(it)
    }

    // 반복하는 방법 (4)
    // 기본 it을 바꾸고 싶을 때
    a.forEach { item ->  
        println(item)
    }

    // 반복하는 방법 (5)
    // (2)번과 동일함
    a.forEachIndexed { index, item ->
        println("index : " + index + " value : " + item)
    }

    // 반복하는 방법 (6)
  	// until은 마지막을 포함하지 않는다
    // a.size는 9 -> 0부터 8까지 이다
    for (i in 0 until a.size) {  
        println(a.get(i))
    }
    
    // 반복하는 방법 (7)
    // 0부터 8까지 (숫자)칸씩 띄어서 반복
    for (i in 0 until a.size step (2)) {
        println(a.get(i))  // 1 3 5 7 9
    }
    
    // 반복하는 방법 (8)
    // 8부터 0까지 반복
    for (i in a.size - 1 downTo (0)) {
        println(a.get(i))  // 9 8 7 6 5 4 3 2 1
    }

    // 반복하는 방법 (9)
    for (i in a.size - 1 downTo (0) step (2)) {
        println(a.get(i))  // 9 7 5 3 1
    }

    // 반복하는 방법 (10)
    // .. -> 마지막을 포함한다
    for (i in 0 .. a.size) {      
        println(i)  // 0 1 2 3 4 5 6 7 8 9
    }
```

<br>

###  while

```kotlin
    // 반복하는 방법 (11)
    var b: Int = 0  // -> 1 -> 2 -> 3 -> 4
    var c: Int = 4

    while (b < c) {
        b++  // while문을 정지 시키기 위한 코드
        println("b")
    }
	
	// 반복하는 방법 (12)
    var d: Int = 0
    var e: Int = 4

    do {
        println("hello")
        d++
    } while (d < e)

}
```


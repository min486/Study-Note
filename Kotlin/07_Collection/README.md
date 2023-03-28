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








## 🔥 Collection

### list, set, map

> collection중에 가장 많이 사용되는 3가지 

<br>

### Immutable Collections (변경 불가능)

```kotlin
fun main(args: Array<String>) {
    
    // List 
    // 	-> 중복을 허용한다
    //  -> 순서가 있다
    val numberList = listOf<Int>(1, 2, 3, 3)
    println(numberList)  // [1, 2, 3, 3]
    println(numberList.get(0))  // 1
    println(numberList[0])  // 1

    // Set
    //  -> 중복을 허용하지 않는다
    //  -> 순서가 없다
    val numberSet = setOf<Int>(1, 2, 3, 3, 3)
    numberSet.forEach {
        println(it)
    }

    // Map 
    // 	-> Key, value 방식으로 관리한다
    val numberMap = mapOf<String, Int>("one" to 1, "two" to 2)
    println()
    println(numberMap.get("one"))
```

<br>

### Mutable Collections (변경 가능)

```kotlin
    val mNumberList = mutableListOf<Int>(1, 2, 3)
    mNumberList.add(3, 4)
    println(mNumberList)  // [1, 2, 3, 4]


    val mNumberSet = mutableSetOf<Int>(1, 2, 3, 4, 4, 4)
    mNumberSet.add(10)
    println(mNumberSet)  // [1, 2, 3, 4, 10]


    val mNumberMap = mutableMapOf<String, Int>("one" to 1)
    mNumberMap.put("two", 2)
    println(mNumberMap)  // {one=1, two=2}
}
```


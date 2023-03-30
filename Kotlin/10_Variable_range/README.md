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








## 🔥 Variable_range

### 변수의 접근 범위

> 변수를 선언하는 위치에 따라서 변수에 접근할 수 있는 범위가 달라진다

- 전역 변수

  : 어디에서나 접근할 수 있는 변수

- 지역 변수

  : 해당 지역에서만 접근할 수 있는 변수

```kotlin
// 전역 변수
var number100: Int = 10

fun main(args: Array<String>) {
    println(number100)  // 10
	
    // Test 클래스의 맴버변수 name에 접근할 수 없다 (지역 변수)
    // 아래처럼 실체화 시킨 후, 객체에는 접근 가능하다
    val test = Test("홍길동")
    test.testFun()
    test.name
    println(number100)  // 100
}

class Test(var name: String) {

    fun testFun() {
        var birth: String = "2000/3/1"
        name = "홍길동"
        number100 = 100
        // gender (접근 불가능)
        fun testFun2() {
            var gender: String = "male"
        }
    }

    fun testFun2() {
        name
		// birth (접근 불가능)
    }
}
```

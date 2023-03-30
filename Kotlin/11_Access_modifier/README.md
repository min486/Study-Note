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








## 🔥 접근 제어자 (Access_modifier)

### private

> 키워드를 붙이면 외부에서 변경할 수 없다

```kotlin
fun main(array: Array<String>) {

    val testAccess: TestAccess = TestAccess("아무개")

	testAccess.test()
	println(testAccess.name)
    
    // 마음대로 변경할 수 있는 문제
    // 지역/전역 변수로는 해결할 수 없다
	testAccess.name = "아무개 투"
	println(testAccess.name)

    val reward: Reward = Reward()
    reward.rewardAmount = 2000

    
    val runningCar: RunningCar = RunningCar()
    runningCar.runFast()
	// runningCar.run()
}

class Reward() {
    var rewardAmount: Int = 1000
}

class TestAccess {
    private var name: String = "홍길동"  // class 외부에서 접근 불가

    constructor(name: String) {
        this.name = name
    }

    fun changeName(newName: String) {
        this.name = newName
    }

    private fun test() {  // // class 외부에서 접근 불가
        println("테스트")
    }
}


class RunningCar() {

    fun runFast() {
        run()
    }
	
    // 기능을 외부에 공개하고 싶지 않을 때 사용
    // 내부 기능을 보조하고 싶을 때 사용
    private fun run() {

    } 
}
```

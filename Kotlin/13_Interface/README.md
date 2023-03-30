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








## 🔥 인터페이스 (Interface)

### 인터페이스 특징

- 인터페이스는 약속

  이것을 구현하면 이 타입이 된다

- 생성자가 없다 

  인스턴스화 시킬 수 없다 -> 설명서가 아니다

- 지침서다

  이것을 구현하고 싶다면 반드시 포함된 기능을 구현해야 한다

<br>

### 상속과 다른점

- 상속은 조상을 찾아가는 느낌
- 인터페이스는 종의 특징

<br>

### 예제

```kotlin
fun main(args: Array<String>) {
    val student_: Student_ = Student_()

    student_.eat()
    student_.sleep()
}

// () 생성자가 없다
// 함수 구현 부분이 없다
interface Person_ {
    fun eat()
    fun sleep()
}

// 구현은 이곳에서 진행
// 이 클래스는 Person_의 타입이 된다 (상속이 만들어낸 특징 동일하게 적용됨)
class Student_ : Person_ {
    override fun eat() {
    }

    override fun sleep() {
    }
}
```

<br>

### 인터페이스 특징 2

- 인터페이스도 구현이 있는 함수를 만들 수 있다
- 인터페이스에 구현이 있는 함수는 그 인터페이스를 구현하는 클래스에서 함수를 구현할 필요가 없다
- 인터페이스에 구현이 없는 함수는 그 인터페이스를 구현하는 클래스에서 함수를 반드시 구현해야 한다

```kotlin
fun main(args: Array<String>) {
    val student = Student__()
    student.sleep()  // 잔다
}

interface Person__ {
    fun eat() {
        println("먹는다")
    }

    fun sleep() {
        println("잔다")
    }

    // 반드시 구현하게 만들어주는 키워드 abstract
    abstract fun study()
}

class Student__ : Person__ {
    override fun study() {
    }
}

class Teacher__ : Person__ {
    override fun study() {
    }
}
```

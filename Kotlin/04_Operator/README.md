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









## 🔥 연산자 (Operator)

### 산술 연산자

> +, -, *, / (몫만 취함), % (나머지만 취함)

```kotlin
var a = 10 + 1
var b = 10 - 1
var c = 1 * 9
var d = 20 / 3
var e = 20 % 3
```

<br>

### 대입 연산자

> 좌변 = 우변 (우변 값이 좌면에 들어간다)

```kotlin
val f = 5
// val 5 = f (error)
```

<br>

### 복합 대입 연산자

> +=, -=, *=, /=, %=
>
> 의미 : a += 10 -> a = a + 10

```kotlin
a += 10
b -= 10
c *= 3
d /= 4
e %= 2
```

<br>

### 증감 연산자

> ++, --

```kotlin
a++
b--
```

<br>

### 비교 연산자

> \>, >=, <, <=, ==, !=

True == True -> True

True == False -> False

True != True -> False

True != False -> True

```kotlin
val g = a > b
val h = a == b
val i = g != h
```

<br>

### 논리 연산자

> &&, ||, !

True && True -> True

True || False -> True

!True -> False

!False -> True

```kotlin
val j = h && i
val k = h || i
val l = !h
```


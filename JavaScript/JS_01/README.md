<p align='middle'>
	<img src="../README.assets/js.png">
</p>
<br>

<h2 align='middle'>자바스크립트 기초</h2>

<p align='middle'>자바스크립트(ES6) 공부 후 정리 하였습니다</p>
<br>
<br>


## 🔥 Goal

- 강의에서 봤던 예시 코드들을 따라서 실행해본다
- 자바스크립트 기초를 탄탄히 다진다
- 자주 사용했던 언어(Python)와 다른 문법을 자세히 살펴본다



## ⭐목차

> 변수
>
> 타입
>
> - let
> - const
>
> 자료형
>
> - 문자형
> - 숫자형
> - Boolean
> - null과 undefined
> - typeof
>
> 대화상자
>
> - alert()
> - prompt()
> - confirm()
>
> 형변환
>
> - String()
> - Number()
> - Boolean()
>
> 연산자
>
> - 연산자 줄여서 쓰기
> - 증가, 감소 연산자
>
> 비교 연산자
>
> - 동등 연산자
> - 일치 연산자



## 🔧세부 내용

### 변수

```javascript
name = 'Min'
age = 30
```



### 타입

- let

  > 변할 수 있는 값 선언할 때

- const

  > 변하지 않는 값 선언할 때



### 자료형

- 문자형

  👉 " " or ' ' 사용 가능

  👉 ``(백틱)은 변수나 표현식도 넣을 수 있다

  ```javascript
  `My name is ${name}`
  `나는 ${20+1}살 입니다`
  ```

- 숫자형

  NaN 주의! Not a number 라는 뜻

- Boolean

  true / false

- null과 undefined

  null은 존재하지 않는 값

  undefined 값이 할당되지 않았을 때

- typeof

  타입을 알 수 있음

  

### 대화상자

- alert()

  👉 메시지를 띄워서 알리는 용도

- prompt()

  👉입력 받음

  👉 두번째 인수는 default 값으로 설정 가능

- confirm()

  👉 확인 받음

```javascript
const name = prompt('이름을 입력하세요')
alert(`안녕하세요, ${name}님. 환영합니다`)
```



### 형변환

- String() 

  문자형으로 변환

- Number() 

  숫자형으로 변환

- Boolean()

  불린형으로 변환

  

### 연산자

- 우선순위

  /  *   ` >`    +  -

- 연산자 줄여서 쓰기

  num += 5

- 증가, 감소 연산자

  ```javascript
  let num = 10
  let result = num++
  ```

  👉 증가시키기 전인 10이 할당

  ```javascript
  let result = ++num
  ```

  👉 증가시킨 값 11이 할당



### 비교 연산자

- 동등 연산자

  ```javascript
  const a = 1
  const b = '1'
  console.log(a == b)
  ```

  👉 true 반환

- 일치 연산자

  ```javascript
  console.log(a === b)
  ```

  👉 false 반환

  👉 3개는 타입까지 비교

  👉 동등보단 일치 사용하기 !!

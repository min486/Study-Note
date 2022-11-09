<div align="center">
  <p>
    <img src="../README.assets/python.png">
  </p>
  <br>
  <h2>내장함수</h2>
  <p>코딩테스트 대비 내장함수 정리</p>
  <br>
  <br>
</div>







## 🧊 알파벳순 정리

> - abs
> - all
> - any
> - bool
>
> - count
> - dict
>
> - filter
>
> - float
>
> - format
>
>   - format() 내장 함수를 이용하면 숫자를 다른 진수의 문자열로 바꿀 때 접두어(0b, 0o, ox 등)를 제외할 수 있다.
>
>     ```python
>     >>> format(42, 'b') # 2진수
>     '101010'
>     >>> format(42, 'o') # 8진수
>     '52'
>     >>> format(42, 'x') # 16진수
>     '2a'
>     ```
>
> 
>
> - index
>
> - int
>
> - isalpha / isalnum
>
> - 
>
> - join
>
>   > 매개변수로 들어온 리스트의 값과 값 사이에 구분자를 넣어서 하나의 문자열로 바꾸어 반환하는 함수
>
>   ### '구분자'. join(리스트)
>
>   ```python
>   ex = ['a', 'b', '1', '2']
>   >>> ''.join(ex)
>   ab12
>   >>> '_'.join(ex)
>   a_b_1_2
>   ```
>
> - len
>
> - list
>
> - map
>
> - max / min
>
> - ord / chr
>
>   > ord(c)는 문자의 유니코드(Unicode) 값을 돌려주는 함수
>   >
>   > 문자 => 정수
>
>   > chr(i)는 유니코드 값을 입력받아 그 코드에 해당하는 문자를 출력하는 함수
>   >
>   > 정수 => 문자
>
>   *a~z 문자와 97~122 숫자 / A~Z 문자와 65~90 숫자 서로 변환
>
>   ```python
>   >>> ord('a')
>   97
>   >>> chr(97)
>   'a'
>   ```
>
> 
>
> - range
>
> - remove
>
> - replace 확인!!
>
> - reverse / reversed
>
> 
>
> - round
>
>   > 반올림하는 함수, 소수점을 n번째 까지만 표현, n 안적으면 반올림해서 정수로 표현
>
>   ### round(실수, n)
>
>   ```python
>   n = 0.4666
>   >>> round(n,2)
>   0.47
>   >>> round(n,3)
>   0.467
>   >>> round(n)
>   0
>   ```
>
> 
>
> - sort / sorted
>
> - set
>
> - split
>
> - str
>
> - sum
>
> - type
>
> - upper / lower
>
>   > string.upper()는 문자열 내부에 모든 알파벳을 대문자로 변경
>
>   > string.lower()는 문자열 내부에 모든 알파벳을 소문자로 변경
>
>   ```python
>   str = 'Hello'
>   >>> str.upper()
>   HELLO
>   >>> str.lower()
>   hello
>   ```
>
> 
>
> - isupper / islower
>
>   > string.isupper()는 문자열 내부에 있는 모든 문자가 대문자인지 검사하는 함수
>
>   > string.islower()는 문자열 내부에 있는 모든 문자가 대문자인지 검사하는 함수
>
>   ```python
>   str1 = 'Hello'
>   str2 = 'WORLD'
>   >>> str1.islower()
>   False
>   >>> str2.isupper()
>   True
>   ```
>
> 
>
> - zip

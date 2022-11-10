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
>
>   > abs(x) 는 어떤 숫자를 입력받았을 때, 그 숫자의 절댓값을 돌려주는 함수
>
>   ```python
>   >>> abs(-3)
>   3
>   >>> abs(-1.2)
>   1.2
>   ```
>
> - all
>
>   > all(x) 는 반복 가능한(iterable) 자료형 x를 입력 인수로 받으며 이 x의 요소가 모두 참이면 True, 
>   >
>   > 거짓이 하나라도 있으면 False
>
>   ```python
>   >>> all([1, 2, 3])
>   True
>   >>> all([1, 2, 3, 0])
>   False
>   >>> all([])
>   True
>   ```
>
> - any
>
>   > any(x) 는 반복 가능한(iterable) 자료형 x를 입력 인수로 받으며 이 x의 요소 중 하나라도 참이 있으면 True, 
>   >
>   > x가 모두 거짓일 때에만 False 
>   >
>   > => all(x)의 반대
>
>   ```python
>   >>> any([1, 2, 3, 0])
>   True
>   >>> any([0, ""])
>   False
>   >>> any([])
>   False
>   ```
>
> - bool
>
> - count
>
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
>   > int(x) 는 문자열 형태의 숫자나 소수점이 있는 숫자 등을 정수 형태로 돌려주는 함수
>
>   ```python
>   >>> int('3')
>   3
>   >>> int(3.4)
>   3
>   ```
>
> 
>
> - isalpha / isalnum
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
>   > len(s) 은 입력값 s의 길이(요소의 전체 개수)를 돌려주는 함수
>
>   ```python
>   >>> len("python")
>   6
>   >>> len([1,2,3])
>   3
>   >>> len((1, 'a'))
>   2
>   ```
>
> - list
>
>   > list(s) 는 반복 가능한 자료형 s를 입력받아 리스트로 만들어 돌려주는 함수
>
>   ```python
>   >>> list("python")
>   ['p', 'y', 't', 'h', 'o', 'n']
>   >>> list([1, 2, 3])
>   [1, 2, 3]
>   ```
>
> - map
>
>   > map(f, iterable) 은 함수(f)와 반복 가능한(iterable) 자료형을 입력으로 받는다.
>   >
>   > map은 입력받은 자료형의 각 요소를 함수 f가 수행한 결과를 묶어서 돌려주는 함수
>
> - max / min
>
>   > max(iterable) 는 인수로 반복 가능한 자료형을 입력받아 그 최댓값을 돌려주는 함수
>
>   > min(iterable) 은 인수로 반복 가능한 자료형을 입력받아 그 최솟값을 돌려주는 함수
>
>   ```python
>   >>> max([1, 2, 3])
>   3
>   >>> min([1, 2, 3])
>   1
>   ```
>
> - ord / chr
>
>   > ord(c) 는 문자의 유니코드(Unicode) 값을 돌려주는 함수
>   >
>   > 문자 => 정수
>
>   > chr(i) 는 유니코드 값을 입력받아 그 코드에 해당하는 문자를 출력하는 함수
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
> - range
>
>   - range(MAX) - 인수가 한 개
>
>     > 0 에서부터 MAX - 1까지의 숫자 연속된 객체로 만들어서 반환해주는 함수 (MAX 미포함)
>     > (0 <= x < MAX) 
>
>   - range(MIN, MAX) - 인수가 두 개
>
>     > MIN 에서부터 MAX - 1까지의 숫자를 연속된 객체로 만들어서 반환 (MAX 미포함)
>     >
>     > (MIN <= x < MAX)
>
>   - range(MIN, MAX, GAP) - 인수가 세 개일 때
>
>     > MIN에서 MAX -1까지의 숫자를 연속된 객체로 만들어 주는데, 각 숫자들 사이에 GAP 만큼의 차이를 둔다
>     
>     ```python
>     >>> for i in range(3, -1, -1):
>     		print(i, end=' ')
>     3 2 1 0
>     >>> range(0, 10, 2)
>      0, 2, 4, 6, 8
>     ```
>   
>
> - remove
>
> - replace 확인!!
>
> - reverse / reversed
>
>   > 모두 리스트의 요소를 뒤집을 때 사용
>
>   ### [리스트].reverse()
>
>   > list 타입에서만 사용 가능
>
>   - 값을 반환하지 않는다 => 변수에 값을 담기 불가능
>
>   - 해당 리스트의 원형을 바꾼다
>
>   ``` python
>   >>> B = A.reverse()
>   None
>   >>> print(A.reverse())
>   None
>   # 위의 코드들은 A라는 리스트를 모두 reverse 해준다. 
>   # 하지만 B라는 변수에 담거나 print를 바로 할 수 없다.
>   # 코드 이후에 print(A) 해야 reversed 된 값들이 나온다.
>   
>   a = [1, 2, 3, 4]
>   a.reverse()
>   >>> print(a)
>   [4, 3, 2, 1]
>   ```
>
>   ### reversed([리스트])
>
>   > list 뿐만 아니라 tuple, string, dictionary 에도 사용 가능
>
>   - 객체 값을 반환한다. 반환된 값은 다시 다른 메서드를 통해 표현될 수 있다
>   - 해당 객체의 원형을 바꾸지 않는다
>
>   ```python
>   a = [1, 2, 3]
>   b = reversed(a)
>   >>> print(b)
>   [3, 2, 1]
>   >>> print(a)
>   [1, 2, 3]
>   ```
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
>   > sum(iterable) 은 입력받은 리스트나 튜플의 모든 요소의 합을 돌려주는 함수
>
>   ```python
>   >>> sum([1,2,3])
>   6
>   >>> sum((4,5,6))
>   15
>   ```
>
> - type
>
> - upper / lower
>
>   > string.upper() 는 문자열 내부에 모든 알파벳을 대문자로 변경
>
>   > string.lower() 는 문자열 내부에 모든 알파벳을 소문자로 변경
>
>   ```python
>   str = 'Hello'
>   >>> str.upper()
>   HELLO
>   >>> str.lower()
>   hello
>   ```
>
> - isupper / islower
>
>   > string.isupper() 는 문자열 내부에 있는 모든 문자가 대문자인지 검사하는 함수
>
>   > string.islower() 는 문자열 내부에 있는 모든 문자가 대문자인지 검사하는 함수
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
> - zip
>
>   > zip(*iterable) 은 동일한 개수로 이루어진 자료형을 묶어 주는 역할을 하는 함수
>
>   *iterable 은 반복 가능(iterable)한 자료형 여러 개를 입력할 수 있다는 의미
>
>   ```python
>   >>> list(zip([1, 2, 3], [4, 5, 6]))
>   [(1, 4), (2, 5), (3, 6)]
>   >>> list(zip([1, 2, 3], [4, 5, 6], [7, 8, 9]))
>   [(1, 4, 7), (2, 5, 8), (3, 6, 9)]
>   >>> list(zip("abc", "def"))
>   [('a', 'd'), ('b', 'e'), ('c', 'f')]
>   ```
>
>   


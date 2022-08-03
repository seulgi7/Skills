# PART01. 시작하기
## Python설치
보통 맥에는 python 2.x버전이 자동적으로 설치되어 있지만 python3을 사용할려며 별도로 python3을 설치해야한다.
+ www.python.org에서 다운로드 메뉴 - Python 3.5이상 선택해서 다운로드
+ 다운로드 받은 폴더에서 .pkg파일을 실행.
+ "확인되지 않은 개발자가 배포했기 때문에 열 수 없습니다"라는 메세지가 뜨면 승인을 누르고 다시 한번 파일을 실행
+ 계속/동의/설치 버튼을 눌려주면서 설치
+ 설치 확인
  + command + space를 눌러서 나오는 창에 터미널을 치고, 엔터를 눌러서 터미널실행
  + 터미널화면에서 python3이라고 입력해서 Python 3.5.1 (v3.5.1:37a07cee5969, Dec 5 2015, 21:12:44)와 비슷한 글이 뜨면 성공

## printf함수

# PART02.변수의 계산
## 변수 사용하기
```python
  identity = '지구인'
  number_legs = 2
  print('안녕! 나는', identity, '이야. 나는 다리가', number_legs, '개 있어.')
  
  identity = '외계인'
  number_legs = 4
  print('안녕! 나는', identity, '이야. 나는 다리가', number_legs, '개 있어.')
```
### 변수의 선언
+ identity = '지구인'
   + <strong>변수의 이름</strong> : 가자 왼쪽에 identity라고 쓰이 부분
   + <strong>= (등호)</strong> : 변수에 값을 저장하라는 의미
   + <strong>값</strong> : '지구인'이라고 쓰인 값 
   + 즉, identify라는 변수에 '지구인'이라는 값으 저장하라는 명령

### 변수의 사용 
+ identity = '지구인'이라고 변수를 선언하고 나면, 변수의 이름을 가지고 그 값을 불러와서 사용할 수 있다.
+ 다음 두 코드는 같은 결과를 출력
  +  print('안녕 나는','지구인','이야')
  +  print('안녕 나는',identity,'이야')
+ 변수에 새로운 값을 입력하는 방법은 변수를 선언하는 것과 같다.
  +  identity = '외계인'이라고 쓰면 이후부터 identity라는 변수의 값은 '외계인'이라는 값을 가지게 된다.

## 4. 주석
### 주석
+ 코드를 설명하기 위해 코드에 적어 놓은 프로그래밍 언어가 무시하는 문자
+ 코드를 임시로 작동하도록 꺼 두기 위해서도 사용
+ #을 쓰고 그 오른쪽에 주석을 입력
+ 여러줄을 주석으로 처리하고 싶을때는 따옴표 """로 그 내용을 둘러싼다.
```python
 #정체와 다리의 수를 출력하는 코드입니다.
    identity = '지구인' #정체1
    number_of_legs  #다리의 수

    print('안녕!')

    #이 아래 줄은 주석처리 되었기 때문에 실행되지 않습니다.
    #print('너는 누구니?')

    """
    여러줄을
    한 번에
    주석처리할때는 이렇게 따옴표 3개로 
    내용을 감싸주세요.
    """
```

## 5. 숫자와 문자열
### 숫자
+ 변수에 숫자를 넣는 예
  + a = 33
+ 숫자는 계산이 가능 ( 수학 연산이 가능 )
  + 더하기 + (summation)
    + summation = a + 1   
  + 곱하기 * (multiply)
    + multiply = 9 * 9
  + 나누기 / (divide)
    + divide = 30 / 5    
  + 나머지 % (remainder)   
    + remainder = 15 % 4
    + 15를 4로 나눈 다음의 나머지 = 3
  + 거듭제곱 ** (power)
    + power = 2 ** 10 (2의 10승)   

```python
a=33
b=3

summation = a + b
multiply = a * b
divide = a / b 
remainder = a % b 
power = a ** b

print("summation은 ",summation,"입니다.") # summation은  36 입니다.
print("multiply는 ",multiply,"입니다.") # multiply는  99 입니다.
print("divide는 ",divide,"입니다.") # divide는  11.0 입니다.
print("remainder는 ",remainder,"입니다.") # remainder는  0 입니다.
print("power는",power,"입니다.") # power는 35937 입니다.
```

### 문자열
+ 따옴표로 감싸진 글
+ 변수에 문자열을 넣는 예
  + my_name = 'Python'
+ 텍스트 두개를 더하면 문자열이 이어붙여짐
  + text = '2015' + '1991'하고 나면 text에는 '20151991'이라는 값이 저장
+ 텍스트는 더하기만 가능하고, 빼기(-)등 다른 계산은 불가능

```python
  text = '2015' + '1991'
  number = 2015 + 1991
  
  print(text) # 20151991
  print(number) # 4006
  
  text_minus = text - '1991'
  print(text_minus) # TypeError: unsupported operand type(s) for -: 'str' and 'str' 
```

# PART03. 조건문
## if문
### 조건문
+ 특정 조건에 따라 다른 동작을 할 수 있도록 해 주는 구문
```python
 people = 3
 apple = 20
  if people < apple / 5 :
    print('신나는 사고 파티! 배 터지 먹자!!')
  if apple % people > 0 :
    print('사과 수가 많ㅈ 않아! 몇 개는 쪼개 먹자!')
  if people > apple :
    print('사람이 너무 많아! 몇 명은 못먹겠네')   
```
+ 구조
  + <strong>if 예약어</strong> : 조건문의 시작을 알림
  + <strong> 조건</strong>: people > apple와 같이 참/거짓을 판단할 수 있는 조건
  + <strong>:</strong> 조건이 끝났다는걸 표현한하는 명령
  + 실행하고자 하는 코드. 코드는 탭키를 이용해서 들여서 쓴다.
    + print('사람이 너무 많아! 몇 명은 못먹겠네')
    <img width="230" height = "150" alt="image" src="https://user-images.githubusercontent.com/107892937/182723996-338c4365-82ae-4da3-9dd2-1580c4bd854f.png"> 
    <img width="230" height = "150" alt="image" src="https://user-images.githubusercontent.com/107892937/182724033-ba6a8748-7767-4c90-bb91-0d02cc7c48e9.png">
    <img width="230" height = "150" alt="image" src="https://user-images.githubusercontent.com/107892937/182724117-4c2da230-2094-40e9-b66d-f5ee52648d1a.png">
    <img width="230" height = "150" alt="image" src="https://user-images.githubusercontent.com/107892937/182724164-39d565b0-d005-462a-aa61-d7592fb4c25e.png">



 

  

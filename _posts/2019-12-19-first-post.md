---
layout: article
title: python
tags: python
---

# Tody I Learned Python

> **Note**: 파이썬 기본 문법


## Table of Contents

  1. [변수](#변수)
  1. [타입](#타입)
  1. [연산자](#연산자)
  1. [조건문](#조건문)
  1. [반복문](#반복문)
  1. [함수](#함수)
  1. [문자열관리](#문자열관리)
  1. [리스트와튜플](#리스트와튜플)  
  1. [사전과집합](#사전과집합)  
  1. [컬렉션관리](#컬렉션관리)  
  1. [표준모듈](#표준모듈)  
  1. [예외처리](#예외처리)  
  1. [파일](#파일)  
  
  
### 변수
  - 1.1 **기본구조**\
    -세미콜론(;)을 사용하지 않는다.\
    -대문자와 소문자를 구분한다.\
    -주석은 #으로 처리하고 여러줄 주석은 지원안한다.\
    -들여쓰기로 블록을 구분한다.

    - 출력
    >  코드의 결과를 보기위해 print로 출력한다. []안에 있는 내용은 생략가능하다.
    ```python
    print(출력 내용, [sep=구분자], [end=끝 문자])
    ```
  
    - 입력
    > 사용자와 상호 작용을 위해서 사용하고 입력 받은 내용은 문자열 형식이다.(숫자를 입력 받아도 문자열로 저장된다)
    ```python
    변수 = input(‘입력 받을 내용')
    ```
    
  - 1.2 **변수**\
    -메모리에 이름을 붙여 값을 저장하는 것\
    -별도의 타입을 지정하지 않는다.\
    -스페이스,특수문자,내부키워드,숫자로 시작하는 변수명은 사용할 수 없다.
    
**[⬆ back to top](#table-of-contents)**

### 타입
  - 2.1 **수치형**
  
    - 정수형 타입
    > 가격, 나이, 점수 등의 일상적으로 사용하는 수와 음수는 표현가능하지만 소수점은 표현할 수 없다. 또한 길이 제한이 없다.
    ```python
    print(9999) 
    print(-999)
    print(2 ** 100)
    ```
    - 실수형 타입
    > 평균이나 무게와 같이 소수점 이하의 정밀한 값을 표현하기위해 사용한다.
    ```python
    print(99.999) 
    print(82.8)
    print(-3.1515)
    ```
  - 2.2 **문자열**

    - 문자열
    > 따옴표로 감싸진 말이나 문장이다."문장" 또는 '문장'으로 사용된다.
    ```python
    print("Hello World!")
    a = "Hello World!" 
    print(a)
    
    print('Hello World!') 
    a = 'Hello World!' 
    print(a)
    ```

    > 따옴표를 같이 사용하기 위해서는 앞에 \을 붙여준다.
    ```python
    print("I Say \"Help\" to you") 
    print('I Say \'Help\' to you')
    print("Let's go")
    ```
    
    - 확장열
    > 개행이나 탭등 문자열에 담기힘든 문자나 특수문자는 \문자를 앞에 붙여준다.
    ```python
    \n - 개행
    \t - 탭
    \' - 작은 따옴표
    \" - 큰 따옴표
    \\ - 문자
    ```
    
    - 긴 문자열
    > 너무 긴 문자열은 따옴표 세 개를 연속으로 사용하고 개행되는 곳에 \를 사용하면 개행이 되지 않는다.
    ```python
    s = """강나루 건너서 밀받 길을 구름에 달 가듯이 가는 나그네 \ 
    길은 외줄기 남도 삼백리 술 익는 마을마다 타는 저녁놀 \ 
    구름에 달 가듯이 가는 나그네""
    ```
  - 2.3 **그 외 타입**

    - Bool
    > 참 또는 거짓으로 True, False를 반환한다.
    ```python
    a = True 
    print(a)  
    a = 5 b = a == 5 
    print(b)
    b = a == 7 print(b)
    ```
    - list
    > 여러개의 값을 저장하는 데이터 타입으로 변경가능하고 []를 사용한다.
    ```python
    member = ["손오공", "저팔계", "사오정", "삼정법사"] 
    print(member)
    ```
    - tuple
    > 여러개의 값을 저장하는 데이터 타입으로 변경이 불가능하고 ()를 사용한다.
    ```python
    member = ["손오공", "저팔계", "사오정", "삼정법사"] 
    print(member)
    ```
    
**[⬆ back to top](#table-of-contents)**

### 연산자
  - 3.1 **산술 및 대입**
    - 산술 연산자
    > + 더하기, - 빼기, * 곱하기, / 나누기
    ```python
    print(3 + 4)    # 7 
    print(5 - 2)    # 3
    print(2 * 4)    # 8 
    print(8 / 2)    # 4.0
    ```
    - 고급 연산자
    > ** 거듭제곱, // 정수나누기, % 나머지
    ```python
    print(11 ** 2)  # 121
    print(5 / 2)    # 2.5 
    print(5 // 2)   # 2
    print(7 % 2)    # 1 
    print(8 % 3)    # 
    ```
    
    - 복합 대입 연산자
    > 우변의 값이나 수식을 계산하여 좌변에 대입한다.
    ```python
    a = 5
    a += 1
    print(a)
    ```
  - 3.2 **타입 변환**  
    - 문자열 연산
    > 문자열도 연산이 가능하지만 수학적인 연산과는 다르다.
    ```python
    a = 5
    s1 = "대한민국"
    s2 = "만세" 
    print(s1 + s2) 
    print("대한민국" + "만세")
    print("만세" * 5) # 만세가 5번 출력된다.
    print("-" * 40) # -가 40번 출력된다.
    ```
    
    - 정수와 문자열 연산
    > 정수와 문자열은 섞어서 사용할 수 없어서 같은 타입으로 바꿔서 사용해야한다.
    ```python
    print("대한민국" + str(2002)
    print("대한민국" + str(2002)
    ```    

    - 실수의 변환
    > 문자열을 실수로 변환 : float, 실수를 정수로 변환 : int, 반올림 : round
    ```python
    print(10 + float("10.4"))         # 20.4 
    print(10 + int(22.5))             # 32 
    print(10 + int(float("12.4")))    # 22
    print(int(2.54))                  # 2 
    print(round(2.54))                # 3 
    print(round(2.54, 1))             # 2.5 / 소수점 한자리수까지남긴다.
    print(round(123456, -3))          # 123000 / 뒤에서 3자리를 0으로 처리한다.
    ```
    
**[⬆ back to top](#table-of-contents)**

### 조건문
  - 4.1 **if 조건문**
    - if문
    > 조건의 진위 여부에 따라 명령을 실행하며 if키워드를 쓰고 조건과 콜론(:)을 찍은다음 명령을 작성한다.
    ```python
    age = 10 
    if age < 19:   
    print("청소년 입니다")
    ```

    - 비교 연산자
    > 두 값의 같고 다름과 대소관계를 비교하여 True와 False로 리턴한다.
    ```python
    == - 같다
    != - 다르다
    < - 우변이 크다
    > - 좌변이 크다
    <= - 우변이 크거나 같다
    >= - 좌변이 크거나 같다
    ```
    
    - 논리 연산자
    > 두 개 이상의 조건을 한번에 점걸할 때 사용한다.
    ```python
    and - 두 조건이 모두 참이다.
    or - 두 조건중 하나라도 참이다.
    not - 조건을 반대로 뒤집는다.
    ```
    ```python
     a = 3 
     b = 4 
     if a == 3 and b == 4:   
       print("AND OK") 
     if a == 3 and not b == 8:   
       print("AND OK") 
     if a == 3 or b == 8:   
       print("OR OK"
    ```   
  - 4.2 **블록 구조**
    - 블록 구조 
    > 들여쓰기 수준이 같을때(if문이 True일때만 출력된다)
    ```python
    age = 16 
    if age < 19:   
      print("청소년 입니다.")   
      print("공부 열심히 해야지")
    ```
    > 들여쓰기 수준이 다를때(공부 열심히 해야지는 if문과 상관없이 무조건 출력된다)
    ```python
    age = 16 
    if age < 19:   
      print("청소년 입니다.")   
    print("공부 열심히 해야지")
    ```
    - else문
    > 조건의 진위에 따라 실행할 명령을 선택한다.한,번만 사용할 수 있다.
    ```python
    age = 22 
    if age < 19:   
      print("학생입니다") 
    else:   
      print("어서 옵쇼")
    ```

    - elif문
    > if와 else사이에 여러개 들어갈 수 있으며 조건을 더 추가할때 사용한다.
    ```python
    age = 22 
    if age < 19:   
      print("학생입니다") 
    elif age< 25:
      print("대학생입니다")
    else:   
      print("어서 옵쇼")
    ```
    - elif문 중첩
    > if안에 또 if문이 들어갈 수 있다.
    ```python
    age = 23 
    if age < 19:   
      print("청소년입니다.") 
    else:   
    if age < 25:       
      print("대학생입니다.")   
    else:       
      print("어서 옵쇼")
    ```
    - Rock Scissor Paper GAME
    > 컴퓨터와 가위바위보 게임하는 예제
    ```python
    import random
    com = ['가위','바위','보']
    computer = com[random.randint(0,2)]   #com리스트에 담겨진 값을 랜덤으로 인덱싱하여 가져온다
    me = input("가위 바위 보!!")
    print("컴퓨터 : "+computer,"",sep="\n")

    if computer == me:
        print("비겼습니다 한번더")
    elif computer == "가위" and me == "바위":
        print("이겼습니다")
    elif computer == "바위" and me == "보":
        print("이겼습니다")
    elif computer == "보" and me == "가위":
        print("이겼습니다")
    elif me != "가위" and me !="바위" and me !="보":
        print("오타났습니다")
    else:
        print("졌습니다 다음기회에")
    ```
**[⬆ back to top](#table-of-contents)**

### 반복문
  - 5.1 **반복문**
    - while 반복문
    > 조건이 만족하는 동안 계속 실행된다.
    ```python
    student = 1 
    while student <= 5:   
      print(student, "번 학생의 성적을 처리한다.")   
      student += 1
    ``` 
    - for 반복문
    > 컬렉션의 요소를 순서대로 반복하면서 실행된다.
    ```python
    for student in [1, 2, 3, 4, 5]:   
      print(student, "번 학생의 성적을 처리한다.")
    ``` 
    - range
    > 컬렉션의 범위가 넓다면 하나하나 입력할 수 없으니 처음과 끝값을 입력해서 컬렉션을 만들어준다. 끝값은 +1해서 입력해주자
    ```python
    sum = 0 
    for num in range(1, 101):   
      sum += num

    print("sum = ", sum)
    ``` 
    - 제어 변수
    > 반복문 내부에서 변화를 주기 위해 사용한다.
    ```python
    for num in range(1, 11):   
      if num % 2 == 0:       #2로 나눌때 나머지가 0이라면 짝수겠지
        print(num, "짝수")   
      else:       
        print(num, "홀수")
    ``` 

    - break
    > 반복문을 실행 중에 중지해야할 때 사용한다.
    ```python
    score = [92, 86, 68, 120, 56] 
    for s in score:   
      if s < 0 or s > 100:      
        break   
      print(s)
    print("성적 처리 끝")
    ``` 
    
    - continue
    > 반복문중 건너 뛰고 나머지를 수행할 때 사용한다.
    ```python
    score = [92, 86, 68, -1, 56] 
    for s in score:   
      if s == -1:       
        continue   
      print(s)
    print("성적 처리 끝")
    ``` 
  - 5.2 **루프의 활용**
    - 이중 루프(구구단)
    > 반복문 안에 다른 반복문이 중첩되어 사용한다.
    ```python
     for i in range(2,10):
         print(i,"단")             # 시작하기전 몇단인지 알려주기위해
         for j in range(1,10):
             print(i,"x",j,"=",i*j)
         print()                   # 단이 끝나고 한줄 띄어주기 위해
    ``` 
    
    - 무한 루프(문제 맞출때까지)
    > 반복 횟수를 정하지 않고 무한히 반복하다가 중간에 조건을 충족하면 탈출한다.while문만 가능하고 for문은 불가능하다.
    ```python
    print("3 + 4 = ?") 
    while True:   
      a = int(input("정답을 입력하시오 : "))   
      if a == 7:       
        break 
    print("참 잘했어요")
    ``` 
**[⬆ back to top](#table-of-contents)**

### 함수
  - 6.1 **함수와 인수**
    - 함수
    > 함수는 반복되는 코드를 줄여주고 def키워드로 생성한다. 또한 코드수정이 요이하고 재사용하기 쉽다.
    > 파이썬은 처음부터 순서대로 읽어 실행하는 인터프리터 언어이기 때문에 함수를 호출하기전에 함수가 먼저 정의되어 있어야 한다.
    ```python
    def calcsum(n):              # 함수정의
      sum = 0   
      for num in range(n + 1):       
        sum += num   
      return sum
      
      print(calcsum(4))          # 호출
    ``` 
    
    - 인수 or 매개 변수
    > 인수는 ()안에 개수 제한없이 입력하여 전달가능하다.
    ```python
    def calcsum10():          # 인수가 없는 경우
      sum = 0   
      for num in range(11):       
        sum += num   
      return sum
    ``` 
    ```python
    def calcsumrange(begin, end):      # 인수가 여러개인 경우
      sum = 0   
      for num in range(begin, end +1): #  끝값은 +1을 시켜줘야한다  
        sum += num   
      return sum

      print("3 ~ 7 =", calcsumrange(3, 7))
     ``` 
     
    - 리턴값
    > 함수 실행 결과를 돌려주고 값이 없거나 하나만 쓸 수 있다.
    
    - pass
    > 아무 동작도 하지 않기 때문에 함수의 내용을 나중에 작성 해야할 경우 사용한다.
    ```python
    def calctotal():   # 함수의 내용을 나중에 작성할 때
      pass
    ``` 
    ```python
    if sum >= 90:       # if else내용을 나중에 작성할 때
      pass 
    else:   
      pass
    ``` 
  - 6.2 **인수의 형식**
    - 가변인수
    > 임의 개수의 인수를 받을때 인수앞에 \*를 붙여서 사용한다. 가변인수는 인수의 마지막에 와야한다.
    ```python
    def intsum(*ints):            # 인수를 모두 더할 수 있다
      sum = 0
      for num in ints:
        sum += num 
      return sum
      
      print(intsum(1, 2, 3)) 
    ```
    - 인수의 기본값
    > 잘 변하는 값이 아니라면 인수의 기본값을 지정해서 호출할 때 생략이 가능하다.
    ```python
    def calcstep(begin, end, step = 1):
      sum = 0
      for num in range(begin, end + 1, step):
        sum += num 
      return sum
      print(calcstep(1, 10))
    ```
    - 키워드 인수
    > 인수가 많을경우 호출할때 인수의 키워드를 지정해서 호출할 수 있다.
    ```python
    def calcstep(begin, end, step):
      sum = 0
      for num in range(begin, end + 1, step):
        sum += num return sum

    print(calcstep(begin=3, end=5, step=1)) 
    print(calcstep(step=1, end=5, begin=3))
    ```
  - 6.3 **변수의 범위**
    - 지역변수
    > 함수 내부에 선언하는 변수로 밖에서는 사용할 수 없다.
    ```python
    def kim():
        temp = "김과장의 함수" 
        print(temp)

    print(temp)              # NameError
    ```
    - 전역변수
    > 함수 밖에 선언하는 변수로 어디서나 사용할 수 있다.
    ```python
    salerate = 0.9 
    def kim():
        print("오늘의 할인율 :", salerate)
    def lee():
        price = 1000
        print("가격 :",price * salerate)
    kim()                # 결과값 : 0.9
    salerate = 1.1 
    lee()                # 결과값 : 1100   함수 호출전에 선언된 변수의 값이 적용된다.(선언할때는 상관없다)
    ```
    - docstring
    > 함수의 사용법이나 주의사항을 남길때 선언문과 본체사이에 작성한다. help함수를 사용해 출력가능하다.
    ```python
    def calcsum(n):
        """합계를 구해서 리턴한다."""
        sum = 0
        for i in range(n+1):
            sum += i
        return sum

    help(calcsum)        # 결과값 : 합계를 구해서 리턴한다.
    ```
  
**[⬆ back to top](#table-of-contents)**

### 문자열관리
  - 7.1 **문자열 분리**
    - 첨자
    > 앞에서는 0부터 시작하고 뒤에서는 -1부터 시작한다.
    ```python
    s = "python" 
    print(s[2])   #t
    print(s[-2])  #o
    ``` 
    - 문자열 변경
    > pass
    ```python
    pass
    ``` 
  - 7.2 **문자열 메서드**
    - 검색
    > 특정 문자의 위치를 검색하는 메서드로 len 내장함수는 문자열의 길이를 리턴한다.
    ```python
    find - 문자열 위치를 조사한다.                    #문자열이 없을경우 -1리턴
    rfind - 뒤에서부터 가까운 문자열 위치를 조사한다.   #문자열이 없을경우 -1리턴
    index - 문자열 위치를 조사한다.                    #문자열이 없을경우 오류
    count - 특정 문자의 개수를 센다.                   #문자열이 없을경우 0리턴
    ``` 
    ```python
    s = "python programming" 
    print(len(s)) 
    print(s.find('o')) 
    print(s.rfind('o'))     
    print(s.index('r')) 
    print(s.count('n'))
    ``` 
 
    - 조사
    > 특정 문자가 포함되어 있는지 없는지 조사
    ```python
    s = "python programming" 
    print('a' in s) 
    print('pro' in s) 
    print('x' not in s)
    ``` 
    > 특정 문자로 시작하고 끝나는것을 조사 / 변수명.startswith or 변수명.endswith
    ```python
    name = "김한결" 
    if name.startswith("김"):   
      print("김가입니다.") 

    file = "girl.jpg" 
    if file.endswith(".jpg"):   
      print("그림 파일입니다."
    ``` 
    > 모든 문자가 숫자인지 조사 / 변수명.isdecimal()
    ```python
    height = input("키를 입력하세요")                #타입이 문자열이라도 그안에 숫자만 있는지 확인한다.
    if height.isdecimal():
        print("키는 ", height, "입니다.")
    else:
        print("다시 입력하세요")
    ``` 
    
    - 변경
    > 영문의 대소문자를 변경한다
    ```python
    s = "Good morning, my love KIM."
    print(s.upper())                  #GOOD MORNING, MY LOVE KIM.
    print(s.lower())                  #good morning, my love kim.
    print(s.capitalize())             #Good morning, my love kim.
    print(s.title())                  #Good Morning, My Love Kim.
    ``` 
    ```python
    python = input("파이썬의 영문 철자를 입력하시오 :")    #대문자로 입력해도 철자만 맞으면 정답처리
    if python.lower() == "python":   
      print("맞췄습니다.") 
    else:   
      print("땡!!!")
    ``` 
    
    - 분할
    > 구분자를 기준으로 문자열을 분할 할 수 있다. / 변수명.split()
    ```python
    s = "짜장 짬뽕 탕수육"
    print(s.split())                   #결과값 : ['짜장', '짬뽕', '탕수육']
    ``` 
    ```python
    s2 = "서울->대전->대구->부산"
    for j in s2.split("->"):
        print(j)             
    ``` 
    
    - 대체
    > 특정 문자열을 다른 문자열로 바꾼다. / 변수명.replace("바꿀값","바뀔값")
    ```python
    s = "독도는 일본땅이다"
    print(s.replace("일본","한국")))      #결과값 : 독도는 한국땅이다
    ``` 
    - 조인
    > 특정 문자열을 기준으로 문자열을 합친다.
    ```python
    print(",".join("abcd"))                   #결과값 : a,b,c,d
    print(",".join(['a','b','c','d']))        #결과값 : a,b,c,d
    ``` 

  - 7.3 **포맷팅**
    - 포맷팅
    > 문자열 사이사이에 다른 정보를 삽입하기 위한 방법이다. %d-정수, %f-실수, %s-문자열
    ```python
    anni = "광복절"
    mo = 8
    day = 15

    print("%d월 %d일은 %s이다" %(mo,day,anni))  #결과값 : 8월 15일은 광복절이다
    ``` 
    ```python
    num = 1234
    print("%d" %num)       
    print("%10d" %num)    # 총 10자리를 차지해야하니 앞에는 빈칸으로 채워진다.
    print("%1d" %num)     # num이 4자리니 아무리 1d를 입력해도 4자리는 기본으로 차지하게된다.
    ``` 
    ```
    price = [30, 13500, 2000]
    for p in price:
        print("가격:%7d원" % p)    #뒤로 정렬

    for p in price:
        print("가격:%-7d원" % p)   #앞으로 정렬
    ```
    ```
    pie = 3.14159265
    print("%10f" % pie)                     3.141593
    print("%10.8f" % pie)                 3.14159265
    print("%10.5f" % pie)                    3.14159
    print("%10.2f" % pie)                       3.14
    ```
    - 신형 포맷팅
    > {}를 적고 format 메서드의 인수로 넣어준다.
    ```python
    name = "재형" 
    age = 16 
    height = 162.6
    print("이름 :{}, 나이 :{}, 키 :{}".format(name, age, height))
    print("이름 : {1} / 나이 : {0} / 키 : {2}".format(age,name,h))   # 인덱스 번호를 입력해서 순서 설정가능
    print("이름 :{name}, 나이 :{age}, 키 :{height}".format(age= age, height= height, name= name)  # 변수명을 입력해서 순서 설정가능
    ``` 
    
**[⬆ back to top](#table-of-contents)**

### 리스트와튜플
  - 8.1 **리스트**
    - 리스트
    > 여러개의 값을 []괄호를 사용하여 집합으로 저장할 수 있다.
    ```python
    score = [90, 80, 70, 55, 20]
    sum = 0
    for i in score:
        sum += i
    print("총점은? : {}점".format(sum))
    print("평균은? : {}점".format(sum/len(score)))
    ```
    > 리스트의 값은 인덱싱할 수 있다.
    ```python
    nums = [1, 2, 3, 4, 5, 6, 7, 8, 9] 
    print(nums[2:5])         # 2~5까지 
    print(nums[:4])          # 처음부터 4까지 
    print(nums[6:])          # 6에서 끝까지 
    print(nums[1:7:2])       # 1~7까지 하나씩 건너
    ```
    > 리스트의 값은 변경 가능하다.
    ```python
    score = [90,80,66,20,100]
    score[2]=100
    print(score)                  # 결과값 : [90,80,100,20,100]
    ```
    - 이중 리스트
    > 리스트 안에 리스트를 넣을 수 있다.
    ```python
    score = [
        [91,80,54,25],
        [82,25,45,69],
        [22,55,44,88]
    ]
    num = 0
    for i in score:
        sum = 0
        num+=1
        for j in i:
            sum += j
        print("{}반의 총점은 {}입니다".format(num,sum))
        print("{}반의 평균은 {}입니다.".format(num,sum/len(i)))
    ```
    - 리스트 컴프리헨션
    > 리스트 안의 요소가 일정한 규칙을 가졌다면 간단하게 입력가능하다.
    ```python
     nums = [num for num in range(1,11)]
     print(nums)
    ```
  - 8.2 **리스트 관리**
    - 추가
    > append는 맨뒤로 추가하고 insert는 원하는 인덱스 위치에 값을 추가할 수 있다.
    ```python
    nums = [1, 2, 3, 4] 
    nums.append(5) 
    nums.insert(2, 99) 
    print(nums)
    ```
    - 삭제
    > 요소를 삭제할 때는 삭제하는 대상에 따라 방법이 다르다.
    ```python
    score = [88, 95, 70, 100, 99, 80, 78, 50]     
    score.remove(100)        # 값을 삭제할 때
    del score[2]             # 특정 인덱스 값 삭제할 때
    score[1:4] = []          # 특정 범위 값 삭제할 때
    score.pop()              # 마지막 값 삭제할 때
    ```
    - 검색
    > index-위치, count-갯수
    ```python
    score = [88, 95, 70, 100, 99, 80, 78, 50] 
    score.index(100)   # 위치
    score.count(100)   # 갯수
    ```
    > len-길이, max-최대값, min-최소값
    ```python
    score = [88, 95, 70, 100, 99, 80, 78, 50]
    print("학생 수는 {}명 입니다.".format(len(score)))   
    print("최고점수는 {}명 입니다.".format(max(score)))   
    print("최저점수는 {}명 입니다.".format(min(score)))   
    ```
    > in / not in - 있는지 없는지 검색
    ```python
    ans = input("결제 하시겠습니까?")       
    if ans in ['yes','y','네']:
        print("결제가 완료되었습니다.")
    else:
        print("안녕히 가세요")
    ```
    ```
    ans = input("결제 하시겠습니까? ") 
    if ans not in ['no', 'n', '아니오']:   
      print("결제 완료 되었습니다.")
    else:   
      print("안녕히 가세요."
    ```
    - 정렬
    > sort-순서정렬, reverse-반대로 정렬
    ```python
    score = [88, 95, 70, 100, 99, 80, 78, 50] 
    score.sort() 
    score.reverse() 
    ```
    > sorted-원본을 유지하고 순서 정렬
    ```python
    score = [88, 95, 70, 100, 99, 80, 78, 50] 
    score_sort = sorted(score)                  #score는 원본, score_sort는 정렬
    ```
    
  - 8.3 **튜플**
    - 튜플
    > ()를 써서 값을 저장하고 편집이 불가능하다. 하지만 가볍고 속도가 빠르고 편집이 불가능해 안전한 측면이 있다.
    ```python
    tuple_value = 2,   #값을 하나만 입력할 경우 뒤에 ,를 붙여준다.
    ```
    > 인덱싱과 값을 추가하는것은 가능하지만 값 변경 및 삭제는 불가능하다.
    ```python
      tuple_value = 1, 2, 3, 4, 5
      print(tuple_value[1:4])       # 인덱싱 가능
      print(tuple_value + (6, 7)    # 추가 가능

      tuple_value[1] = 100          # 변경 불가능
      del tuple_value[1             # 삭제 불가능
    ```
    
**[⬆ back to top](#table-of-contents)**

### 딕셔너리와집합
  - 9.1 **딕셔너리**
    - 딕셔너리 관리
    > 키와 값의 쌍을 저장할 수 있고 {}로 만든다. 키는 중복이 안되고 변경도 안된다. 
    ```python
    dic = {"boy": "소년", "school": "학교", "book": "책"} 
    print(dic["boy"])                                           # 결과값:소년
    ```
    > 값은 변경가능하고 키를 삭제하면 밸류도 함께 삭제된다.
    ```
    dic = {"boy": "소년", "school": "학교", "book": "책"}
    dic["boy"] = "남자애"
    del dic['book'] 
    print(dic)
    ```
    > 키와 값을 가져올 수 있다.
    ```
    dic = {"boy": "소년", "school": "학교", "book": "책"} 
    print(dic.keys())     # 결과값 : dict_keys(['boy', 'school', 'book'])
    print(dic.values())   # 결과값 : dict_values(['소년', '학교', '책'])
    print(dic.items())    # 결과값 : dict_items([('boy', '소년'), ('school', '학교'), ('book', '책')])
    ```
    > 두개의 딕셔너리를 update()를 통해 병합할 수 있다.
    ```
    dic = {"boy": "소년", "school": "학교", "book": "책"} 
    dic2 = {"student": "학생", "teacher": "선생님", "book": "서적"} 
    dic.update(dic2)         # dic과 dic2의 키값이 같으면 dic2값이 적용되고 dic에 없는 키값은 추가된다.
    ```
    > 딕셔너리를 응용하여 알파벳 문자의 횟수를 셀 수 있다.
    ```
    song = """by the rivers of babylon, there we sat down yeah we wept, when we remember zion.
    when the wicked carried us away in captivity required from us a song
    new how shall we sing the lord's song in a strange land """
    
    alphabet = dic()
    for i in song:
        if i.isalphabet()==False:
            continue
        i = i.lower()
        if i in alphabet:
            alphabet[i] += 1
        else:
            alphabet[i] = 1
    ```
  - 9.2 **집합**
    - 집합
    > 집합은 키만 저장가능하고 수정가능하다. 딕셔너리와 같이 {}로 선언한다. 
    ```python
    asia = {"korea", "china", "japan"} 
    asia.add("vietnam")                               # 추가
    asia.remove("japan")                              # 삭제
    asia.update({'singapore', 'hongkong', 'korea'})   # 업데이트
    ```
    ```python
    | - 합집합(union)
    & - 교집합(intersection)
    - - 차집합(difference)
    ```
    
**[⬆ back to top](#table-of-contents)**

### 컬렉션관리
  - 10.1 **컬렉션관리 함수**
    - enumerate
    > 인덱스와 값을 한꺼번에 구해주는 내장함수이다.
    ```python
    score = [88, 95, 70, 100, 99]
    for no, i in enumerate(score,1):
        print(no, "번 학생의 성적 :", s)
    ```
  - 10.2 **람다 함수**
    - lambda
    > 함수를 선언할필요 없이 입력과 출력으로 정의된 축약방식이다.
    ```python
    score = [88, 95, 70, 100, 99]
    for i in filter(lambda x:x<90,score):
        print(i)
    ```
    ```python
    score = [88, 95, 70, 100, 99]
    for i in map(lambda x:x/2,score):
        print(i)
    ```
  - 10.3 **컬렉션의 사본**
    - 컬렉션의 사본
    > 리스트는 copy() 메서드를 활용해서 사본을 만들어야한다. 사용하지 않을경우 원본이 변한다.
    ```python
    list1 = [1, 2, 3] 
    list2 = list1.copy()
    list2[1] = 100 
    print(list1)             # 결과값 : [1, 2, 3]
    print(list2)             # 결과값 : [1, 100, 3]
    ```
    
**[⬆ back to top](#table-of-contents)**

### 표준모듈
  - 11.1 **시간**
    - 시간 조사
    > 현재 날짜와 시간을 알 수 있다.
    ```python
    import datetime
    now = datetime.datetime.now()
    print("%d년 %d월 %d일" % (now.year, now.month, now.day)) 
    print("%d:%d:%d" % (now.hour, now.minute, now.second))
    ```
  - 11.2 **난수**
    - 난수
    > random 모듈로 난수나 0에서 1미만의 실수를 생성할 수 있다.
    ```python
    import random 
    
    for i in range(5):
      print(random.random())
    for i in range(5): 
      print(random.randint(1, 10))
    ```
    
**[⬆ back to top](#table-of-contents)**

### 예외처리
  - 11.1 **예외 처리**
    - 예외 처리
    > 예외 종류에 따라 적절한 처리를 할 수 있다.
    ```python
    try:
      print(calcsum(10)) 
    except ValueError:
      print("입력값이 잘못되었습니다.")
    ```
    ```python
    str = "89" 
    try:
      score = int(str) 
      print(score)
      a = str[5]
    except ValueError:
      print("점수의 형식이 잘못되었습니다.")
    except IndexError:
      print("첨자의 범위를 벗어났습니다.")
    ```
    
**[⬆ back to top](#table-of-contents)**

### 파일
  - 12.1 **파일 입출력**
    - 파일 쓰기
    > 파일을 생서하고 내용을 저장할 수 있다. 마지막엔 꼭 close()를 해줘야한다.
    ```python
    file = open("live.txt", "w", encoding='UTF-8') 
    file.write("""
    삶이 그대를 속일지라도
    슬퍼하거나 노하지 말라!
    우울한 날들을 견디면 믿으라, 기쁨의 날이 오리니 
    """)
    file.close()
    ```
    - 파일 읽기
    > 생성된 파일을 읽어서 출력할 수 있다. 한줄만 읽고싶다면 readline()을 사용한다.
    ```python
    file = open("live.txt", "r") 
    text = file.read()
    print(text)
    file.close()
    ```
    - 파일 내용 추가
    > 생성된 파일의 내용을 추가할 수 있다.
    ```python
    file = open("live.txt", "a") 
    file.write("감사합니다.")
    file.close()
    ```
  
**[⬆ back to top](#table-of-contents)**

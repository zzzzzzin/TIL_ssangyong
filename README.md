# TIL_ssangyong
### 국비지원학원 수업 복습 기록 2023.12.29 ~ 2024.6.17

선생님 필기자료: http://192.168.10.30:8011/  
과제: http://pinnpublic.dothome.co.kr/
---

## 목차

[1일차_자료형, 변수](#자료형)  
[1일차_변수](#변수)  
[2일차_연산자_주의사항](#연산자_주의사항)  
[2일차_Escape_Sequence](#Escape_Sequence)  
[2일차_콘솔_입출력](#콘솔_입출력)  
[2일차_형식_문자_확장_기능](#형식 문자 확장 기능)  
[2일차_BufferedReader_클래스](#BufferedReader_클래스)  
[2일차_Error](#Error)  
[2일차_형_변환](#형_변환)  
---
### 자료형

클래스 : 코드의 집합. 자바의 기본적 단위.
메서드 : 코드의 집합. 메서드로 나뉨
*클래스와 메서드의 형태는 바뀔 수 없다.*

오류 주의: 대소문자, 문법, 세미콜론

ctrl + space : 코드 자동 완성
main + ctrl + space
perspective는 개발환경에 맞게

<mark>**모든 파일/폴더명의 규칙** </mark>
**'영어+숫자+_'만 사용 (한글 x)**
**숫자로 시작 금지 (1234 > _1234)**

프로젝트 하나 당 프로그램 하나
프로젝트 간의 연관성은 없음
프로젝트 내의 빨간 엑스표시 제거가 최우선 순위

새로운 언어 > 자료형 (가장 우선순위)

**자바의 자료형(Data type)**
자료형 : 데이터(자료)의 형태. 데이터의 길이(범위)와 생김새를 미리 정의하고, 이 정의에 따라 분류해 놓은 규칙

자바의 자료형의 기준 2가지
1. 형태
2. 
3. 길이
  
자료형 분류

1. 기본형 = 원시형(Primitive Type) = 값형(Value Type)
  
  - 8가지 (byte, short, int, long, float, double, char, boolean) <mark>암기</mark>
    
    - 숫자형
      
      1. 정수형
        
        a. byte : 1byte = 8bit > 2^8 = -128~127
        
        b. short : 2byte = 16bit > 2^16 =
        
        약-32000~32000
        
        c. int : 4byte = 32bit > 2^32 = 약-21억~21억 (대부분 int)
        
        d. long : 8byte = 64bit > 2^64 = 약-922경~922경
        
      2. 실수형
        
        a. float : 4byte (무한에 가깝).
        
        - 지수(8bit) + 가수(23bit)
          
        - 소수점 이하 6-7자리를 유효하게 표현
          
        - 단정도형
          
        
        b. double : 8byte (무한에 가깝)
        
        - 지수(11bit) + 가수(52bit)
          
        - 소수점 이하 15-16자리를 유효하게 표현
          
        - 배정도형
          
        
        고정소수점 방식 : ex) 12.345
        
        부동소수점 방식 : ex) 1.23x2e-1
        
        부동소수점의 단점 : 0이 연속이 아닐 때 손실분이 생김
        
        *수의 범위보다 훨씬 더 정밀한 숫자를 저장할 수 있는 것이 중요*
        
    - 문자형 (컴퓨터는 숫자로 이해)
      
      1. 문자형
        
        a. char : 2byte (숫자형 중, 정수형) > 0~65535 (음수 없음. 부호 비트 없음)
        
        ASCII (아스키 코드) > Unicode(유니코드) - 16bit
        
        A = 65
        
    - 논리형
      
      1. 논리형
        
        a. boolean : 참, 거짓 판별(true, false)
        
        8bit : 0과 1만으로 표현가능해서 1bit로도 가능하지만 자바는 최소한 8bit를 사용해야함
        
        00000000(참),00000001(거짓)
        
2. 참조형(Reference Type) *종류가 나뉘지 않음*
  
  - class, Array(배열), Enum(열거형), Interface
    
  - class는 사용자가 정의 가능
    

bit : 0 또는 1이 들어가는 공간
최소한 8bit(1=byte)를 사용해야 함
자바는 메모리에 할당받을 수 있는 것은 1byte (무조건 byte로 할당받음)
자바의 맨 앞의 데이터가 0이면 양수, 1이면 음수
부호비트(맨 앞) + 데이터 비트
최솟값과 최대값: '-128~127' (0을 양수에 포함시킴)

---
### 변수
자료형 + 변수
변수 (variable) : 개발자가 명령어로 메모리에 할당받은 공간
각 bit마다 물리적인 주소 > 메모리 번지(주소)
- 주소는 연속적으로 존재하기 때문에 가장 첫번째 메모리의 주소만으로 찾을 수 있다. 첫 메모리의 크기는 4byte. > 물리적 주소는 정확히 알기 어려움 > 주소대신 별칭을 사용 > 그 때의 별칭이 변수이자 공간
  
1. 변수 생성하기
  - 자료형 변수명; ex) '''int kor;''' > 정수 4byte 만큼 저장
2. 변수 초기화
  - 변수명 = 값;  
  ```java
  kor = 100;
  ```  
  - 대입 연산자 or 오른쪽 값을 왼쪽에 할당
3. 변수 사용하기
4. - 출력, 연산, 조건, 기록 등
   - 변수명
    

Q. 학생 1명의 영어점수를 저장한 후 화면에 다시 출력하시오

1. 데이터 성질 파악 > 영어 점수
    - 형태 > 정수/실수 > 정수
    - 길이 > 0~100
    
2. 1의 결과에 따라 적당한 자료형 선택
 - byte 선택

3. 2의 결과 자료형으로 변수 생성하기

```java
public class Ex01_DataType {
    public static void main(String[] args) {
        byte eng;
        eng = 90;
        System.out.println(eng)    
        }
}
```
```java
- byte eng;
  eng = 90;
  System.out.println(eng);
  
  // 변수 (값) 수정하기
  eng = 95; // 덮어쓰기
  System.out.println(eng);
```
  
상수 : 표현이 같고 결과값이 같다 vs 변수 : 표현은 같지만 결과값이 다름
> 변수는 데이터를 갖고 있는 공간의 대상
> *의미부여 + 값을 변화시킬 수 있음*

#### 변수명 만들 때 규칙

1. 영문자 + 숫자 + __ 만 사용 *(관습)*
2. 숫자로 시작 불가능
3. 키워드 사용 불가능
4. <mark>의미있게</mark>
5. 동일한 이름의 변수 생성 불가능

```java
byte kor1;     //byte kor(); error   
byte _1kor;    //byte 1kor; error
                //byte byte; error
```

##### 변수 선언하는 방식

- 선언 > 선언 직후 > 비어있는 상태 > null
  
  ```java
  int n1;       // null
  n1 = 100;     // 초기화
  int n2 =200;  // 선언 + 초기화
  int n3, n4;    // n5, n6 모두 int 자료형
  int n5 =10, n6 = 12; // 다른 값도 같이 가능
  ```
  
- 지도 좌표
  
```java
double x1;    // 우리집 x좌표
double y1;    // 우리집 y좌표

double x2, y2; // 친구집 x좌표, 친구집 y좌표
*주석은 프로그래밍 사이에 작성 불가능. 작성하면 주석 뒤의 코드가 주석처리 됨*

double x3,    // 마트 x좌표
       y3;    // 마트 y좌표

// 학교 x좌표
double x4;
// 학교 y좌표
double y4;
```

- **주의할 점**

```java
int m;                    //The local variable m may not have been initrialized
System.out.println(m);
//error : m에 값이 할당이 안 됨
//변수는 값을 가지고 있지 않은 상태에서는 어느 용도로든 사용이 불가능(출력x, 연산x, 사용금지)
//변수는 반드시 초기화를 해야 함

int m;
m=5;
System.out.println(m);
```

**error 메세지 잘 보는 사람이 빠르게 성장 > <mark> error 메세지 꼭 정리</mark>**

- 식별자또는 변수이외의 다른 요소 명명법(패턴)
  
  1. 헝가리언 표기법
    - 식별자의 접두어로 자료형을 표기 (자료형을 기억하기 번거롭)
  2. 파스칼 표기법
    - 식별자의 첫문자를 대문자로 + 나머지를 소문자로 표기 / 주로 2개 이상의 단어
    - (**클래스명은 반드시 대문자로 시작**)
  3. 캐멀 표기법
    - 각 단어의 첫 문자를 대문자로 표기 (주로 변수명)
  4. 스네이크 표기법
    - 전부 소문자 / 합성어일때 각 단어를 _로 연결
  5. 케밥 표기법
    - 전부 소문자 / 합성어일때 각 단어 -로 연결 (java는 -불가능)
  
  ```java
  1. int intAge;    // 요즘은 잘 안 씀(변수 위에 마우스를 올리면 자료형 뜸)
  2. int EnglishScore;    // 주로 자바의 class명에 사용
  3. int mathScore;            // 주로 변수명에 사용
  4. int english_score    // 스네이크는 자유롭게 사용
  5. int english-score    // html, css에서 사용
  ```
  
  **정리**
  
  클래스명 : 파스칼 표기법
  변수명 : 캐멀 표기법
  
  **데이터 중 일부는 값을 변화시키면 안되는 값 존재**
  

```java
double pi = 3.14;
pi = 3.55;    // error 안 남 (pi의 값은 바뀌면 안 됨) 

// 변수 내의 수정 불가능을 위해 final 변수 사용
final double pi = 3.14;    // final 변수 : 상수 (constant)

// pi = 상수
// 3.14 = 데이터 상수 > 리터럴(literal)

//상수는 모두 대문자로 생성 (변수와 구분을 위해)
final double PI = 3.14;
```

#### 모든 자료형 + 변수 생성하기

- 정수
  
  ```java
  byte b1;
  b1 = 100;
  System.out.println(b1);
  ```

  ```java
// b1 = 128 or b1 = - 129 Type mismatch:

b1 = Byte.MAX_VALUE; // 상수(MAX_VALUE), 
System.out.println(b1);

b1 = Byte.MIN_VALUE; // 상수(MIN_VALUE)
System.out.println(b1);
```

```java
short s1;
s1 = 100;
System.out.println(s1);

s1 = 128;
System.out.println(s1);

s1 = Short.MAX_VALUE;
System.out.println(s1);
````

```java
int n1;
n1= Integer.MAX_VALUE;
System.out.println(n1);
```

**숫자 셀 때 10,000이 아니라 10_000을 사용**

```java
long l1;
l1=3_000_000_000
System.out.println(l1)    //error 이유 : 오른쪽이 interger라 LValue != RValue

l1=3_000_000_000L


// 모든 상수도 자료형을 가짐
b1 = 100; // byte = int 논리적으론 에러지만 내부적으로 작동하게 만듦
s1 = 100; // short = int 
n1 = 100; // int = int 
l1 = 100; // long = int 
l1 = 100L; // long = long // 처음부터 RValue의 할당 공간을 8칸으로 잡기

System.out.println(100); // 100의 자료형이 뭔지? integer
// 결과: 
// int n1 = 100; > int n1, n1=100, 100 (100부터 메모리 할당공간 필요) > java 정수타입에 상수가 나오면 integer로 취급 > 이름없는 공간 > 변수명 선언 및 초기화 > 할당 > 실제로는 두개가 생성됨 > 후에 java가 임의로 삭제함
```

**중요**

1. LValue 와 RValue는 반드시 자료형이 동일해야 함
  - 왼쪽 (변수) = 오른쪽 (상수);
  - LValue = RValue;
2. 모든 상수들도 자료형을 가진다.
  - <mark>정수형 상수는 int 타입</mark> (4byte로 처리)
  - 운영 체제가 한번에 처리하는 데이터의 양이 int가 됨
  
- 실수
  
  **<mark>실수형 상수는 double 형</mark>**
  
  - 단정도형
    
    ```java
    float f1;
    f1 = 3.14F;        
    // f1 = 3.14;가 error인 이유: 실수는 기본적으로 double타입으로 처리하기 때문에 float타입 변수 
    값의 수 마지막에 f나 F를 적어야 함
    System.out.println(f1);
    ```
    
  - 배정도형
      
     ```java
     double d1;
     d1 = 6.28;
     System.out.println(d1);    // 변수 값 뒤에 d나 D를 적지 않아도 error 없음
     ```
      
    - 단정도형과 배정도형의 차이점
      
      ```java
      f1 =123.1234567890123456789012345678901234567890F;
      d1 =123.1234567890123456789012345678901234567890D;
      System.out.println(f1);
      System.out.println(d1);
      ```
      
    
    System.out.println(Float.MAX_VALUE);
    System.out.println(Double.MAX_VALUE);
    
    // 결과값: 3.14 / 6.28 / 123.12346 / 123.12345678901235
    
    double d2 = 0.2;
    double d3 = 0.1;
    System.out.println(d2+d3); // error: 결과값이 0.30000000000000004
    
    > 정수로 만들어주기 위해 10의 배수를 곱 > 계산 > 다시 10배수로 나눠줌
    
    
    - 문자형
    ```java
    char c1;
    c1 = 'A'; // error: 대입할건지 식별자인지 컴파일러가 구분 못 함 > 홑따옴표 사용으로 해결
                                                                (문자형 상수, 리터럴)
    System.out.println(c1);                            *리터럴: 읽는 그대로 의미가 있는 상수
    
    c1 = '1'; // 문자형 1임 (숫자형 1 아님)
    System.out.println(c1);
    
    // 결과값: A / 1(문자형 1)
    
    c1 = '홍길동'; 
    System.out.println(c1) ;
    // error: char는 문자 하나만 인식하기 때문 > String 사용으로 해결
    ````
    
- 논리형
  참(0)과 거짓(1) 판별
  
  ```java
  boolean flag;
  flag = true; // 논리형 상수 (리터럴)
  System.out.print(flag);        // 결과값: 1
  ```
  
  flag = false; // 논리형 상수 (리터럴)
  System.out.print(flag); // 결과값: 0
  
  /*
   미리 알아둬야 할 참조형
  
  - String(문자열): 문자들이 열을 지은 형태/문자 집합/char 여러개 모은 자료형
    char name = '홍길동''
    char name = '홍''
    char name = '길''
    char name = '동''
    error: char는 문자 하나만 인식 하기 때문 > String으로 문자열 인식 가능
    */
    
    ```java
    String name;
    name = "홍길동"; // 문자열 상수 (리터럴)
    System.out.println(name);
    // 결과값: 홍길동
    
    char m1 = 'A';
    String m2 = "A";
    System.out.println(m1);
    System.out.println(m2);
    // 결과값: A / A
    
    String m3 = ""; // 0개의 문자열 = 빈문자열(Empty String) : 문자열 변수를 초기화할 때 사용
    ```
    
- 값형 vs 참조형
  
  - 둘을 나눈 이유 : 논리적인 차이 (메모리에 생성되는 규칙이 다름)
    
    - 스택 Stack
      
      - 정적으로 메모리에 할당됨
        
      - 스택 영역에 있는 변수들은 선언된 함수을 빠져나가면 소멸됨
        
        (블록을 닿는 괄호를 만나면 소멸됨)
        
      - FILO(First In Last Out) 또는 LIFO(Last In First Out) 구조
        
        스택 영역에 처음 생성된 변수는 마지막에 소멸, 마지막에 생성된 변수는 처음으로 소멸됨
        
    - 힙 Heap
      
      - 동적으로 메모리에 할당됨
        
      - 프로그래머가 원하는 시점에 동적으로 메모리를 할당하는데, 바로이러한 유형의 변수들이 할당되는 영역
        
      - CLR의 가비지 컬렉터가 힙 영역에 사용되지 않는 데이터 소멸시킴
        
    - 스택과 값형
      
      - 값 형식은 스택 메모리 공간에 데이터가 생성이 되며 값을 직접적으로 가지고 있음. {를 만나 데이터 순차적 생성, }를 만나 순차적 소멸
        
        ```java
        {                    // 1. 블록 시작
            int a = 100;    // 2. 변수 a 선언 및 초기화
            int b = 200;    // 3. 변수 b 선언 및 초기화
         }                    // 4. 블록 종료
        ```
        
        1. 블록 시작: 스택 영역에 아무것도 존재 x
          
        2. 변수 a 선언 및 초기화: int a=100; 실행되며 변수 a가 스택 영역에 쌓임
          
        3. 변수 b 선언 및 초기화 : int b=200; 실행되며 변수 b가 a위에 쌓임
          
        4. 블록 종료: }를 만나 {}사이의 변수 소멸
          
          1. 스택은 마지막에 들어온 변수가 제일 먼저 소멸 > b 소멸
          2. 변수 b 전에 들어온 변수 a가 다음으로 소멸
          3. 변수 a,b가 모두 소멸된 스택의 메모리 공간
       
      - 힙과 참조 형
        
        - 참조 형식은 힙 영역에 데이터가 저장되고 스택 영역에서 데이터가 저장된 힙 영역의 메모리 주소 저장.
          
          스택 영역에 실제로 값을 가지고 있지 않고 힙 영역의 데이터를 참조하고 있음
          
        
        ```java
        {                        // 블록시작        
            object a = 100;    // 변수 a 생성 및 초기화
            object b = 200;    // 변수 b 생성 및 초기화
        }                        // 블록 종료
        ```
        
        1. 블록 시작
          
          브록 시작 시점에는 스택 영역과 힙 영역에는 아무것도 존재하지 않음
          
        2. 변수 a 생성 및 초기화
          
        - object는 참조 형식으로 변수 a는 스택 영역에 생성되고 변수 a의 실제 값인 100은 힙영역에 생성됨. 스택 영역에 생성된 변수 a는 힙 영역에
          생성된 100의 주소값인 1000을 가지고 있음. 변수 a는 주소값 1000으로 힙 영역에 접근하게 됨
          
        3. 변수 b 생성 및 초기화
          
          스택영역에 생성된 변수 b는 힙 영역에 생성된 200의 주소값을 지님
          
        4. 블록 종료
          
          }를 만나 {}사이의 변수 모두 소멸
          
          스택 영역에서 변수가 소멸됐지만, 힙 영역의 가비지 콜렉터가 소거하므로 아직 소멸 x
          
  - 값형과 참조형의 주요 차이점
    
    - 값 유형은 스택 메모리에 저장되고 참조 유형은 힙 메모리에 저장됨
      (참조형은 스택 메모리의 데이터의 주소값이 힙 메모리 존재 > 스택 메모리의 주소값을 참조) 
    - 구조체, 문자열, 열거형을 제외한 모든 기본 데이터 유형은 값형의 예시
      
    - 값형이 다른 값형에 복사되면 실제 값은 복사되지만 참조형이 다른 참조형에 복사되면 값의 참조 주소는 복사
      
    - 값형은 0으로 초기화하고 참조형은 null로 초기화 가능      
    - 값형 null 불가능 (변수 속의 값이 반드시 존재해야 함)
    
---
### 연산자 주의사항
```java
//연산자
int a = 10;
int b =  20;
System.out.println(a+b);  //결과: 
```
 +는 이항연산자: 피연산자가 2개 필요(윗 코드:a,b)
 컴퓨터는 피연산자가 숫자면 연산, 문자면 연결
 연산자 우선순위(수학의 연산자 우선순위와 비슷)
 연산자 방향: 왼쪽부터 연산
```java
//연산자 우선순위
System.out.println(a + "+" + b + "=" + a + b);   //결과: 
System.out.println(a + "+" + b + "=" + (a + b)); //결과:
```
```java
//주민번호 입출력
int jumin1 = 950105;  
System.out.println("주민번호: "+ jumin1);  //결과: 
  
int jumin2 = 030711; // error: 8진수로 인식  
System.out.println("주민번호: "+ jumin2);  //결과:
```
```java
//진법별로 10을 작성
System.out.println(10); 	//10진수
System.out.println(010);	//8진수
System.out.println(0x10);	//16진수
System.out.println(0b10);	//2진수
```
```java
// 실수 리터럴 표기법
double d1 = 1200;
double d2 = 1.2e+3;

System.out.println(d1); //결과:
System.out.println(d2);	//결과:
	
d1 = 0.012;
d2 = 1.2e-2;

System.out.println(d1);	//결과:
System.out.println(d2);	//결과:
```	
---
### Escape Sequence
특수 문자가 아닌 Escape Sequence로 표현할 것
컴파일러가 번역할 때, 소스의 문자를 그대로 출력x, 미리 약속된 표현으로 바꿔서 출력하는 요소

1.\n
new line, line feed (개행 문자, 엔터)
컴파일러는 한 글자로 인식
```java
char c1 = '\n'; //결과: 
//\n은 한 글자임으로 char로 써도 error 안남
```
```java	
// 요구사항] "안녕하세요. 홍길동입니다." 출력
String msg = "안녕하세요. 홍길동입니다";
System.out.println(msg);

//수정사항] "안녕하세요"와 "홍길동입니다."를 다른 줄에 출력 (중간에 엔터)
> String msg ="안녕하세요." 
>             "홍길동입니다"
System.out.println(msg);
//error: 문자열 리터럴내에는 엔터 작성 불가능 > 반드시 한줄로 > \n을 사용

//올바른 작성법
String msg2 = "안녕하세요. \n홍길동입니다";
System.out.println(msg2);
// 결과: 안녕하세요.
//       홍길동입니다.
		
//빈줄입력
System.out.println();
```
		
2.\r
carriage rerutn
캐럿(문자를 넣는 곳)의 위치를 현재 라인의 맨 앞으로 이동
키보드의 Home키 역할
msg = "안녕하세요. \r홍길동입니다";
```java
System.out.println(msg);
// 결과: 홍길동세요 > 이클립스는 제대로 이해못해서 엔터 역할
```
- 운영체제의 엔터
윈도우 > \r\n
맥OS > \r
리눅스 > \n
```java
System.out.println("하나\r\n둘");	//정석 (권장)
System.out.println("하나\n둘");	    //잘 사용
```
3.\t
탭문자, tab > 현재 위치에서 가장 가까운 tab으로 이동 > 열맞춤 목적
가독성을 위해 \t 사용 (탭 몇번했는지 알기 쉽게)
```java
msg = "하나	둘		셋";
System.out.println(msg); 
//결과: 
		
msg = "하나\t둘\t\t셋";
System.out.println(msg);
//결과:
```		
4.\b
backspace > 커서를 앞으로 옮김
```java
msg="홍길동\b입니다.";
System.out.println(msg);	//특수문자 나옴 > 이클립스는 \b 실행 불가능
// 정상 결과값: 홍길입니다.
```			
5.\ ", \ ', \ \ (사이의 띄어쓰기는 제거 후 작성)
이미 역할이 있는 문자를 역할이 없게 만드는 작업
```java
//요구사항] 화면에 '홍길동:"안녕하세요"' 출력
msg = "홍길동: \"안녕하세요.\"";	//컴파일러는 "을 문자열인지 출력내용인지 구분 불가능
System.out.println(msg);
```
```java		
//요구사항] 수업 폴더의 경로 출력
//C:\class\code\java
System.out.println("C:\class\code\java");
Invalid escape sequence
valid ones > \b  \t  \n  \f  \r  \"  \'  \\
System.out.println("C:\\class\\code\\java");
```		
---
### 콘솔 입출력, Console Input Output(IO)
 >기본 입력 장치: 키보드
 기본 출력 장치: 모니터
		 
- 콘솔 출력
클래스(System).필드(out).메서드(println)(값(인자));
  1. System.out.println(값);
      -println 메서드
	   -print line > 값을 행 단위로 출력 > 값을 출력한 뒤 엔터
	2.  System.out.print(값);
	-print 메서드	> 값을 출력하고 엔터를 안 침
	3. System.out.printf(값);
		   - printf 메서드
		   - print format > 출력 형식을 제공
		   - String.format() 메서드와 동일
      ```java
      //성적표 출력하기
      System.out.println(100); 
      System.out.println(200); 
      System.out.println(300); 

      System.out.print(100); 
      System.out.print(200); 
      System.out.print(300); 
		
      String name1="홍길동";
      int kor1 = 100;
      int eng1 = 90;
      int math1 = 90;

      String name2="아무개";
      int kor2 = 95;
      int eng2 = 98;
      int math2 = 87;
      System.out.println();

      //위 성적표를 좀 더 보기좋게 열 맞추기
      System.out.println("====================="); 
      System.out.println("	성적표"); 
      System.out.println("====================="); 
      System.out.println("[이름]\t[국어]\t[영어]\t[수학]"); 
      System.out.println("-------------------------");

      //\r, \t 사용
      System.out.println(name1);
      System.out.println("\t");
      System.out.println(kor1 + "\t");
      System.out.println(eng1 + "\t");
      System.out.println(math1 + "\r\t");

      System.out.println(name2 + "\t" + kor2 + "\t" + eng2 + "\t"+ math2);

      //뭘 쓴건지 모르겠듬... 확인 필요	
      System.out.println();
      System.out.println();
      System.out.println();
``` ```

printf()
형식 문자 (PlaceHolder) 제공
가독성 향상(***)\
>%s > String
%d > Decimal(정수) > byte, short, int, long
%f > Float(실수) > float, double
%c > Char
%b > Boolean
```java
//요구사항] "안녕하세요. 홍길동님" 문장 출력
String name = "홍길동"; 
System.out.println("안녕하세요. 홍길동님");

//name 변수에 사용자가 키보드로 입력한 이름
System.out.println("안녕하세요. "+name+"님");	// 배웠던 걸로 활용
System.out.printf("안녕하세요. %s님", name);	// printf() 활용
		
System.out.println("\n");

//요구사항 "안녕하세요. 홍길동님. 안녕히가세요. 홍길동님"
System.out.println("안녕하세요 "+name+"님. 안녕히가세요 "+name+"님.");
System.out.printf("안녕하세요 %s님. 안녕히가세요 %s님.", name,name);	//printf()
System.out.println("\n");
		
System.out.printf("문자열: %s\n", "문자열");
System.out.printf("정수: %d\n", 100);
System.out.printf("실수: %f\n", 3.14);
System.out.printf("문자: %c\n", 'A');
System.out.printf("논리: %b\n", true);
System.out.println("\n");
```
- 콘솔 입력  
  입력 - 콘솔 입력 한번 더 읽기  
  
1. System.in.read()  
-1문자만 입력 가능 (1byte씩 읽기)  
-문자 코드값을 반환  
-한글 입력 불가능 (2byte 문자 미지원, ASCII 문자만 지원)   

2. BufferedReade 클래스  
  
3. Scanner 클래스 
 ```java
//요구사항] 사용자에게 문자 1개를 입력 > 입력값을 화면에 출력  
//1. 라벨 출력  
//2. 문자 입력  
//3. 문자를 화면에 출력  
  
System.out.print("문자 입력: ");  
  
//사용자로부터 키보드 입력을 받아 입력한 문자를 돌려준다.  
//현재 상태: 사용자의 키 입력을 대기 > 블럭 걸렸다  
//사용자 입력(엔터까지) 후, 대기 상태 해제  
int code = System.in.read(); //키보드로 입력한 값을 읽음으로 System.in.read()의 역할 끝  
//a입력 > int code = a  
  
System.out.println("출력: " +code);  
System.out.printf("출력: %d\n",code);  
System.out.printf("출력: %c\n",code); //입력한 문자 한개를 그대로 출력  
  
code = System.in.read(); //위 코드와 합쳐 총 2문자 읽음 가능  
  
System.out.printf("출력: %d\n",code);  
System.out.printf("출력: %c\n",code);  
// 여기서 문자 1개만 입력 > 이상함(중간에 빈 곳이 있음)  
// 이유: 키보드에서 입력한 값은 버퍼에 저장되고 read를 만나는 순간 프로그램이 입력값을 연산하고 입력된 값은 삭제됨  
// 엔터까지 버퍼로 저장됨. 엔터는 \t\n. \t는 13, \n은 10		
```
---
### 형식 문자 확장 기능
1. %숫자d, %숫자s, %숫자f, %숫자c, %숫자b
숫자는 정수만 가능
출력할 내용의 너비 지정 (내용물과 상관없이 너비 확보)
탭문자처럼 열을 맞추기 위한 기능
숫자가 양수면 우측 정렬, 음수는 좌측 정렬
```java
int num =123;
System.out.printf("[%d]\n", num);
System.out.printf("[%10d]\n", num);
System.out.printf("[%-10d]\n", num);
System.out.println();
```
		
2. %.숫자f
		소수점 이하 자릿수 지정
   ```java		
	   	double num2 = 3.14;
		
		System.out.println(num2);
		System.out.printf("%f\n", num2);
		System.out.printf("%.2f\n", num2);
		System.out.printf("%.1f\n", num2);
		System.out.printf("%.0f\n", num2);
		System.out.printf("%.3f\n", 3.4567);//3.456아니라 3.457임 > 항상 확인 후 작업
		System.out.println();
```	```

3. %,d와 %,f
   자릿수 표기(천단위)

   ```java
   int price = 1234567;
   System.out.printf("금액: %d원\n", price);
   System.out.printf("금액: %,d원\n", price);
		
		
	//천단위 + 소수이하 + 출력너비
	//요구사항] 천단위 + 소수이하 둘째자리 + 출력너비 20자리에 우측정력
	 double num3 = 1234567.7890123; 
	 
	 System.out.printf("[%f]\n", num3);
	 System.out.printf("[%,f]\n", num3);
	 //System.out.printf("[%,.f]\n", num3); error: 소숫점 자리수를 지정하지 않음
	 System.out.printf("[%,.2f]\n", num3);
	 System.out.printf("[%,20.2f]\n", num3);
	 //[Obsolete Methods on the Stack] contains obsolete methods > 디버그 모드 해제하면 해결
		 
		
	//메뉴판 출력 > 열 정렬 > 탭 문자 + %10d 혼합
	System.out.println("=========================");
	System.out.println("음료 가격");
	System.out.println("=========================");
	System.out.printf("콜라: %d\n", 2500);
	System.out.printf("스무디: %d\n", 3500);
	System.out.printf("사이다: %d\n", 500);
	System.out.printf("아메리카노: %d\n", 15000);
	
	//가독성 좋게 변경 > 열 맞춤 + 너비(가격) 맞춤
	System.out.println("=========================");
	System.out.println("\t음료 가격 (단위:원)");			//단위 반드시 존재해야 함
	System.out.println("=========================");
	System.out.printf("콜라: \t\t%,6d\n", 2500);
	System.out.printf("스무디: \t\t%,6d\n", 3500);
	System.out.printf("사이다: \t\t%,6d\n", 500);
	System.out.printf("아메리카노: \t%,6d\n", 15000);
	```
	---
	### BufferedReader 클래스
	1. 유니코드 입력 가능(한글 입력 가능)
	2. 문장을 입력 가능

>BufferedReader를 사용하기 위해서는 도구 선언 필요> 클래스를 import
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.*; > *(와일드카드_모든 클래스) 이것도 가능
ctrl + shift + o > 도구 선언 단축키
       
   ```java
	//기본 문법
	BufferedReader reader = new BufferedReader (new InputStreamReader(System.in)); 
	//자료형,class   변수
	
	// 요구사항] 사용자로부터 문자 1개를 입력받아 화면에 출력	
    System.out.print("입력: ");  
    int code = reader.read();  
    System.out.println(code);
	
	//콘솔로부터 키보드 값을 입력받을 수 있는 도구  
    System.in.read  

	System.out.print("문자 입력: ");  
   
	int code = reader.read();  
   
	System.out.println(code);  
	System.out.printf("%c\n",code);  
```
		
>암기해야 함
A(65) ~ Z(90)
a(97) ~ z(122)
0(48) ~ 9(57)
숫자 1은 0000_0001, 문자 1은 0011_0001
\r(13)
\n(10)
스페이스(32)
탭(9)
한글 완성형 > 가 ~ 힣

- JDK,JRE 차이점
 JDK = JRE + Java Development Tools > 프로그램 개발
 JRE (Java Runtime Environment) > 프로그램 실행
 Java Development Tools > 프로그램 생성
run하면 기존 프로그램에 덮어서 새로운 프로그램이 실행됨 > 메모리 차지
 콘솔창 우측 상단의 x버튼 > 빨간ㅁ버튼 >>

  ```java		
  //이름 입력 (여러글자 가능)
  System.out.println("이름: ");
  String name = reader.readLine();	//입력된 라인 전체를 읽기
  System.out.printf("안녕. %s\n", name);

  //나이 입력
  System.out.println("나이: ");
  String age = reader.readLine();	//자료형 int 불가능 > readLine()은 문자열로 고정되어 있기 때문
  								//이때의 나이값(숫자)는 숫자가 아닌 '숫자'인 문자열
  System.out.printf("%s님의 나이는 %s살입니다.\n", name, age);
		
  //요구사항] 사용자로부터 2개의 숫자를 입력받아 두 수를 더하시오
  System.out.print("첫번째 숫자: ");
  String input1 = reader.readLine();
		
  System.out.print("두번째 숫자: ");
  String input2 = reader.readLine();
		
  System.out.printf(input1 +"\n"+ input2);		//위의 이름,나이 입력 후에 숫자를 입력하는 과정 필요 > 위에것을 주석하면 해결
  System.out.println("\n");
  ```
- 문자열 > (변환) > 숫자
Integer.parseInt()
Byte.parseByte()
Short.parseShort()
Long.parseLong()
Float.parseFloat()
Double.parseDouble()
Boolean.parseBoolean()

- 자바는 모든 입력 값을 문자열
 
 ```java  
 int num1 = Integer.parseInt(input1);	//문자열>숫자  
 int num2 = Integer.parseInt(input2);	//문자열>숫자  
 System.out.println(num1 + num2);		//위의 이름,나이 입력 후에 숫자를 입력하는 과정 필요 > 위에것을 주석하면 해결  
```

```java
//실수
double num1 = Double.parseDouble(input1);
double num2 = Double.parseDouble(input2);
System.out.println(num1 + num2);
```
---
### Error
```java
int a = 10;                        //사용자 입력한 숫자라고 가정 > 10대신 0이 들어가면 오류
System.out.println(100/a);
//단, 정수/정수일 때 재수가 0이 될 수 없음
```	
에러, Error 
: 오류, 버그(Bug), 예외(Exception) 등
			
	1. 컴파일 에러
				- 컴파일 작업 중에 발생하는 에러
				- 컴파일러가 번역하다가 에러 발견 > 문법이 틀려서
				- 에러 발생 > 컴파일 작업 중단 > 프로그램 생성 불가
				- 반드시 해결해야 함 
				- 난이도 가장 낮음 > 컴파일러가 알려줌 > 에러
				- 대부분 오타 > 이클립스의 빨간 밑줄
				
	2. 런타인 에러
				- 런타임 > 실행중
				- 컴파일 작업 중에는 없었는데, 실행 중에 발생하는 에러
				- 문법에는 오류 없음, 다른 원인으로 발생하는 에러
				- 예외 (Exception)
				- 난이도 중간 > 발견 여부 랜덤
			
	3. 논리 에러
				- 컴파일 성공 + 실행 성공 but, 결과 이상함
				- 발견이 매우 어려움 > 애초에 안 내려고 노력하기
---
### ==형 변환==
-Promotion, Casting
-하나의 자료형을 다른 자료형으로 변환하는 작업
-코드 작성을 유연하게
-boolean 제외
-int > double
-float > short
   1. 암시적 형 변환(자동 형 변환), Promotion
				- 큰 형 = 작은 형
				- 100% 안전 > 생략 가능
			
	2. 명시적 형 변환(강제 형 변환), Casting
				- 작은 형 = 큰 형 
				- 경우에 따라 다름
- 형 변환 방법
-`(변환할 자료형)변환할 변수명;`
-*==LValue자료형 = RValue 자료형==*
```java
//short = Byte
//s1 = b1;
//Short = Short 
byte b1;
b1 =10;
short s1;

s1 = (short)b1;  //에러 아닌 이유: short에 short를 넣음

s1 = b1;
System.out.println(s1);
---
byte b2;
short s2;

s2 = 128; //원본

//Byte(1) = Short(2)
//작은형 = 큰형		
//b2 = s2		     //error> 형변환 필요

b2 = (byte)s2;	//큰 형의 값이 작은 형의 값보다 클 때는 무조건 형변환 작성
```
```java
//기업 은행 계좌
int m1;
long m2 = 300000000L;
		
//계좌 이체 > m2 돈을 m1으로
m1 = (int)m2;
System.out.printf("계좌이체 결과: %,d원\n", m1);
```
>큰형 = 작은형
			- long = int
			- long = short
			- long = byte
			- int = short
			- int = byte
			- short = byte
			작은형 = 큰형
			 - byte = long
			 - byte = short
			 - byte = int
			 - short = long
			 - short = int
			 - int = long

- 정수형 리터럴은 int, 실수형 리터럴은 double
byte = int
작은형(1) = 큰형(4)
명시적 형변환
   ```java
  byte  a1  = 10;	//명시적 형변환
  short a2  = 10;	//명시적 형변환
  int   a3  = 10;	//명시적 형변환
  long  a4  = 10;	//암시적 형변환(생략 가능)
```	```	
- 작은형(4) = 큰형(8)
명시적 형변환
   ```java
   loat f1 = 3.14F;
   float f2 = (float)3.14;
	
  double d1 = 3.14F;
``` `

`정수 > 정수 실수 > 실수 실수 > 정수 정수 > 실수`

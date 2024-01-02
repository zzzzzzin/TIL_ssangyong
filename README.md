# TIL_ssangyong
국비지원학원 수업 복습 기록 2023.12.29 ~ 2024.6.17
Ex02_Variable

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
  
2. 길이
  

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

- byte eng;
  
  eng = 90;
  
  System.out.println(eng);
  
- 변수 (값) 수정하기
  
  eng = 95; 덮어쓰기
  

상수 : 표현이 같고 결과값이 같다 vs 변수 : 표현은 같지만 결과값이 다름

> 변수는 데이터를 갖고 있는 공간의 대상
> 
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

- 주의할 점

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

---

## Ex

#### 모든 자료형 + 변수 생성하기

- 정수
  
  ```java
  byte b1;
  b1 = 100;
  System.out.println(b1);
  ```
  

// b1 = 128 or b1 = - 129 Type mismatch:

b1 = Byte.MAX_VALUE; // 상수(MAX_VALUE), 
System.out.println(b1);

b1 = Byte.MIN_VALUE; // 상수(MIN_VALUE)
System.out.println(b1);

````
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
    
    ````
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
      
      - 값 형식은 스택 메모리 공간에 데이터가 생성이 되며 값을 직접적으로 가지고 있음. {를 만나 데이터 순차적 생성, }를 만나 순차적소멸
        
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
          
          object는 참조 형식으로 변수 a는 스택 영역에 생성되고 변수 a의 실제 값인 100은 힙영역에 생성됨. 스택 영역에 생성된 변수 a는 힙 영역에 생성된 100의 주소값인 1000을 가지고 있음. 변수 a는 주소값 1000으로 힙 영역에 접근하게 됨
          
        3. 변수 b 생성 및 초기화
          
          스택영역에 생성된 변수 b는 힙 영역에 생성된 200의 주소값을 지님
          
        4. 블록 종료
          
          }를 만나 {}사이의 변수 모두 소멸
          
          스택 영역에서 변수가 소멸됐지만, 힙 영역의 가비지 콜렉터가 소거하므로 아직 소멸 x
          
  - 값형과 참조형의 주요 차이점
    
    - 값 유형은 스택 메모리에 저장되고 참조 유형은 힙 메모리에 저장됨
      
    - 구조체, 문자열, 열거형을 제외한 모든 기본 데이터 유형은 값형의 예시
      
    - 값형이 다른 값형에 복사되면 실제 값은 복사되지만 참조형이 다른 참조형에 복사되면 값의 참조 주소는 복사
      
    - 값형은 0으로 초기화하고 참조형은 null로 초기화 가능
      
    - 값형 null 불가능 (변수 속의 값이 반드시 존재해야 함)

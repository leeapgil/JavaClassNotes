# Java 프로그래밍 언어 기초
## 프로그래밍 이란?

- **프로그램(Program)**: 컴퓨터나 다른 전자 장치가 특정 작업을 수행하기 위한 명령들의 집합.
- **프로그램밍(Programming)**: 프로그램은 프로그래밍 언어로 작성되며, 컴퓨터 하드웨어가 이해할 수 있는 기계어로 변환되어 실행됨.  

## 프로그래밍 패러다임

- **절차 지향 프로그래밍**: 문제를 연속적인 단계로 해결 (예: C, Pascal)
- **이벤트 지향 프로그래밍**: 사용자 동작에 따라 흐름 결정 (예: JavaScript)
- **객체 지향 프로그래밍(OOP)**: 데이터와 메서드를 캡슐화한 객체 중심 (예: Java)

## 기계어와 어셈블리 언어, 고급언어

- **기계어**: 컴퓨터가 이해하는 이진 코드 (예: `10110000 01100001`)
- **어셈블리 언어**: 사람이 이해할 수 있는 저수준 컴퓨터 언어
- **예시**: 
  ```assembly
  section .data
      hello db 'Hello, World!',0

  section .text
      global _start

  _start:
      mov eax, 4
      mov ebx, 1
      mov ecx, hello
      mov edx, 13
      int 0x80
      mov eax, 1
      xor ebx, ebx
      int 0x80
    ```
- **고급언어** : 사람이 이해하기 쉬우며 복잡한 작업 및 자료 구조, 알고리즘 등을 표현하기 위해 고안된 언어. 
C, C++, Java, Python...

## Java란?

- **개발자**: Sun Microsystems의 "Green Team"
- **개발 시기**: 1990년대 초
- **최초 목표**: "Write Once, Run Anywhere" 구현
- **최초 이름**: "Oak" (이미 사용 중이어서 변경)
- **현재 이름의 유래**: 자바섬의 커피
- **공개 시기**: 1995년
- **적용 분야**: 웹 애플리케이션, 서버 애플리케이션, 모바일 애플리케이션(안드로이드)

## Java의 주요 특징
 
- **플랫폼 독립성**: Java의 가장 큰 특징 중 하나는 "한 번 작성하면 어디서나 실행된다(Write Once, Run Anywhere - WORA)"는 개념입니다. Java 애플리케이션은 Java 가상 머신(JVM) 위에서 실행되며, 이는 다양한 운영 체제에서 동일하게 작동합니다. 이는 프로그램이 특정 시스템에 구속되지 않도록 하는 데 중점을 두었습니다.

- **객체 지향 프로그래밍**: Java는 객체 지향 프로그래밍 언어입니다. 이는 코드의 재사용성, 모듈성, 유지 보수성을 증진시키는 것을 목표로 합니다. 클래스와 객체를 사용하여 더욱 체계적이고 유연한 프로그래밍이 가능합니다.

- **보안**: Java는 원격 소스에서 실행되는 코드에 대한 보안을 중시합니다. JVM은 코드를 실행하기 전에 여러 가지 보안 검사를 수행하여 시스템의 안전을 유지합니다.

- **네트워크 지향**: Java는 인터넷과 네트워크 애플리케이션 개발에 강력한 지원을 제공합니다. 초기에 Java는 웹 애플리케이션과 더 넓은 네트워크 환경에서의 사용을 염두에 두고 개발되었습니다.

- **성능**: 처음에는 인터프리터 언어로 인식되어 성능이 느리다는 인식이 있었지만, JIT(Just-In-Time) 컴파일러의 도입과 여러 최적화 기법을 통해 성능이 크게 향상되었습니다.

- **멀티스레딩**: Java는 내장된 멀티스레딩 기능을 지원하여, 효율적인 동시성과 병렬 처리가 가능합니다.

- **메모리 관리**: 자동 메모리 관리 및 가비지 컬렉션 기능은 메모리 누수와 같은 문제를 최소화하고 프로그래머의 부담을 줄입니다.

- **요약**: C++와 유사, 객체 지향 프로그래밍에 중점, 메모리 관리 및 보안을 추상화, 코드의 재사용성과 확장성, 복잡성 관리

Java의 이러한 특징들은 넓은 범위의 애플리케이션 개발, 특히 대규모 엔터프라이즈 시스템, 모바일 애플리케이션, 임베디드 시스템, 클라우드 기반 서비스 등에 적합하게 만들어짐.

## 추상화와 추상적 개념

- **추상화(abstracting)**: 복잡한 개념이나 시스템을 간단하게 만드는 과정
- **추상적(abstract)**: 구체적이지 않고 다양한 해석 가능
- **예술에서의 추상화**: 복잡한 현실을 단순화, 일반화하는 미술 기법

## 알고리즘

- **정의**: 문제 해결을 위한 명확한 절차나 규칙
- **예시**: 두 수를 더하는 간단한 알고리즘 (f(a, b) = a + b) 
- **성능 측정**: 시간 복잡도와 공간 복잡도


# 실습 

- Hello.java

```java
public class Hello {
    // 라인 주석 Ctrl + /
    // Ctrl + (+)or(-) 글자크기 + or -
    public static void main(String[] args) {
        // 콘솔 출력 
        // 각 코드의 종료는 ;< -- 세미콜론
        System.out.println("Hello World");
        // main 코드실행 Ctrl + F11 or 마우스 우클릭 + Run as + Java application
        // Ctrl + d 라인삭제 
        // Alt + (위/아래) 라인이동 
    }
}
```

- VariableName.java

```java
package ch02_variable;

public class VariableName {

    public static void main(String[] args) {
        // 변수명, 클래스명 명명 규칙 

        // 여러줄 주석 
        /*  
         *  프로젝트,클래스명 이름은 앞에 대문자를 씀.(JavaStudy..)
         *  
         *  패키지(폴더) 이름은 전부 소문자로 작성
         *  필요하다면 단어 사이에 언더바(_)를 넣어서 사용 (ch01_start..)
         * 
         *  변수명( or 함수명)
         *  카멜 표기법(Camel, 낙타 표기법이라함.)
         *  첫글자는 소문자, 다음 단어들은 대문자로 시작 
         *  ex) todayIsHappy 
         *  
         *  python은 스네이크 표기법사용
         *  ex) today_is_happy
         *  
         * */
        //[데이터 타입] [변수명]      
        // 정수타입
        int todayIsHappy = 0;
        todayIsHappy = todayIsHappy + 10;
        todayIsHappy = todayIsHappy + 1;
        System.out.println(todayIsHappy);

        byte byteVar = 1;
        System.out.println(byteVar);
        short shortVar = 2;
        System.out.println(shortVar);
        int intVar = 3;
        System.out.println(intVar);
        long longVar = 30000000000L;   // long 은 L이 붙음
        System.out.println(longVar); //ctrl + alt + 아래방향
        // 정수 이면서 문자에 해당
        char charVar = 44032; // '가'와 같음
        char ga = '가';
        // 소수 타입
        float floatVar = 3.14f;
        double doubleVar = 3.14;
        // 불리언 타입(참/거짓, ture/false)
        boolean boolVar = false;
        // 문자열 타입
        String strToday = "오늘은 1월 2일";

    }

}
```

- VariableMain.java

```java
package ch02_variable;

public class VariableMain {

    public static void main(String[] args) {
        // 상수(Constant) 변경 불가 
        final double MATH_PI = 3.14;
        // MATH_PI = 4.23;  // 오류남(상수는 변경이 안되기 때문)
        double mathPi2 = 3.11;
        mathPi2 = 3.14;  // 변수는 변경가능

        // 문자열 String 타입은 클래스로 관리되어짐.(다양한 메소드(함수)를 내장하고 있음)
        String fruits = "Apple, Banana, Cherry";
        //.length() 문자열의 길이를 리턴 
        System.out.println(fruits);
        System.out.println("길이 :" + fruits.length()); // 함수는 함수명() <-- 실행
        //.charAt(인덱스) 
        System.out.println("3인덱스:" + fruits.charAt(3));
        //.indexOf(문자열) 
        // 해당 String에서 '문자열'을 찾아서 첫번째 인덱스를 반환 존재하지 않으면 -1 반환
        System.out.println("Banana 시작인덱스:" + fruits.indexOf("Banana"));
        //.substring(시작 인덱스) 해당 문자열의 시작 인덱스 부터 끝까지 자른다.
        //.substring(시작, 종료인덱스) 해당 문자열의 시작 인덱스부터 끝인덱스 전까지 자른다.)
        System.out.println(fruits.substring(15));
        System.out.println(fruits.substring(7, 13));
        // .replace(바뀔 문자열, 바꿀 문자열)
        System.out.println(fruits.replace("Cherry","Chamwui"));
        // , <-- 를 찾아서 | 로 변경하시오 
        System.out.println(fruits.replace(",","|"));

        String email = "pangsu@gmail.com";
        // 다음 문자열에서 @ 를 기준으로 앞과 뒤를 각각 출력하시오 
        // pangsu
        // gmail.com
        System.out.println(email.indexOf("@"));
        System.out.println(email);
        System.out.println(email.substring(0,email.indexOf("@")));
        System.out.println(email.substring(email.indexOf("@")+1));
    }
}
```


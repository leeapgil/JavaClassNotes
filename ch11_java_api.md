# Java API 소개

Java API (Application Programming Interface)는 자바 프로그래밍 언어로 작성된 소프트웨어 구성 요소 간의 상호 작용을 용이하게 하는 라이브러리 및 도구 모음입니다. 

## 주요 특징들

1. **표준 라이브러리**
   - 기본 데이터 구조, 네트워킹, 파일 시스템 접근, 그래픽 사용자 인터페이스 구성 등을 위한 클래스와 인터페이스 제공.
2. **객체 지향 디자인**
   - 코드의 재사용성과 유지 관리 용이.
3. **플랫폼 독립성**
   - Java 가상 머신(JVM)이 설치된 모든 시스템에서 실행 가능.
4. **확장성 및 유연성**
   - 다양한 유형의 응용 프로그램 개발 지원.
5. **풍부한 라이브러리**
   - 수학 함수, 날짜 및 시간 처리, I/O 처리, 네트워킹, XML 파싱 등 지원.
6. **보안 및 강력한 에러 처리**
   - 안정적이고 신뢰할 수 있는 소프트웨어 개발 가능.

---

# Java 표준 라이브러리: Math, Random, Date, Calendar

Java는 다양한 기능을 수행하는 표준 라이브러리를 제공합니다. 여기에는 수학 연산, 난수 생성, 날짜 및 시간 처리와 관련된 클래스들이 포함됩니다.

## Math 클래스

### 기본 설명
- `Math` 클래스는 기본적인 수학 연산과 관련된 메소드를 제공합니다.
- 모든 메소드는 정적(static)이므로, 객체 생성 없이 직접 사용 가능합니다.

### 주요 사용법
```java
// 절대값 계산
int absValue = Math.abs(-10);

// 최대값, 최소값
int max = Math.max(10, 20);
int min = Math.min(10, 20);

// 제곱근
double sqrtValue = Math.sqrt(25);

// 거듭제곱
double powValue = Math.pow(2, 3);
```

## Random 클래스

### 기본 설명
- `Random` 클래스는 난수를 생성하는 데 사용됩니다.
- 객체를 생성하여 다양한 타입의 난수를 얻을 수 있습니다.

### 주요 사용법
```java
import java.util.Random;

Random random = new Random();

// 정수 난수 생성
int randomInt = random.nextInt();

// 0과 100 사이의 정수 난수
int randomInt100 = random.nextInt(100);
```

## Date 클래스

### 기본 설명
- `Date` 클래스는 날짜와 시간을 표현하는 데 사용됩니다.
- 현재 시간으로 `Date` 객체를 생성하거나, 특정 시간을 설정할 수 있습니다.

### 주요 사용법
```java
import java.util.Date;

// 현재 날짜와 시간으로 Date 객체 생성
Date now = new Date();

// Date 객체의 시간 출력
System.out.println(now.toString());
```

## Calendar 클래스

### 기본 설명
- `Calendar` 클래스는 날짜와 시간을 조작하는 데 사용됩니다.
- `Date` 클래스보다 더 유연하고 세밀한 날짜/시간 조작이 가능합니다.

### 주요 사용법
```java
import java.util.Calendar;

// Calendar 객체 생성
Calendar calendar = Calendar.getInstance();

// 현재 날짜와 시간
int year = calendar.get(Calendar.YEAR);
int month = calendar.get(Calendar.MONTH); // 주의: 0부터 시작
int day = calendar.get(Calendar.DAY_OF_MONTH);

// 특정 필드 값 변경
calendar.set(Calendar.YEAR, 2023);
```

---

이 내용은 `Math`, `Random`, `Date`, `Calendar` 클래스의 기본적인 사용법과 그 특징을 간략하게 설명합니다. Java에서 제공하는 이러한 클래스들은 일반적인 프로그래밍 작업에서 매우 유용하게 사용됩니다.

---

Java의 `Random` 클래스를 사용하여 10% 확률로 특정 이벤트가 발생하는 카드 뽑기 게임 예제를 만들어보겠습니다. 이 예제에서는 100개의 카드 중 10개만 당첨 카드로 설정하고, 사용자가 카드를 뽑았을 때 당첨 여부를 판단합니다.

```java
import java.util.Random;

public class CardGame {
    public static void main(String[] args) {
        Random random = new Random();

        // 카드 뽑기
        int card = random.nextInt(100) + 1; // 1부터 100까지의 숫자 중 하나를 랜덤으로 선택

        // 10% 확률 (1부터 10까지의 숫자 중 하나가 선택되면 당첨)
        if (card <= 10) {
            System.out.println("축하합니다! 당첨된 카드입니다: " + card);
        } else {
            System.out.println("아쉽지만, 당첨되지 않은 카드입니다: " + card);
        }
    }
}
```

이 코드는 다음과 같이 작동합니다:
1. `Random` 객체를 생성합니다.
2. 1부터 100까지의 숫자 중 하나를 랜덤으로 뽑습니다 (`nextInt(100)`는 0부터 99까지 반환하므로, +1을 해서 1부터 100까지가 되도록 합니다).
3. 뽑힌 카드 번호가 10 이하이면 당첨된 것으로 간주합니다 (이는 10% 확률과 같습니다).
4. 당첨 여부에 따라 적절한 메시지를 출력합니다.

이 예제는 간단한 확률 게임의 기본 개념을 보여주며, 확률을 변경하거나 게임의 규칙을 더 복잡하게 만들어 더 다양한 시나리오를 구현할 수 있습니다.

# Java 표준 라이브러리: SimpleDateFormat, TimeZone

Java에서는 `SimpleDateFormat`과 `TimeZone` 클래스를 통해 날짜 및 시간 포맷팅과 시간대 처리를 할 수 있습니다.

## SimpleDateFormat 클래스

### 기본 설명
- `SimpleDateFormat`은 날짜와 시간을 원하는 형식으로 포맷팅하는 데 사용됩니다.
- 다양한 패턴 문자를 사용하여 날짜 및 시간 형식을 지정할 수 있습니다.

### 주요 사용법
```java
import java.text.SimpleDateFormat;
import java.util.Date;

// SimpleDateFormat 객체 생성
SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");

// 현재 날짜와 시간으로 Date 객체 생성
Date now = new Date();

// 날짜를 지정된 포맷으로 변환
String formattedDate = sdf.format(now);

System.out.println(formattedDate);
```

이 예제에서는 `yyyy-MM-dd HH:mm:ss` 포맷을 사용하여 현재 날짜와 시간을 문자열로 변환합니다.

## TimeZone 클래스

### 기본 설명
- `TimeZone` 클래스는 세계의 다양한 시간대를 표현하고 처리하는 데 사용됩니다.
- `SimpleDateFormat`과 함께 사용하여 특정 시간대에 맞는 날짜와 시간을 표시할 수 있습니다.

### 주요 사용법
```java
import java.text.SimpleDateFormat;
import java.util.Calendar;
import java.util.TimeZone;

// TimeZone 객체 생성
TimeZone timeZoneNY = TimeZone.getTimeZone("America/New_York");

// SimpleDateFormat에 TimeZone 설정
SimpleDateFormat sdfNY = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
sdfNY.setTimeZone(timeZoneNY);

// 현재 날짜와 시간
Calendar now = Calendar.getInstance();

// 날짜를 뉴욕 시간대에 맞게 변환
String formattedDateNY = sdfNY.format(now.getTime());

System.out.println("New York Time: " + formattedDateNY);
```

이 예제에서는 `America/New_York` 시간대를 사용하여 뉴욕의 현재 시간을 포맷팅하여 출력합니다.

---

이 내용은 `SimpleDateFormat`과 `TimeZone` 클래스를 사용하여 날짜와 시간을 원하는 형식으로 포맷팅하고, 다양한 시간대에 맞게 조정하는 방법을 설명합니다. 이러한 기능은 특히 글로벌하게 서비스하는 응용 프로그램 개발에 매우 유용합니다.

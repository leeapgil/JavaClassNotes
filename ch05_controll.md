## Java `if` 문

### 설명
Java에서 `if` 문은 조건을 테스트하고, 조건이 `true`일 경우 코드 블록을 실행합니다. `if` 문은 다음과 같은 형식으로 작성됩니다:

```java
if (조건) {
    // 조건이 참일 때 실행될 코드
}
```

선택적으로 `else` 블록을 추가하여 조건이 `false`일 때 실행될 코드를 정의할 수 있습니다.

### 예제
```java
int number = 10;

if (number > 0) {
    System.out.println("Number is positive.");
} else {
    System.out.println("Number is not positive.");
}
```
물론입니다. Java에서 `if`, `if-else`, 그리고 중첩 `if` 문에 대한 예제와 주의사항을 Markdown 형식으로 작성하겠습니다.

---

## Java `if` 문

### 예제
```java
int number = 7;

if (number > 5) {
    System.out.println("Number is greater than 5.");
}
```

### 주의사항
- `if` 문의 조건은 항상 괄호 안에 작성해야 합니다.
- 조건이 참(`true`)일 때만 코드 블록이 실행됩니다.
- 코드 블록은 중괄호 `{}`로 묶어야 합니다.

---

## Java `if-else` 문

### 예제
```java
int number = 4;

if (number % 2 == 0) {
    System.out.println("Number is even.");
} else {
    System.out.println("Number is odd.");
}
```

### 주의사항
- `if-else` 문은 두 개의 코드 블록 중 하나만 실행됩니다.
- `if` 조건이 거짓(`false`)일 때 `else` 블록이 실행됩니다.

---

## Java 중첩 `if` 문

### 예제
```java
int number = 15;

if (number > 10) {
    if (number % 2 == 0) {
        System.out.println("Number is greater than 10 and even.");
    } else {
        System.out.println("Number is greater than 10 and odd.");
    }
}
```

### 주의사항
- 중첩 `if` 문은 한 `if` 문 안에 다른 `if` 문을 포함합니다.
- 중첩이 깊어질수록 코드의 복잡성이 증가하므로, 가능한 한 간결하게 유지하는 것이 좋습니다.
- 각 `if` 블록은 독립적으로 조건을 검사합니다.

---

이 예제들은 `if`, `if-else`, 그리고 중첩 `if` 문의 기본적인 사용법을 보여줍니다. 복잡한 조건을 처리할 때 유용하게 사용할 수 있지만, 중첩된 `if` 문은 코드의 가독성을 저하시킬 수 있으므로 주의해서 사용해야 합니다.

---

## Java `switch` 문

### 설명
`switch` 문은 변수의 값에 따라 다양한 경우(case)를 실행할 수 있도록 합니다. `switch` 문의 기본 구조는 다음과 같습니다:

```java
switch (변수) {
    case 값1:
        // 변수가 값1일 때 실행될 코드
        break;
    case 값2:
        // 변수가 값2일 때 실행될 코드
        break;
    // 추가적인 경우...
    default:
        // 어떤 경우에도 해당하지 않을 때 실행될 코드
}
```

### 예제
```java
int day = 4;

switch (day) {
    case 1:
        System.out.println("Monday");
        break;
    case 2:
        System.out.println("Tuesday");
        break;
    case 3:
        System.out.println("Wednesday");
        break;
    case 4:
        System.out.println("Thursday");
        break;
    case 5:
        System.out.println("Friday");
        break;
    case 6:
        System.out.println("Saturday");
        break;
    case 7:
        System.out.println("Sunday");
        break;
    default:
        System.out.println("Invalid day");
}
```

---

이 예제들은 Java의 기본적인 조건문 사용법을 보여줍니다. 실제 프로그래밍에서는 이러한 조건문들을 조합하여 복잡한 로직을 구현할 수 있습니다.

---

## Java `for` 문

### 기초 설명
`for` 문은 반복문으로, 조건이 참인 동안 코드 블록을 반복해서 실행합니다. 기본 구조는 다음과 같습니다:

```java
for (초기화; 조건; 증감) {
    // 반복 실행될 코드
}
```

- **초기화**: 반복문이 시작할 때 한 번 실행되며, 반복문의 제어 변수를 초기화합니다.
- **조건**: 각 반복 전에 평가되며, 참일 경우 반복문이 계속 실행됩니다.
- **증감**: 반복문의 끝에 도달할 때마다 실행되어 제어 변수를 갱신합니다.

### 예제
#### 기본 `for` 문
```java
for (int i = 0; i < 5; i++) {
    System.out.println("i = " + i);
}
```

#### 무한 `for` 문
```java
for (;;) {
    // 무한 반복
}
```

#### 배열과 함께 사용
```java
int[] numbers = {1, 2, 3, 4, 5};
for (int i = 0; i < numbers.length; i++) {
    System.out.println("Number: " + numbers[i]);
}
```

#### 개선된 `for` 문 (for-each)
```java
int[] numbers = {1, 2, 3, 4, 5};
for (int number : numbers) {
    System.out.println("Number: " + number);
}
```

### 주의사항
- 초기화 부분에서 선언된 변수는 `for` 문 내에서만 유효합니다.
- `for` 문의 조건이 항상 거짓이면 코드 블록은 한 번도 실행되지 않습니다.
- 무한 루프를 피하기 위해 적절한 종료 조건을 설정해야 합니다.

---

## Java 중첩 `for` 문

### 예제
```java
for (int i = 1; i <= 5; i++) {
    for (int j = 1; j <= i; j++) {
        System.out.print("*");
    }
    System.out.println();
}
```

### 주의사항
- 중첩 `for` 문은 반복문 안에 또 다른 반복문이 있는 구조입니다.
- 중첩 깊이가 깊어질수록 코드의 복잡성과 실행 시간이 증가할 수 있습니다.
- 각 반복문은 독립적인 제어 변수를 가져야 합니다.

---

`for` 문과 중첩 `for` 문은 Java에서 반복적인 작업을 수행하기 위해 널리 사용됩니다. 이들을 효과적으로 사용하면 코드를 간결하고 효율적으로 만들 수 있습니다. 그러나 중첩 반복문은 복잡도가 높아질 수 있으므로 주의 깊게 사용해야 합니다.
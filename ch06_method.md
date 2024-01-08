# Java의 메소드와 함수의 차이점 및 접근 제한자와 기본 사용법

## Java에서의 메소드 개념

Java에서 **메소드(method)** 는 특정 작업을 수행하는 코드 블록입니다. 클래스 내에 정의되며, 다른 코드에서 호출되어 실행될 수 있습니다. 메소드는 코드의 재사용성, 가독성 및 조직화에 도움이 됩니다.

### 기본 문법

```java
accessModifier returnType methodName(parameterList) {
    // 메소드 본문
}
```

- `accessModifier`: 메소드의 가시성을 결정합니다 (예: `public`, `private`).
- `returnType`: 메소드에서 반환하는 값의 데이터 타입입니다. 반환 값이 없는 경우 `void`를 사용합니다.
- `methodName`: 네이밍 컨벤션을 따르는 메소드의 이름입니다.
- `parameterList`: 메소드에 전달되는 인자들로, 괄호 안에 포함됩니다.

## 함수와의 차이점

Java에서는 "함수(function)"라는 용어가 일반적으로 메소드와 동일하게 사용됩니다. 하지만, 기술적으로 Java는 객체 지향 언어이므로 모든 함수는 클래스의 일부로 존재하는 "메소드"입니다. 함수는 보통 독립적인 코드 블록을 의미하며, 객체 지향이 아닌 언어에서 더 일반적으로 사용됩니다.

## 접근 제한자(Access Modifiers)

접근 제한자는 클래스, 변수, 메소드 또는 생성자에 대한 접근을 제어하는 키워드입니다. Java에는 네 가지 주요 접근 제한자가 있습니다:

1. `public`: 어디서든 접근 가능합니다.
2. `protected`: 같은 패키지 내부, 또는 서브 클래스에서 접근 가능합니다.
3. `default`(선언되지 않음): 같은 패키지 내에서만 접근 가능합니다.
4. `private`: 같은 클래스 내에서만 접근 가능합니다.

### 예시

```java
public class ExampleClass {
    private int privateVar;
    public int publicVar;

    private void privateMethod() {
        // ...
    }

    public void publicMethod() {
        // ...
    }
}



# Java에서 기본적인 메소드 생성과 사용법 및 재귀함수의 사용법과 주의사항

## 기본적인 메소드 생성과 사용법

Java에서 메소드를 생성하고 사용하는 것은 클래스의 기능을 구현하는 데 중요한 부분입니다.

### 메소드 생성하기

1. **메소드 선언**: 반환 타입, 메소드 이름, 매개변수를 포함합니다.
2. **매개변수**: 메소드가 수행할 작업에 필요한 입력을 정의합니다.
3. **반환 타입**: 메소드가 작업을 완료한 후 반환하는 데이터의 유형입니다. 반환 값이 없는 경우 `void`를 사용합니다.

### 예시

```java
public class Calculator {
    // 두 수의 합을 반환하는 메소드
    public int add(int a, int b) {
        return a + b;
    }
}
```

### 메소드 사용하기

메소드를 사용하기 위해서는 해당 메소드가 정의된 클래스의 인스턴스를 생성한 후, 이 인스턴스를 통해 메소드를 호출합니다.

```java
public class Main {
    public static void main(String[] args) {
        Calculator calc = new Calculator();
        int result = calc.add(5, 10);
        System.out.println("Result: " + result);
    }
}
```

## 재귀함수의 사용법과 주의사항

재귀함수는 자기 자신을 호출하여 문제를 해결하는 함수입니다. 재귀는 많은 알고리즘에서 유용하지만, 주의 깊게 사용해야 합니다.

### 재귀함수 사용법

1. **기본 단계(Base Case)**: 재귀 호출이 멈추는 조건을 정의합니다. 이는 무한 루프에 빠지지 않도록 합니다.
2. **재귀 단계(Recursive Case)**: 문제를 더 작은 문제로 나누고 자기 자신을 다시 호출합니다.

### 예시: 팩토리얼 계산

```java
public class Factorial {
    public static int factorial(int n) {
        if (n == 1) { // 기본 단계
            return 1;
        } else {
            return n * factorial(n - 1); // 재귀 단계
        }
    }
}
```

### 주의사항

1. **무한 재귀 방지**: 항상 기본 단계를 정의하여 재귀 호출이 종료될 수 있도록 해야 합니다.
2. **스택 오버플로우**: 재귀 호출이 너무 많이 발생하면 스택 오버플로우가 발생할 수 있습니다. 따라서 재귀 깊이에 주의해야 합니다.
3. **성능 고려**: 일부 경우에는 반복문이 재귀보다 효율적일 수 있으므로, 성능을 고려하여 적절한 접근 방식을 선택해야 합니다.

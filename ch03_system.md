### Java의 표준 스트림: `System.out`, `System.in`, `System.err`

#### 1. `System.out`
`System.out`은 주로 콘솔에 메시지를 출력할 때 사용됩니다. `System.out.println()`, `System.out.print()`, `System.out.printf()` 등의 메소드를 포함합니다.

**예제:**
```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!"); // 새로운 줄에서 메시지 출력
        System.out.print("Hello, Java!"); // 줄바꿈 없이 메시지 출력
        System.out.printf("Hello, %s!", "Programming"); // 형식화된 출력
    }
}
```

#### 2. `System.in`
`System.in`은 사용자의 입력을 받기 위해 사용됩니다. 보통 `Scanner` 클래스와 함께 사용됩니다.

**예제:**
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter your name: ");
        String name = scanner.nextLine();
        System.out.println("Hello, " + name + "!");
    }
}
```

#### 3. `System.err`
`System.err`은 오류 메시지를 출력할 때 사용됩니다. `System.out`와 유사하지만, 일반적으로 오류 메시지를 다룰 때 사용됩니다.

**예제:**
```java
public class Main {
    public static void main(String[] args) {
        try {
            int[] numbers = new int[5];
            numbers[10] = 3; // 이 줄에서 ArrayIndexOutOfBoundsException 발생
        } catch (ArrayIndexOutOfBoundsException e) {
            System.err.println("Error: " + e.getMessage());
        }
    }
}
```

이 예제들은 각 스트림의 기본적인 사용법을 보여줍니다. 실제 프로그램에서는 이러한 스트림들을 다양한 방식으로 활용할 수 있습니다.

--- 


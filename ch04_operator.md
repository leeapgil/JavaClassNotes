### Java 연산자

#### 1. 증감 연산자
증감 연산자는 변수의 값을 1 증가시키거나 감소시킵니다. `++`는 값을 1 증가시키고, `--`는 값을 1 감소시킵니다. 증감 연산자는 변수 앞(전위)이나 뒤(후위)에 위치할 수 있으며, 위치에 따라 연산의 결과가 달라질 수 있습니다.

**예제:**
```java
public class Main {
    public static void main(String[] args) {
        int a = 5;
        int b = 5;

        System.out.println(a++); // 후위 증가: 출력 후 증가, 출력값은 5
        System.out.println(++b); // 전위 증가: 증가 후 출력, 출력값은 6
    }
}
```

#### 2. 비교 연산자
비교 연산자는 두 값을 비교하여 true 또는 false 값을 반환합니다. 주로 `==`, `!=`, `>`, `<`, `>=`, `<=` 등이 있습니다.

**예제:**
```java
public class Main {
    public static void main(String[] args) {
        int x = 10;
        int y = 20;

        System.out.println(x == y); // false
        System.out.println(x != y); // true
        System.out.println(x > y);  // false
        System.out.println(x < y);  // true
        System.out.println(x >= 10); // true
        System.out.println(y <= 20); // true
    }
}
```

#### 3. 삼항 연산자
삼항 연산자는 조건식을 평가하여 두 개의 결과 중 하나를 반환합니다. 형식은 `조건식 ? 값1 : 값2`입니다. 조건식이 참이면 값1을, 거짓이면 값2를 반환합니다.

**예제:**
```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        int b = 5;

        int max = (a > b) ? a : b;
        System.out.println("큰 수: " + max); // 10
    }
}
```

#### 4. 논리 연산자
논리 연산자는 불리언 값(참/거짓)을 기반으로 한 연산을 수행합니다. 주로 `&&`(논리곱), `||`(논리합), `!`(부정) 연산자가 있습니다.

**예제:**
```java
public class Main {
    public static void main(String[] args) {
        boolean a = true;
        boolean b = false;

        System.out.println(a && b); // false (둘 다 참이어야 true)
        System.out.println(a || b); // true (하나라도 참이면 true)
        System.out.println(!a);     // false (a의 부정)
    }
}
```


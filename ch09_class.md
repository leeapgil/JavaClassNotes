## Chapter 09: Classes in Java and Object-Oriented Programming

### Object-Oriented Programming (OOP) - History and Objectives

- **역사**: 객체 지향 프로그래밍(OOP)은 1960년대 후반에 등장했습니다. 이 개념은 소프트웨어의 복잡성을 관리하고, 더 나은 코드 재사용과 유지 보수를 가능하게 하는 데 중점을 두고 있습니다.
- **목표**:
  - **캡슐화**: 데이터와 이 데이터를 처리하는 함수를 하나의 단위로 묶어 관리합니다.
  - **상속**: 기존 클래스의 특성을 상속받아 새로운 클래스를 생성합니다.
  - **다형성**: 같은 이름의 메소드가 다양한 방식으로 동작할 수 있게 합니다.

### Java Classes - Basic Components

Java의 클래스는 객체 지향 프로그래밍의 핵심 구성 요소입니다. 클래스는 객체의 설계도와 같으며, 객체의 상태를 나타내는 필드(변수)와 행동을 나타내는 메소드(함수)로 구성됩니다.

- **구성 요소**:
  - **필드(Fields)**: 객체의 상태를 저장하는 변수
  - **메소드(Methods)**: 객체의 행동을 정의하는 함수
  - **생성자(Constructor)**: 객체를 생성할 때 초기화하는 특별한 메소드

### Example: Defining a Class in Java

아래는 Java에서 간단한 클래스를 정의하고 사용하는 예제입니다.

```java
public class Car {
    // 필드 (Fields)
    String brand;
    int year;

    // 생성자 (Constructor)
    public Car(String brand, int year) {
        this.brand = brand;
        this.year = year;
    }

    // 메소드 (Methods)
    public void displayInfo() {
        System.out.println("Brand: " + brand + ", Year: " + year);
    }
}

public class Main {
    public static void main(String[] args) {
        // Car 객체 생성
        Car myCar = new Car("Toyota", 2020);

        // 메소드 호출
        myCar.displayInfo();
    }
}
```

이 예제에서, `Car` 클래스는 브랜드와 연도를 나타내는 필드를 가지고 있습니다. `Car`의 생성자는 이 필드들을 초기화하며, `displayInfo` 메소드는 이 정보를 출력합니다. `main` 메소드에서는 `Car` 객체를 생성하고, 이 객체의 `displayInfo` 메소드를 호출하여 정보를 출력합니다.

---
이러한 클래스와 객체 지향 개념은 Java 프로그래밍에서 매우 중요합니다. 클래스를 통해 데이터와 기능을 묶어 관리함으로써, 코드의 재사용성과 유지보수가 용이해집니다.

## Java Programming: Getters, Setters, toString, `this`, and Constructors

### Getters and Setters

- **설명**: Getter와 Setter는 객체의 필드(변수)에 안전하게 접근하고 수정하기 위한 메소드입니다. Getter는 필드 값을 반환하고, Setter는 필드 값을 설정합니다.
- **예제**:
  ```java
  public class Student {
      private String name;

      // Getter
      public String getName() {
          return name;
      }

      // Setter
      public void setName(String name) {
          this.name = name;
      }
  }
  ```

### toString Method

- **설명**: `toString` 메소드는 객체의 문자열 표현을 반환합니다. `Object` 클래스에서 상속받은 `toString`을 오버라이드하여 객체의 상태를 나타내는 문자열을 제공할 수 있습니다.
- **예제**:
  ```java
  @Override
  public String toString() {
      return "Student{" +
             "name='" + name + '\'' +
             '}';
  }
  ```

### `this` Keyword

- **설명**: `this` 키워드는 현재 객체를 참조하는 데 사용됩니다. 주로 로컬 변수와 인스턴스 변수를 구별하는 데 사용됩니다.
- **예제**:
  ```java
  public void setName(String name) {
      this.name = name; // 'this.name' refers to the instance variable
  }
  ```

### Constructors

- **설명**: 생성자는 클래스의 인스턴스를 초기화하는 특별한 메소드입니다. 클래스 이름을 사용하며, 반환 타입을 가지지 않습니다.
- **예제**:
  ```java
  public Student(String name) {
      this.name = name;
  }
  ```

### Complete Example

아래는 위의 개념들이 적용된 전체 예제입니다.

```java
public class Student {
    private String name;

    // Constructor
    public Student(String name) {
        this.name = name;
    }

    // Getter
    public String getName() {
        return name;
    }

    // Setter
    public void setName(String name) {
        this.name = name;
    }

    // toString method
    @Override
    public String toString() {
        return "Student{" +
               "name='" + name + '\'' +
               '}';
    }

    public static void main(String[] args) {
        Student student = new Student("John");
        System.out.println(student.toString()); // 출력: Student{name='John'}
        student.setName("Jane");
        System.out.println(student.getName()); // 출력: Jane
    }
}
```

이 예제에서, `Student` 클래스는 이름을 저장하는 `name` 필드를 가지고 있습니다. `Student`의 생성자는 `name` 필드를 초기화하며, `getName`과 `setName` 메소드는 각각 `name` 필드의 값을 읽고 수정합니다. `toString` 메소드는 `Student` 객체의 문자열 표현을 제공합니다.

---
## Java Programming Concepts: Singleton, Encapsulation, and Interfaces

### Singleton Pattern

#### 설명
싱글톤 패턴은 클래스의 인스턴스가 오직 하나만 생성되도록 보장하는 디자인 패턴입니다. 이를 통해 전역적으로 접근 가능한 단일 인스턴스를 제공합니다.

#### 구현 방법
1. 생성자를 `private`으로 선언하여 외부에서의 인스턴스 생성을 차단합니다.
2. 클래스 내부에 `static` `private` 인스턴스를 유지합니다.
3. `public static` 메소드를 통해 인스턴스에 접근할 수 있도록 합니다.

#### 예제
```java
public class Singleton {
    private static Singleton instance = new Singleton();

    private Singleton() {}

    public static Singleton getInstance() {
        return instance;
    }
}
```

### Encapsulation

#### 설명
캡슐화는 클래스 내부의 데이터(필드)를 외부로부터 숨기고, 해당 데이터에 접근하는 메소드를 제공하는 방법입니다. 이를 통해 데이터 보호 및 추상화가 가능합니다.

#### 구현 방법
1. 클래스 필드를 `private`으로 선언합니다.
2. 필드에 접근할 수 있는 `public` 메소드(getter/setter)를 제공합니다.

#### 예제
```java
public class EncapsulatedObject {
    private int data;

    public int getData() {
        return data;
    }

    public void setData(int data) {
        this.data = data;
    }
}
```

### Interfaces

#### 설명
인터페이스는 메소드의 시그니처만을 정의하는 추상 타입입니다. 이를 구현하는 클래스는 인터페이스에 정의된 모

든 메소드를 구현해야 합니다.

#### 구현 방법
1. `interface` 키워드를 사용하여 인터페이스를 선언합니다.
2. 클래스에서 `implements` 키워드를 사용하여 인터페이스를 구현합니다.

#### 예제
```java
interface Vehicle {
    void drive();
}

public class Car implements Vehicle {
    @Override
    public void drive() {
        System.out.println("Car is driving");
    }
}
```

### Complete Example

아래 예제에서는 싱글톤 패턴, 캡슐화, 그리고 인터페이스의 적용을 보여줍니다.

```java
// Singleton Pattern Implementation
public class Database {
    private static Database instance = new Database();

    private Database() {}

    public static Database getInstance() {
        return instance;
    }

    public void connect() {
        System.out.println("Database Connection Established");
    }
}

// Encapsulation Implementation
public class Person {
    private String name;

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }
}

// Interface Implementation
interface Greetable {
    void greet();
}

public class FriendlyPerson implements Greetable {
    @Override
    public void greet() {
        System.out.println("Hello!");
    }
}

public class Main {
    public static void main(String[] args) {
        // Singleton Usage
        Database db = Database.getInstance();
        db.connect();

        // Encapsulation Usage
        Person person = new Person();
        person.setName("John Doe");
        System.out.println("Name: " + person.getName());

        // Interface Usage
        FriendlyPerson friendlyPerson = new FriendlyPerson();
        friendlyPerson.greet();
    }
}
```

---

이러한 Java 프로그래밍 개념들은 소프트웨어 설계에서 중요한 역할을 합니다. 싱글톤 패턴은 전역 접근과 인스턴스 관리에 유용하며, 캡슐화는 데이터 보호와 추상화를 달성하는 데 도움을 줍니다. 인터페이스는 유연한 코드 구조와 다형성을 가능하게 합니다.

### Java 상속(Inheritance)의 개념

#### 정의 및 목적
- **상속**은 Java에서 중요한 객체지향 프로그래밍의 개념 중 하나입니다.
- 상속을 통해 한 클래스가 다른 클래스의 속성 및 메소드를 상속받을 수 있습니다.
- 이를 통해 코드의 재사용성을 높이고, 유지 보수를 용이하게 만듭니다.

#### 기본 구문
```java
class Subclass extends Superclass {
    // additional fields and methods
}
```
- `Subclass`는 `Superclass`의 모든 public 및 protected 멤버를 상속받습니다.
- `private` 멤버는 상속되지 않습니다.

#### 예시
```java
class Animal {
    void eat() {
        System.out.println("동물이 먹는 중...");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("개가 짖는 중...");
    }
}
```
- `Dog` 클래스는 `Animal` 클래스로부터 `eat()` 메소드를 상속받습니다.

### Java 추상 클래스(Abstract Class)의 개념

#### 정의 및 목적
- **추상 클래스**는 하나 이상의 추상 메소드를 포함하며, 자체로는 인스턴스화될 수 없는 클래스입니다.
- 추상 클래스는 상속을 통해 그 기능을 확장하는 데 사용됩니다.
- 추상 클래스는 일반 메소드와 필드 뿐만 아니라 추상 메소드(구현되지 않은 메소드)를 포함할 수 있습니다.

#### 기본 구문
```java
abstract class ClassName {
    // abstract methods and fields
}
```

#### 예시
```java
abstract class Animal {
    abstract void eat();
    // 추상 메소드
}

class Dog extends Animal {
    void eat() {
        System.out.println("개가 먹이를 먹는 중...");
    }
    // 'eat' 메소드 구현
}
```
- `Animal` 클래스는 추상 클래스로, `eat()` 메소드는 추상 메소드입니다.
- `Dog` 클래스는 `Animal` 클래스를 상속받고, `eat()` 메소드를 구현합니다.

#### 참고 사항
- 추상 클래스의 인스턴스를 직접 생성할 수 없습니다.
- 추상 클래스를 상속받는 하위 클래스는 추상 메소드를 반드시 구현해야 합니다.
- 추상 클래스는 일반 클래스처럼 생성자를 가질 수 있으며, 이는 하위 클래스 생성자에서 호출될 수 있습니다.
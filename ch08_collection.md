## Java Collection Framework

Java의 컬렉션 프레임워크는 데이터를 저장하고 처리하는 데 사용되는 다양한 클래스와 인터페이스를 제공합니다. 여기서는 `List`, `Set`, `Map` 인터페이스와 이들을 활용하는 방법에 대해 알아보겠습니다.

### List

- **사용법**:
  - `List` 인터페이스는 순서가 있는 컬렉션을 나타냅니다.
  - 예를 들어, `ArrayList` 클래스는 `List` 인터페이스를 구현합니다.

- **예제**:
  ```java
  import java.util.ArrayList;
  import java.util.List;

  public class ListExample {
      public static void main(String[] args) {
          List<String> fruits = new ArrayList<>();
          fruits.add("Apple");
          fruits.add("Banana");
          fruits.add("Cherry");

          // 반복문을 사용하여 리스트의 요소 출력
          for (String fruit : fruits) {
              System.out.println(fruit);
          }
      }
  }
  ```

### Set

- **사용법**:
  - `Set` 인터페이스는 중복되지 않는 요소의 집합을 나타냅니다.
  - `HashSet` 클래스는 `Set` 인터페이스의 일반적인 구현입니다.

- **예제**:
  ```java

  ```java
  import java.util.HashSet;
  import java.util.Set;

  public class SetExample {
      public static void main(String[] args) {
          Set<String> countries = new HashSet<>();
          countries.add("USA");
          countries.add("Canada");
          countries.add("Mexico");

          // 반복문을 사용하여 세트의 요소 출력
          for (String country : countries) {
              System.out.println(country);
          }
      }
  }
  ```

### Map

- **사용법**:
  - `Map` 인터페이스는 키와 값의 쌍을 저장합니다.
  - `HashMap` 클래스는 `Map` 인터페이스의 일반적인 구현입니다.

- **예제**:
  ```java
  import java.util.HashMap;
  import java.util.Map;

  public class MapExample {
      public static void main(String[] args) {
          Map<String, Integer> ageMap = new HashMap<>();
          ageMap.put("Alice", 25);
          ageMap.put("Bob", 30);
          ageMap.put("Charlie", 22);

          // 반복문을 사용하여 맵의 요소 출력

  ```java
          for (Map.Entry<String, Integer> entry : ageMap.entrySet()) {
              String key = entry.getKey();
              Integer value = entry.getValue();
              System.out.println(key + " : " + value);
          }
      }
  }
  ```

이러한 컬렉션들은 Java에서 데이터를 효율적으로 관리할 수 있게 해줍니다. 각 컬렉션 타입에는 자신만의 특징이 있으며, 이를 이해하고 적절히 활용하는 것이 중요합니다. `for-each` 반복문은 컬렉션의 모든 요소를 순회하는 데 매우 유용하며, `Map`의 경우 `entrySet()` 메소드를 사용하여 키-값 쌍을 순회할 수 있습니다.

## Java Collection Framework and Generics

Java의 컬렉션 프레임워크는 데이터 그룹을 효율적으로 저장하고 처리하기 위한 여러 클래스와 인터페이스를 제공합니다. 이들은 제네릭을 사용하여 다양한 타입의 객체를 저장할 수 있습니다.

### Generics in Collections

- **설명**: 제네릭은 컬렉션에 저장되는 객체의 타입을 컴파일 시점에서 체크하여, 타입 안전성을 제공합니다. 이는 클래스나 인터페이스 이름 뒤에 `<T>` 같은 형태로 사용됩니다.
- **예**: `List<String>`, `Map<String, Integer>`

### List Interface and Classes

#### ArrayList

- **설명**: `ArrayList`는 `List` 인터페이스를 구현한 클래스로, 내부적으로 동적 배열을 사용합니다. 요소의 추가 및 접근 시 빠른 성능을 제공합니다.
- **특징**: 배열 기반, 인덱스로 빠른 접근, 크기 조정 가능

#### LinkedList

- **설명**: `LinkedList`는 `List` 인터페이스를 구현한 클래스로, 이중 연결 리스트를 내부적으로 사용합니다. 요소의 삽입과 삭제가 빈번할 때 유용합니다.
- **특징**: 연결 리스트 기반, 요소 삽입 및 삭제 효율적

### Set Interface and Classes

#### HashSet

- **설명**: `HashSet`은 `Set` 인터페이스를 구현한 클래스로, 해시 테이블을 사용하여 요소를 저장합니다. 중복을 허용하지 않으며, 순서를 보장하지 않습니다.
- **특징**: 해시 테이블 기반, 중복 없음, 순서 없음

#### TreeSet

- **설명**: `TreeSet`은 `Set` 인터페이스를 구현한 클래스로, 레드-블랙 트리를 사용합니다. 정렬된 순서로 요소를 저장하며, 중복을 허용하지 않습니다.
- **특징**: 레드-블랙 트리 기반, 정렬된 순서, 중복 없음

### Map Interface and Classes

#### HashMap

- **설명**: `HashMap`은 `Map` 인터페이스를 구현한 클래스로, 키-값 쌍을 해시 테이블을 이용하여 저장합니다. 키는 중복될 수 없으며, 값은 중복될 수 있습니다.
- **특징**: 해시 테이블 기반, 키-값 쌍, 키 중복 불가

#### TreeMap

- **설명**: `TreeMap`은 `Map` 인터페이스를 구현한 클래스로, 레드-블랙 트리를 기반으로 키-값 쌍을 정렬된 순서로 저장합니다.
- **특징**: 레드-블랙 트리 기반, 키-값 쌍, 정렬된 키

---

이러한 컬렉션들은 제네릭을 사용하여 다양한 타입의 객체를 효율적으로 관리할 수 있게 해줍니다. 제네릭을 사용함으로써, 컴파일 시간에 타입 체크를 할 수 있어 런타임 시 발생할 수 있는 `ClassCastException`을 예방할 수 있습니다. 각각의

컬렉션 클래스는 고유의 특성과 사용 목적을 가지고 있으므로, 상황에 맞게 적절한 컬렉션을 선택하여 사용하는 것이 중요합니다.

- `ArrayList`와 `LinkedList`는 리스트 인터페이스를 구현하지만, 내부 구조와 성능 특성이 다릅니다. `ArrayList`는 빠른 임의 접근이 가능하지만 크기 변경이 비효율적이고, `LinkedList`는 요소의 삽입과 삭제에 유리합니다.
- `HashSet`과 `TreeSet`은 둘 다 집합을 나타내지만, `HashSet`은 해시 테이블을 사용하여 작동하고 `TreeSet`은 레드-블랙 트리를 사용하여 요소를 정렬된 순서로 저장합니다.
- `HashMap`과 `TreeMap`도 마찬가지로, `HashMap`은 해시 테이블을 기반으로 하여 빠른 검색을 제공하는 반면, `TreeMap`은 키를 정렬된 순서로 저장하여 순서가 중요한 상황에서 유용합니다.

제네릭을 통해 이러한 컬렉션들에 저장되는 객체의 타입을 미리 지정함으로써, 코드의 안정성과 가독성이 향상됩니다.
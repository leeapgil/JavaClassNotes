### Java 배열 (Array)

#### 정의:
- Java에서 배열은 같은 타입의 여러 변수를 하나의 연속된 메모리 공간에 저장하기 위한 방법입니다.
- 배열은 인덱스를 사용하여 각 요소에 접근합니다.

#### 배열 선언 및 초기화:
```java
int[] myArray;      // 배열 선언
myArray = new int[5]; // 배열 초기화, 5개의 정수를 저장할 수 있음
```
- 또는 한 줄로 선언 및 초기화할 수 있습니다:
```java
int[] myArray = new int[5]; // 선언과 동시에 초기화
```

#### 배열 사용:
```java
// 배열 요소에 값 할당
myArray[0] = 10;
myArray[1] = 20;

// 배열 요소의 값 읽기
int a = myArray[0]; // a에는 10이 할당됨
```

#### 배열 초기값으로 초기화:
```java
int[] myArray = {10, 20, 30, 40, 50}; // 5개의 요소로 배열 초기화
```

#### 배열의 길이:
- `array.length`를 사용하여 배열의 길이를 알 수 있습니다.

### 참조 타입 (Reference Type) 및 기본 타입 (Primitive Type)

#### 기본 타입 (Primitive Type):
- 기본 타입은 Java에서 기본적으로 제공하는 타입으로, int, long, float, double 등이 있습니다.
- 값이 직접 변수에 저장됩니다.

#### 참조 타입 (Reference Type):
- 참조 타입은 객체의 메모리 주소를 저장하는 변수입니다.
- 예를 들어, 클래스, 인터페이스, 배열 등이 참조 타입에 해당합니다.
- 참조 타입 변수는 실제 객체를 가리키는 포인터로, 객체의 메모리 주소를 저장합니다.

```java
String str = "Hello"; // 'str'은 String 객체를 참조하는 참조 변수
int[] arr = new int[10]; // 'arr'은 int 타입의 배열을 참조하는 참조 변수
```

물론입니다. Java에서 배열과 for문을 사용한 데이터 수정 방법, 그리고 얕은 복사와 깊은 복사에 대해 Markdown 형식으로 설명하겠습니다.

---

### 배열과 For문을 사용한 데이터 수정

#### For문을 사용하여 배열 데이터 수정:
배열의 각 요소를 순회하면서 데이터를 수정할 수 있습니다.

```java
int[] numbers = {1, 2, 3, 4, 5};

// For문을 사용하여 배열의 각 요소를 수정
for(int i = 0; i < numbers.length; i++) {
    numbers[i] = numbers[i] * 2; // 각 요소의 값을 두 배로 증가
}
```

#### 향상된 For문 (Enhanced For Loop):
Java 5 이상에서는 향상된 for문을 사용하여 배열 또는 컬렉션을 더 쉽게 순회할 수 있습니다. 단, 이 방법은 배열 요소를 수정할 때는 사용할 수 없습니다.

```java
for(int number : numbers) {
    System.out.println(number); // 배열의 각 요소를 출력
}
```

### 얕은 복사 (Shallow Copy) vs 깊은 복사 (Deep Copy)

#### 얕은 복사 (Shallow Copy):
- 얕은 복사는 객체의 주소만 복사하여, 원본과 복사본이 동일한 데이터를 공유합니다.
- 배열 예시:

```java
int[] original = {1, 2, 3, 4, 5};
int[] shallowCopy = original; // 얕은 복사
```

#### 깊은 복사 (Deep Copy):
- 깊은 복사는 객체의 실제 값을 새로운 메모리에 복사하여, 원본과 복사본이 완전히 독립적입니다.
- 배열 예시:

```java
int[] original = {1, 2, 3, 4, 5};
int[] deepCopy = new int[original.length];

// 배열 요소를 하나씩 복사
for(int i = 0; i < original.length; i++) {
    deepCopy[i] = original[i];
}
```

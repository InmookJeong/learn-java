# JDK 5

> <b>개요</b>
- _`JDK 5`_ 버전은 2024년 9월에 출시된 Java Development Kit입니다.
- JDK 5를 정확히 표현하자면 Java 2 Platform Standard Edition(J2SE) 5.0 Development Kit이라고 하며
- Product version을 기준으로 JDK 5.0, Developer version 기준으로 1.5.0이라고 불립니다.
- _`JDK 5`_ 버전이 출시되며 `Generics`, `향상된 for Loop`, `Autoboxing/Unboxing`, `Enum`, `Varargs`, `Static Import`, `Metadata` 등의 기능이 추가되었는데
- 각 기능이 어떤 역할을 하는지 알아보겠습니다.

### JDK 5 Structure
![JDK 5 Structure](./images/jdk5_structure.gif)

### Generics
- Collection에서 Element를 가져올 때 저장된 데이터의 타입에 맞게 가져와야 합니다.
- 기존에는 Element를 가져올 때 아래 `예시 1`과 같이 `개발자가 직접 Type Casting`을 해줬습니다.

    ```java
        /* 예시 1 */
        1 static void printElement(Collection c) {
        2    for(Iterator i = c.iterator(); i.hasNext();) {
        3        // 직접 TypeCasting
        4        String value = (String) i.next();
        5        System.out.println(value);
        6    }
        7 }
    ```
- 개발자들이 Collection에 어떤 데이터가 전달되는지 이미 알고있다면 `예시 1`과 같이 사용해도 됩니다.
- 하지만 신규 개발자가 Collection에 저장된 데이터의 타입을 모른다면?
- **아마 잘못된 TypeCasting을 하겠죠.**
- 신규 개발자가 `예시 1`의 4번줄 소스코드를 아래와 같이 변경했다고 가정하겠습니다.
    ```java
        int value = (int) i.next();
    ```
- Java에서는 value의 타입(int)과 Element(i.next())의 타입(int)만 확인하면 되기 때문에 개발 과정에서 에러가 발생하지 않습니다.
- 하지만 Collection 안에 저장된 Elemet의 데이터 타입은 `String`이기 때문에 Method가 실행되면 오류가 발생할 것입니다. (Run-time Error)
- 아마도 `Numberformatexception`이 발생하겠죠.
- 그럼 Collection 안에 저장된 Element의 데이터 타입을 `미리 알려준다면` 개발하는 과정에서 에러를 발견할 수 있지 않을까요? (Compile-time error)
- 이러한 역할을 하는 기능이 바로 `Generics`입니다.
- Generics는 Collection의 데이터 타입을 컴파일러에게 전달하고,
- 컴파일러는 Collection의 Generics가 알려준 데이터 타입으로 TypeCasting하여 Element를 가져옵니다.
- 그럼 더이상 개발자가 TypeCasting을 고민할 필요가 없겠죠?
- 즉, 데이터 타입에 대해 명확하고 안전한 소스코드를 작성할 수 있게 됩니다.
- Generics가 적용된 소스 코드는 아래 `예시 2`와 같이 작성할 수 있습니다.
    ```java
        /* 예시 2 */
        1 // <String>를 통해 문자열 c의 컬렉션임을 알 수 있다.
        2 static void printElement(Collection<String> c) {
        3    for(Iterator i = c.iterator(); i.hasNext();) {
        4        // Compiler가 TypeCasting하여 값을 가져온다.
        5        String value = i.next();
        6        System.out.println(value;)
        7    }
        8 }
    ```
- `예시 2`에서 작성한 것과 같이 `<>` 안에 데이터 타입을 작성해주면 Compiler가 알아서 TypeCasting을 합니다.
    - 참고로 `A<Type> b` 코드는 `A of Type b`라고 읽는다고 합니다.
    - `예시 2`의 1번줄에 작성한 것과 같이 `문자열 c의 Collection`이라고 읽는다고 하네요.
- Generics는 매개변수에만 사용할 수 있는 것은 아닙니다.
- 아래 `예시 3`과 같이 Method의 반환 타입으로도 사용할 수 있습니다.
- 또한 `예시 4`와 같이 반환할 데이터 타입을 매개변수로 전달받아 사용할 수도 있습니다.
    ```java
        /* 예제 3 */
        1 static List<String> getUserNames(...) {
        2    // 문자열 userNames의 List 생성
        3    // userNames는 문자열로 된 사용자 이름의 목록을 저장하는 List Collection입니다.
        4    List<String> userNames = new ArrayList<String>();
        5    
        6    // 사용자 이름 목록을 조회하는 기능 구현...
        7
        8    // List<String> 타입의 데이터를 반환합니다.
        9    return userNames;
        10 }

        /* 예제 4 */
        // Documentation에는 아래 주석과 같이 작성 예시 소스코드를 보여주고 있습니다.
        // <T extends Annotation> T getAnnotation(Class<T> annotationType); 
        static <T> List<T> getCustomTypeList(Class<T> c) {
            List<T> list = new ArrayList<T>();

            // 기능 구현...

            return list;
        }
    ```
- 그럼 Generics의 단점은 무엇일까요?
- 잘못 동작하는 레거시 코드와 같이 동작할 때 TypeCast가 실패할 수도 있다는 것입니다.
- 예를 들어 정수를 삽입하는 문자열 s가 있다고 가정하겠습니다.
- 정수의 값은 Generics에 의해 문자열로 TypeCasting을 시도하는데 데이터 타입이 맞지 않기 때문에 실패할 수 있습니다.
- 이때 java.util.Collections에서 제공하는 Wrapper Class를 활용하면 Run-time 시 안전성을 보장할 수 있습니다.
    ```java
        1 // 레거시 코드로 인해 TypeCasting에 실패할 수 있음
        2 Set<String> s = new HashSet<String>();
        3
        4 // 레거시 코드가 정수를 삽입하려고 시도하는 시점에서 ClassCastException을 발생시킵니다.
        5 // 이 때 결과 스택 추적을 통해 문제를 진단하고 복구할 수 있습니다.
        6 // 즉, Collections가 한 번 더 체크하기 때문에 에러에 대한 안전성을 확보할 수 있음
        7 Set<String> s = Collections.checkedSet(new HashSet<String>(), String.class);
    ```


### 참고
- JDK 5.0 Documentation : https://docs.oracle.com/javase/1.5.0/docs/
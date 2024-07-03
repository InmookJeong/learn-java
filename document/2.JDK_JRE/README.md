# JDK와 JRE

> <b>개요</b>
- 우리는 JAVA라는 프로그래밍 언어를 이용해 애플리케이션을 작성하여
- OS 또는 브라우저에서 애플리케이션을 실행할 수 있습니다.
- JAVA는 기계어가 아니라 사람이 이해하고 쉽게 사용할 수 있도록 고안된 프로그래밍 언어인데
- 어떻게 OS 또는 브라우저에서 실행이 가능한걸까요?
- 그 이유는 바로 JAVA 언어를 구성하고 있는 `Java Development Kit(JDK)`와 `JAVA Runtime Environment(JRE)`를
- 제공하고 있기 때문이죠!
- 이번에는 JDK와 JRE가 무엇이고 어떻게 동작하는지 알아보겠습니다.

### JDK란?

- JDK란 `Java Development Kit`의 약자로
- Java 개발자를 위한 Software를 의미합니다.
- 즉, Java 프로그래밍 언어를 이용하여 `애플리케이션을 작성할 수 있도록` 돕습니다.
- JDK는 다음 기능들을 포함하고 있습니다.
    - Java Interpreter
    - Java Classes
    - Java Development Tool
- 그 중 Java Development Tool은 아래 항목들을 포함하고 있죠.
   - Compiler
   - Debugger,
   - Disassembler
   - AppletViewer
   - Stub File Generator
   - Documentation Generator
- JDK에 포함되어 있는 기능들을 활용하여 만든 애플리케이션은
- JVM(Java Virtual Machine)에 의해 어디서든 실행(Run)할 수 있습니다.

> <b>JDK의 구조</b>

```
   ╋━━ ━ Java Development Kit ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━━╋
   |                                                                  |
   |  ╋━━ ━ Java Runtime Environment ━ ━ ━ ━━━╋                       |
   |  |                                       |                       |
   |  |   ╋━ ━ ━ Java Virtual Machine ━ ━ ╋   |                       |
   |  |   |                               |   |                       |
   |  |   |                               |   |                       |
   |  |   ╋ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ╋   |                       |
   |  |                                       |   +    Development    |
   |  |                   +                   |            Tool       |
   |  |                                       |                       |
   |  |            Library Classes            |                       |
   |  |                                       |                       |
   |  |                                       |                       |
   |  ╋━━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━━╋                       |
   |                                                                  |
   ╋━━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━ ━╋
```
- JDK의 Tool에는 아래 항목들도 포함되어 있습니다.
    - Javac
    - Javadoc
    - Jar
    - Security
    - monitoring
    - JConsole
    - JPDA
    - JVM TI
    - IDL
    - Java DB
    - Deployment
    - Web Service
    - TroubleShooting
    - etc.

### JRE란?

- JRE란 `Java Runtime Environment`의 약자로
- Class Library 및 특정 Java 프로그램을 `실행하는 데 필요한 리소스를 제공`합니다.
- JRE는 JDK에 포함되어 있고, JDK, JVM과 상호 연관된 컴포넌트입니다.
```
   JDK를 사용하여 Application 개발 ―――――――――――> JVM을 통해 Application 실행
                                      |
                                      |
                                      |
                        JRE가 JVM에서 실행할 때 필요한 ------사용자가 작성한 Source Code와 
                               Library를 제공               JRE의 Library(내장코드)를 결합
                                      &
                            결과 프로그램을 실행하는
                             JVM의 인스턴스를 작성
```

> <b>JRE의 동작 방법</b>
```
    Class Loader ―――> Byte Code Verifier ―――> Interpreter ―――> Run Time ―――> H/W
```
- Class Loader
    - 클래스 로더
    - Java 프로그램의 `실행에 필요한 모든 Class를 동적으로 로드`하는 역할을 수행합니다.
    - Java Class는 필요할 때에만 메모리에 로드되는데
    - JRE가 ClassLoader를 사용하여 요청되는 Class를 자동으로 로드해줍니다.
    - 대표적인 Class Loader는 다음과 같습니다.
        - Bootstrap Class Loader
        - Extensions Class Loader
        - System Class Loader

- Byte Code Verifier
    - 바이트 코드 검증기
    - 인터프리터에 전달되기 전에 `Java 코드의 형식과 정확성을 보장`해야 합니다.
    - 이 역할을 하는 것이 바로 바이트 코드 검증기입니다.
    - 바이트코드 검증기에서 코드가 시스템 무결성 또는 액세스 권한을 위반할 경우
    - Class가 손상된 것으로 간주되어 메모리에 로드되지 않습니다.
    - 참고로 JDK에 Java 코드를 바이트 코드로 변환하는 컴파일러(javac)가 있기 때문에
    - 바이트 코드 검증기가 검증을 할 수 있게 됩니다.

- Interpreter
    - 인터프리터
    - 바이트 코드가 메모리에 로드되면 Java 인터프리터는 프로그램이 시스템에서 실행될 수 있도록
    - `JVM 인스턴스를 작성`해줍니다.
    - 인터프리터는 어셈플리 코드를 한 줄씩 읽으며 다음 두 가지 작업을 수행합니다.
        - (1) 바이트 코드 실행 : _`Run Time`_
        - (2) 필요한 하드웨어(H/W)를 적절히 호출 : _`H/W`_

> <b>JRE의 구성요소</b>
- 개발 도구
    - Application 품질 개선에 사용할 수 있는
    - 사용자 인터페이스 도구 키트 등을 포함하고 있습니다.
        - Java 2D
        - Swing(GUI)
        - Abstract Window Toolkit(AWT)
            - 버튼, 창, 스크롤바 등 UI 객체 생성 시 사용되는 GUI

- 배포 솔루션
    - Java Web Start
        - 웹 브라우저에서 클릭 한 번으로 모든 기능을 갖춘 애플리케이션을 시작할 수 있습니다.
    - Java Plugin
        - 웹 애플릿을 실행할 수 있도록 브라우저와 Java 플랫폼 간의 연결을 설정합니다.

- 언어 및 유틸리티 라이브러리
    - Java 클래스 파일의 모음을 패키지라고 합니다.
    - JRE에는 버저닝, 관리 및 모니터링을 지원하는 여러 패키지가 포함되어 있습니다.
        - 컬렉션 프레임워크
            - 애플리케이션 데이터의 저장 및 처리 개선을 위한 인터페이스가 포함되어 있습니다.
        - Concurrency Utilities
            - 고성능 Threading 유틸리티를 포함하고 있는 프레임워크 패키지입니다.
        - Preferences API
            - 동일한 시스템에 있는 여러 사용자가 자신만의 애플리케이션 기본 설정 그룹을 정의할 수 있습니다.
        - 로깅
            - 보안 실패, 성능 문제, 구성 오류 등 문제 해결을 위한 로그 보고서를 생성합니다.
        - Java 아카이브(JAR)
            - JAR는 플랫폼에 독립적인 파일 형식입니다.
            - 열 파일을 번들로 묶어 애플리케이션의 크기를 줄이고 다운로드 속도를 향상시켜 줍니다.

- 통합 라이브러리
    - 서비스와 애플리케이션 사이에서
    - 원활히 데이터를 연결시켜주는데 도움이 되는 라이브러리입니다.
        - Java IDL
            - Java Interface Definition Language(IDL)의 약자로,
            - Common Object Request Broker Architecture(CORBA)를 기반으로 만들어졌습니다.
            - Java IDL은 네트워크를 통해 서로 다른 플랫폼에서 상호 작용을 하는 객체(분산 데이터 객체)를 지원합니다.
            - 예를 들어 Java로 작성된 객체가 C, C++ 등 다른 언어로 작성된 객체와 상호 작용을 할 수 있습니다.
        - Java Database Connectivity(JDBC)
            - JDBC API를 사용하여 데이터베이스, 스프레드시트, 파일 등에 접근할 수 있습니다.
        - Java Naming And Directory Interface(JNDI)
            - 클라이언트가 이름 지정 규칙을 사용하여 외부 데이터베이스에서 정보를 가져와 호환 가능한 애플리케이션을 만들 수 있도록 지원합니다.

### 참고
- JDK
    - [Java Development Kit - IBM Documentation](https://www.ibm.com/docs/en/i/7.4?topic=platform-java-development-kit)
    - [자바의 JDK - GeeksforGeeks](https://www.geeksforgeeks.org/jdk-in-java/)
    - [Java Development Kit - Wikipedia](https://en.wikipedia.org/wiki/Java_Development_Kit)
- JRE
    - [JRE(Java Runtime Environment)란? - IBM Topics](https://www.ibm.com/kr-ko/topics/jre)
    - [Java 런타임 환경(JRE)이란 무엇인가요? - AWS 개발자 센터](https://aws.amazon.com/ko/what-is/java-runtime-environment/)
    - [What is JRE? - Javapoint](https://www.javatpoint.com/java-jre)
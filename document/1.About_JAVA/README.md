# About JAVA

### JAVA란?

> <b>개요</b>
- JAVA는 컴퓨터 프로그래밍 언어 중 하나입니다.
- 1995년 썬 마이크로시스템즈(Sun Microsystems)의 제임스 고슬리(James Gosling)에 의해 처음으로 만들어 졌습니다.
- 처음에는 가전제품용 프로그램을 기밸하기 위해 만들어졌지만
- 현재는 웹 애플리케이션, 모바일 애플리케이션 등을 개발하는데 많이 사용되고 있습니다.

> <b>그럼 굳이 왜 JAVA라는 언어를 만들었을까?</b>
- 가전제품에 내장되는 프로그램은 주로 C언어를 사용합니다.
- 제품의 특성에 맞는 기능만 구현하면 되기 떄문에 적은 메모리로 실행이 가능하도록 만들어야 하기 때문이죠.
- 이 점에서 C언어는 JAVA보다 효율적인 프로그래밍 언어입니다.
- 그럼 왜 JAVA를 만들었을까요?

    > JAVA는 모든 플랫폼에서 실행이 가능한 언어이기 때문입니다.  
    - JAVA의 General Purpose : Write once, run anywhere (WORA)
    - Windows, MacOS, Linux 등 프로그램이 실행되는 환경, 즉 플랫폼에 따라 개발 방법이 달라집니다.
    - 하지만 JAVA는 플랫폼(실행 환경)에 영향을 받지 않고 어디서나 프로그램을 실행시킬 수 있죠.
    - 이런 일이 어떻게 가능할까요?
    - 바로 JAVA는 JVM(Java Virtual Machine)을 제공하기 때문이죠.
    - JVM(Java Virtual Machine)은 컴파일된 JAVA 소스코드를 바이너리 코드(기계어)로 변환해줍니다.
    - 이 때 설치된 플랫폼의 환경을 고려하여 변환해주죠.
    - 그렇기 때문에 JAVA로 프로그패밍을 하면 어느 플랫폼에서든 실행이 가능하게 됩니다.
    
    > JAVA는 객체 지향 언어이기 때문입니다.
    - JAVA는 클래스 기반의 객체 지향 언어(Object-Oriented Programming Language; OOP)입니다.
    - 한 번 소스코드를 작성하면 다른 클래스(JAVA 소스코드)에서 필요한 기능을 호출하여 사용할 수 있도록 기능을 제공합니다.
    - 즉, 같은 기능을 하는 소스코드를 각 클래스 별로 구현할 필요가 없다는 의미입니다.
    - 이렇듯 JAVA는 객체 지향적 특성을 통해 `재사용`이 가능한 소스코드를 작성하여 효율적으로 개발할 수 있도록 환경을 제공합니다.

### License
- GPL-2.0

### Java EE / ME / SE
- Java EE
    - Enterprise Application을 개발하기 위해 사용하는 환경(Environment)
    - JavaEE를 이용하여 서버(Server) 개발 가능
- Java ME
    - Mobile Application을 개발하기 위해 사용하는 환경(Environment)
- Java SE
    - Desktop Application을 개발하기 위해 사용하는 환경(Environment)

### Java Version

버전|Release 날짜|특징
---|---|---
JDK Beta|1995|Java first release
JDK 1.0|1996. 01|정식 버전 Release
JDK 1.1|1997. 02|Java Beans<br/>JDBC<br/>RMI<br/>직렬화
JDK 1.2|1998. 12|Swing GUI API<br/>JVM에 JIT 컴파일러 탑재<br/>Java IDL<br/>Collection Framework
JDK 1.3|2000. 05|자바 플랫폼 디버거 아키텍쳐(JPDA)<br/>합송 프록시 클래스
JDK 1.5|2004. 09|Generic<br/>Metadata(Annotation)<br/>Autoboxing/unboxing<br/>Enum<br/>Varargs<br/>향상된 for문<br/>다중 Thread<br/>Scanner Class
JDK 7|2011. 07|try-statement(try-with-resources)의 자동 리소스 관리<br/>Instance 생성을 위한 향상된 유형 추론(다이아몬드 연산자 <>)<br/>간소화 된 Varargs 메서드<br/>이진 정수 리터럴<br/>새로운 파일 I/O 라이브러리
JDK 8|2014. 03|LTS(Long Term Support) Version<br/>Rambda<br/>Stream<br/>Optional
JDK 10|2018. 03|var 키워드 도입
JDK 11|2018. 10|LTS(Long Term Support) Version<br/>HttpClient Class<br/>Collection.toArray()
JDK 17|2021. 10|LTS(Long Term Support) Version<br/>Text Block<br/>Sealed Class<br/>Switch문 표현식<br/>Stread.toList()
JDK 21|2023. 10|LTS(Long Term Support) Version
JDK 22|2024. 03|가장 최신 버전
<div style="text-align:center;">
    <img src="./images/java_logo.png" alt="Java Logo" width="200" height="200">
</div>

# # 개요

- Java는 **프로그래밍 언어**의 한 종류로, 1995년 '썬 마이크로시스템즈'의 '제임스 고슬링(James Arthur Gosling)'이 개발한

- 객체지향 프로그래밍 언어입니다.

- 처음에는 가전제품에 탑재할 프로그램을 만들기 위해 개발하였지만

- 현재는 웹 애플리케이션을 개발하는데 많이 사용되고 있어요.

- 그리고 안드로이드 등 모바일 앱도 Java를 이용해 개발할 수 있답니다.

<br/><br/>

# # 라이선스

- Java 언어 자체는 GPL 라이선스이기 때문에 무료로 사용할 수 있어요.

- 하지만 Java 언어로 애플리케이션을 개발하려면 JDK(Java Development Kit)를 꼭 설치해야 하는데,

- 이 JDK를 소유하고 있는 기업(단체)에 따라 라이선스가 달라져요.

- JDK는 크게 Oracle JDK와 OpenJDK로 나눌 수 있는데요.


<div style="text-align:center;">
    <img src="./images/oracle_logo.png" alt="Oracle Logo" width="200" height="200">
</div>

- 2010년, 오라클이 썬 마이크로시스템즈를 인수하였고 2019년부터 유료화 정책을 시행하면서

- JDK에 BCL 라이선스를 적용하였어요.

- 물론 개인 학습이나 테스트 목적으로 JDK를 이용할 때에는 무료로 사용할 수 있지만 기업의 애플리케이션을

- 개발하거나 상용화할 때에는 유료 라이선스를 구입해야 돼요.

    - 참고로 JDK 8U202 버전까지는 용도와 상관없이 무료로 사용할 수 있습니다.

<br/><br/>

<div style="text-align:center;">
    <img src="./images/open_jdk_logo.png" alt="OpenJDK Logo" width="200" height="80">
</div>

<br/><br/>

- 반면 OpenJDK는 이름에서 알 수 있듯이 자유롭게 사용할 수 있도록 공개되어 있어요.

- 초창기 썬 마이크로시스템즈가 제공한 것과 같이 GPL v2 라이선스를 적용하여

- 기업의 애플리케이션을 개발하거나 상용화할 때에도 무료로 사용할 수 있죠

- 요즘 기업용 애플리케이션을 만들 때 OpenJDK를 많이 사용한답니다.

<br/><br/>

# # 분류

### Java SE(Standard Edition / J2SE)

- Java의 표준 에디션으로,

- 핵심 API와 기능을 제공합니다.

<br/>

### Jakarta EE(Java EE / Java Enterprise Edition / J2EE)

- 기업에서 운영하는 서버 페이지에 특화된 에디션으로,

- JSP와 서블릿을 비롯한 웹 애플리케이션 서버에 관련된 기술들을 제공합니다.

<br/>

### Java ME(Java Micro Edition / J2ME)

- 피처폰, PDA, 셋톱 박스, 센서 등 임베디드 시스템 환경에 특화된 경량 에디션입니다.

<br/><br/>

# # Java의 장점

### 객체 지향(Object Oriented)

- 객체별로 코드를 작성하고 객체들을 조합하여 전체 프로그램을 완성합니다.

- 코드를 재상용하기 쉬워, 빠르고 신뢰성 있는 프로그램을 만들 수 있습니다.

<br/>

### 플랫폼에 독립적

- Java의 가장 큰 장점은 플랫폼에 독립적이라는 점입니다.

- Java 언어로 작성된 프로그램을 '컴파일러'가 바이트코드로 변환하고,

- JVM(Java Virtual Machine)이라는 가성머신을 통해 실행됩니다.

- CPU나 운영체제의 종류에 상관없이 JVM을 설치할 수 있다면 Java 프로그램은 어디서든 실행할 수 있습니다.

<br/>

### ☆ Write Once, Run Every Where! ☆
 
<br/><br/>

### 분산 환경 지원

- TCP/IP, HTTP, FTP 같은 프로토콜을 처리할 수 있는 라이브러리를 가지고 있어

- 네트워크와 관련된 프로그램을 개발할 수 있습니다.

<br/>
 
### 멀티스레딩 지원

- Java은 언어 수준에서 멀티스레딩(Multi-threading)을 지원하기 떄문에 효율적인 프로그램을 작성할 수 있습니다.

- 멀티스레딩은 많은 작업을 동시에 할 수 있다는 의미입니다.

<br/><br/>

# # Java의 단점

### 성능 저하

- Java는 JVM(Java Virtual Machine) 위에서 실행되므로, C나 C++ 같은 언어에 비해 실행 속도가 느립니다.

<br/>

### 높은 메모리 사용량

- Java의 가비지 컬렉션(GC) 기능은 자동으로 메모리를 관리하지만

- 이로 인해 CPU 자원을 사용하게 되어 메모리 사용량이 증가합니다.

<br/><br/>

물론 하드웨어의 성능이 발전하면서 실행 속도나 메모리 사용량이 프로그램을 실행하는데 큰 문제가 되지 않지만,

C언어와 같은 저수준의 언어와 비교하면 상대적으로 느리고 자원을 많이 사용한다는 의미에요.

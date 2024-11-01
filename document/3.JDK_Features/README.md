# JDK 버전 별 특징

> <b>개요</b>
- 실무를 경험하면서 여러 JDK 버전을 사용했습니다.
- 학교 과제를 할 때에는 _`JDK 5`_ 버전을, 취업 이후에는 _`JDK 7`_, _`JDK 8`_, _`JDK 17`_ 을 사용하고 있죠.
- 생각해보니 2014년에 릴리즈된 _`JDK 8`_ 을 2021년까지 사용하고 있었네요.
- _`JDK 17`_ 은 2022년 하반기에 이직하면서 처음 접했는데 지금까지 사용하고 있고요.
- 그럼 왜 구 버전의 JDK를 그렇게 오래 사용한 것일까요?
- 실무에는 초기에 프로젝트를 시작할 때 JDK 버전을 결정합니다.
- 당시의 최신 JDK 또는 가장 안정적인 JDK 버전을 선택하여 프로젝트를 시작하게 되죠.
- 시간이 지나도 프로젝트가 안정적으로 동작하면 JDK 버전을 굳이 업그레이드하지 않아요.
- 하지만 구 버전의 JDK는 언젠간 버그나 보안 이슈에 대한 수정이 중단됩니다.
- 그때 다시 최신 버전 또는 가장 안정적인 버전의 JDK를 선택하여 업그레이드를 해야하죠.
- 그럼 지금까지 JDK 버전을 변경하여 사용할 때마다 제공하는 기능을 모두 이해하며 사용했을까요?
- **아니었습니다.**
- 최신 버전의 JDK를 사용하더라도 익숙한 문법을 주로 사용할 뿐 변경 또는 추가된 기능은 많이 활용하고 있지 않더라고요.
- 그렇기 때문에 이번 학습에서는 그동안 사용해본 JDK들을 기준으로 버전 별 특징에 대해 알아보려고 합니다.
- 물론 필요하면 사용해보지 않은 JDK 버전의 특징에 대해서도 알아보겠습니다.
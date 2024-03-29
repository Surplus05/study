# Micro Service Architecture

쇼핑몰을 예시로 들어 보자.

회원과 관련된 기능, 상품과 관련된 기능, 주문과 관련된 기능 등 모든 기능이 하나의 서버에서 호출되어 동작하게 된다.

개발이나 환경설정이 간단하다는 장점이 있다.  
갑자기 주문량이 폭주하는 경우, 다른기능까지 영향을 미칠 수 있다.  
확장하려 해도, 전체를 확장해야 한다.

반면, 모듈화시켜 각 기능을 자체 서비스로 구축하는것이 MSA이다.  
의존관계가 더 적고 유연하다고 할 수 있다.  
각 기능들은 서비스 형태로 구현되며, API 를 통해 타 서비스와 통신하게 된다.  
독립적으로 배포되며 독립되어 있기에 부분확장이 가능하다.  
하나의 서비스가 먹통이 되는 경우, 다른 서비스에 영향이 미치지 않으며, 재사용성이 높다.

장점만 존재하는것은 아닌데, API통신을 하기 때문에 속도가 느릴 수 있으며 트랜잭션이 어려울 수 있다.

또한 모든것이 독립적이기 때문에 인터페이스를 신중하게 처리해야 하며, 의존 서비스가 동작하지 않을 경우를 대비해야 한다.

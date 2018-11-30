세션 발표자 -  신호석(카카오/소프트웨어 엔지니어)

url shortener 는 url 숏컷

goo.gl 2019 종료

나온이유
* squeeze a long URL info fewer characters to make is easier

성격
* Stability - 안정성
* Security - 보안
* Speed - 원 주소에 대한 원복과정의 속도가 일정 수준이상이 되어여 한다.

goo.gl로는 부족한 트래킹을 보완하기 위해 SNAKER라는 프로젝트를 진행

hash와 실제 url을 매핑한다
id, hash, long url, description, createAt

플랫폼에 따른 레코드를 생성하여 플랫폼별로 분기를 만들어 줄수 있다.
Django User agent정보 확인

사용자 정보 또한 request META 정보를 이용하여 저장.

Operating Server, Redirect Server 별도 운영 필수
장고 서버 인프라가 바인딩이 되어있을경우 서버가 흔들릴수 있다. (서버의 인프라 장비를 사용)
그렇기 때문에 서비스는 나누어야 한다.

Redirect 기능은 일정 수준이 넘으면 부하가 발생할 가능성이 있음
그래서 ORM을 사용할떄 Cache를 활용해 조회 및 저장을 해야한다.

Pipenv - 패키지 관리와 가상 환경을 같이 관리 하자!
가상환경을 셋팅해놓고 라이브러리를 설치 하면 자동으로 관리를 해준다.
서비스 레벨에 따른 분리가 가능한가? 가능

Pinject - Django Server 아키텍처에서 MTV 패턴 골조가 기본
위 패턴을 기본으로 DI(Depndency Injection)를 통한 의존성 제거를 하는것이 좋다.
비즈니스 로직을 뷰와 완전히 분리 시키는 라이브러리
테스트 코드를 사용할 경우 해당 비즈니스 로직만 따로 사용 가능하다.

Pytest-Django - Service를 기본으로 테스트 진행 or 하단의 feature에 대해서도 테스트 진행 가능
url요청, db테스트 진행 가능

장고 유저 클러스터링 에 대한 성능
요청이 일정 수준이상 넘어가면 병목 현상이 일어 나게 된다.
체크해야 할것
- 디비에 대한 병목
- 로직상의 병목 체크
- 인프라를 비싸게!

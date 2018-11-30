Django의 배신(주니어 개발자의 Django 삽질기) - 김은향

1. ORM 블랙홀

한컬럼을 걔산할 경우 aggregate을 사용하여 계산 가능
Case와 When을 이용하여 annotate를 이용하여 특정 기준을 이용하여 계산을 할 수 있다.

foreignKey - selected_related
m2m - prefetch_related


3. Transaction - celery

트랜잭션을 사용할 경우 중간에 셀러리의 테스크가 존재 하면 트랜잭션이 실패한다.

트랜잭션을 사용할 경우 걸려 있는 쿼리들을 다 실행한후에 디비에 커밋한다

테스크가 중간에 있는 경우 데이버테이스에 물리적인 데이터가 없기때문에 실패 한다.

on_commit이라는 트랜잭션 훅을 이용하여 트랜잭션 커밋이 다 끝난후 셀러리 테스크가 작동하도록 할 수 있다.


4. New Django

csrf - 유저 - 로그인 - 서버 - csrf토큰 반환 - 이후 서버에서 폼을 렌더하고 요청은 csrf토큰을 같이 보냄

ajax - X-CSRFToken으로 확인

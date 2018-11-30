DB와 ORM에 관한 7가지 고민 - 김찬우

sludeshare bit.ly/devdjango-2018-ed

1. ORM을 왜쓸까?

퍼포먼스 병목 요인 - DB I/O

1. joins, Aggregation, Indexes... 겉할기
2. 데이터 엔지니어와의 소통 힘듬, 다른 스택 개발자들과의 소통 힘듬.

ORM 스키마 괜찮은가?

이름짓기.

규칙
항상 테이블 과 인덱스 이름 지정하기
항상 m2m 중간 테이블 지정하기
스트링 인코딩, 테이블, 칼럼 코멘트, ...

ForeignKey는 뭘까?


---
* CrossDatabase
Database Router

hints를 사용하지 않게
ConncetionRuter()에서 instance힌트를 사용하지 않도록

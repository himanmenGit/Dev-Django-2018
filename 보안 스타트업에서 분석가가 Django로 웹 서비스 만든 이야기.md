보안 스타트업에서 분석가가 Django로 웹 서비스 만든 이야기

admin inspectDB User

inspectDB사용시 주의점

managed = false를 할경우 readonly가 되어 데이터가 저장되지 않는다

class Meta:
    managed = False # 없애서 데이터 베이스 접근을 하게 한다.


테스트 & 배포

일정... ㅜㅜ

모델 테스트 - 일반 장고 문서 테스트
클라이언트 테스트 - 뷰에 대한 테스트
보안성 테스트 -

sql injection 방어 오픈 소스 vega

DB Routing 두개의 데이터 베이스를 쓰는 django 기능

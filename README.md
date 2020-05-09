# 지하철 정보 관리

## 지하철 노선 관리 기능 시나리오
```
Feature: 지하철 노선 관리

  Scenario: 지하철 노선을 관리한다.
    When 지하철 노선 n개 추가 요청을 한다.
    Then 지하철 노선이 추가 되었다.
    
    When 지하철 노선 목록 조회 요청을 한다.
    Then 지하철 노선 목록을 응답 받는다.
    And 지하철 노선 목록은 n개이다.
    
    When 지하철 노선 수정 요청을 한다.
    Then 지하철 노선이 수정 되었다.

    When 지하철 노선 제거 요청을 한다.
    Then 지하철 노선이 제거 되었다.
    
    When 지하철 노선 목록 조회 요청을 한다.
    Then 지하철 노선 목록을 응답 받는다.
    And 지하철 노선 목록은 n-1개이다.
```

## 미션 요구사항
 - [x] 인수 테스트(LineAcceptanceTest) 성공 시키기
 - [x] LineController를 구현하고 인수 테스트에 맞는 기능을 구현하기
 
###  지하철 노선
 - [x] 페이지 호출 시 미리 저장한 지하철 노선 조회
 - [x] 지하철 노선 목록 조회 API 사용
#### 노선 추가
 - [x] 지하철 노선 이름은 중복될 수 없다.
 - [x] 노선 추가 버튼을 누르면 아래와 같은 팝업화면이 뜸
 - [x] 노선 이름과 정보를 입력
 - [x] 지하철 노선 추가 API 사용
 - [ ] 비어있는 값으로 추가 시 추가 불가능
 - [ ] DB에 create/update 시간 자동 생성
 - [ ] 리스트에 id 노출시키지 않기
 #### 노선 상세 정보 조회
 - [x] 목록에서 노선 선택 시 상세 정보를 조회
 #### 노선 수정
 - [x] 목록에서 우측 수정 버튼을 통해 수정 팝업화면 노출
 - [x] 수정 팝업 노출 시 기존 정보는 입력되어 있어야 함
 - [x] 정보 수정 후 지하철 노선 수정 API 사용
 - [ ] 수정 불가능한 항목(노선 이름, 색상) 막아두기
 #### 노선 삭제
 - [x] 목록에서 우측 삭제 버튼을 통해 삭제
 - [x] 지하철 노선 삭제 API 사용
 - [ ] 잘못된 id일 경우 예외 처리
 
 ### 지하철 노선별 지하철역
 
 ####  지하철 노선에 역 추가
 - [ ] `이전역과의 거리`, `이전역과의 소요시간` 이 추가되어야 함
 
 #### 지하철 노선에 역 제거

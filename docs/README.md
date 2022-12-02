# 지하철 노선도 미션
## 기능 목록
### 역 관리
- [ ] 지하철 역을 등록할 수 있다.
- [ ] 현재까지 등록된 지하철 역을 조회할 수 있다.
- [ ] 지하철 역을 삭제할 수 있다.
  - 다만, 역 삭제는 삭제하려는 역이 어떤 노선에도 포함되어 있지 않은 경우에만 가능하다.

### 노선 관리
- [ ] 새로운 노선을 등록할 수 있다.
  - 상행 종점역을 입력받는다.
  - 하행 종점역을 입력받는다.
    - 상행 종점역과 하행 종점역은 이미 등록된 역이어야 한다.
- [ ] 등록된 노선을 조회할 수 있다.
- [ ] 노선을 삭제할 수 있다.
  - 노선을 삭제한다고 역이 삭제되는 것은 아니다.

### 구간 관리
- [ ] 구간을 등록할 수 있다. (= 구간을 등록한다는 것은 노선에 역을 추가한다는 것이다.)
  - 노선을 입력받는다.
  - 추가할 역을 입력받는다.
  - 순서를 입력받는다.
    - 순서는 1부터 시작한다.
- [ ] 구간을 삭제할 수 있다. (= 구간을 삭제한다는 것은 노선에서 역을 제거한다는 것이다.)

### 지하철 노선도 출력
- [ ] 모든 노선과 그 노선에 포함되어 있는 역을 출력한다.



## 예외 상황



## 기능 요구사항
1. 초기 설정
프로그램 시작 시 역, 노선 등 필요한 정보를 미리 셋팅할 수 있다.
아래의 사전 등록 정보로 반드시 초기 설정을 하기

```md
1. 지하철역으로 교대역, 강남역, 역삼역, 남부터미널역, 양재역, 양재시민의숲역, 매봉역이 등록되어 있다.
2. 지하철 노선으로 2호선, 3호선, 신분당선이 등록되어 있다.
3. 노선에 역이 아래와 같이 등록되어 있다.(왼쪽 끝이 상행 종점)
- 2호선: 교대역 - 강남역 - 역삼역
- 3호선: 교대역 - 남부터미널역 - 양재역 - 매봉역
- 신분당선: 강남역 - 양재역 - 양재시민의숲역
```

2. 지하철 역 관련 기능
- 지하철 역을 등록하고 삭제할 수 있다. (단, 노선에 등록된 역은 삭제할 수 없다)
- 중복된 지하철 역 이름이 등록될 수 없다. 
- 지하철 역 이름은 2글자 이상이어야 한다. 
- 지하철 역의 목록을 조회할 수 있다.

3. 지하철 노선 관련 기능
- 지하철 노선을 등록하고 삭제할 수 있다. 
- 중복된 지하철 노선 이름이 등록될 수 없다. 
- 지하철 노선 이름은 2글자 이상이어야 한다. 
- 노선 등록 시 상행 종점역과 하행 종점역을 입력받는다. 
- 지하철 노선의 목록을 조회할 수 있다.

4. 지하철 구간 추가 기능
- 지하철 노선에 구간을 추가하는 기능은 노선에 역을 추가하는 기능이라고도 할 수 있다.
  - 역과 역사이를 구간이라 하고 이 구간들의 모음이 노선이다.
- 하나의 역은 여러개의 노선에 추가될 수 있다. 
- 역과 역 사이에 새로운 역이 추가 될 수 있다. 
- 노선에서 갈래길은 생길 수 없다.

5. 지하철 구간 삭제 기능
- 노선에 등록된 역을 제거할 수 있다. 
- 종점을 제거할 경우 다음 역이 종점이 된다. 
- 노선에 포함된 역이 두개 이하일 때는 역을 제거할 수 없다.

6. 지하철 노선에 등록된 역 조회 기능
- 노선의 상행 종점부터 하행 종점까지 연결된 순서대로 역 목록을 조회할 수 있다.
# 프로젝트6 : Retail Transaction Data Dashboard

# 1. Overview

## 1.1. 문제 정의 및 목적

### 문제
- 지역별 매출 비교나 순위, 매출 규모 등 전반적인 동향 파악을 위한 모니터링 어려움
- 지역별 회원 여부, 쿠폰 사용 여부에 따른 효과를 파악하고 이를 비교하기 어려움

### 목적
- **지역별 소매업 동향, 멤버십 효과 등을 파악할 수 있는 대시보드 제작**

## 1.2. 데이터 소개
- vgames2.csv : 2016년 까지의 게임 정보와 출고량을 나타내는 데이터셋
- 16598 rows × 9 columns

### Columns Description
- transaction_date : 거래 일자
- transaction_hour : 거래 시간
- location_state : 상점 위치(주)
- location_city : 상점 위치(도시)
- rewards_number : 회원 번호
- rewards_member : 멤버십 가입 여부
- num_of_items : 상품 수량
- coupon_flag : 쿠폰 사용 여부
- discount_amt : 할인 금액
- order_amt : 거래 금액

## 1.3. 스킬셋
- pandas
- numpy
- tableau

---
# 2. 데이터 전처리
- 컬럼 데이터타입 변경
- 회원 여부, 쿠폰 사용 여부를 나타내는 부울형 컬럼의 결측치는 자료에 맞게 'False', 'No'등으로 대체

---
# 3. 대시보드 제작
- 대시보드 : https://public.tableau.com/app/profile/yeeoonoo/viz/Retail_16868993295590/1

## 기능
- 지역별 매출 규모 파악 및 시간에 따른 매출 추이 확인
- 지역별 회원 규모 파악 및 멤버십과 쿠폰 효과 분석

### 지역별 매출 규모 파악 및 시간에 따른 매출 변화 확인
- 먼저 맵 차트를 통해 지역별 매출 규모를 대략적으로 파악 가능
![image](https://github.com/yeeoonoo/project6/assets/110115061/648e64d2-2d05-4c9b-9f56-83d92aa8c115)

- 주단위 매출 규모 비율을 확인할 수 있는 파이차트를 클릭하면 해당 지역 전체 매출과 회원 수 확인 가능
![image](https://github.com/yeeoonoo/project6/assets/110115061/1557cf1a-6525-49e1-9c11-5ba57eeff3c2)
  - 현재는 플로리다 주의 매출 규모가 가장 크고, 회원 수도 많은 것을 확인할 수 있음

- 좌측 막대차트로 도시 단위 매출 순위를 원하는 숫자만큼 확인할 수 있음
![image](https://github.com/yeeoonoo/project6/assets/110115061/30d38f86-6921-4046-93f7-3d99a1e4ef16)

- 가장 매출이 높은 Atlanta 막대를 클릭하면 맵차트 아래 라인차트로 월별, 시간별 매출 추이를 확인할 수 있음
![image](https://github.com/yeeoonoo/project6/assets/110115061/bcfde0d7-3182-44ca-9efe-d4ab6a8d0b92)
  - Atlanta의 경우 19년 11월, 20년 2, 4, 6월의 매출이 낮음을 확인 가능. 원인 파악과 함께 보완책 마련이 필요함을 알 수 있음
  - 또 시간대로 보았을 때 오후 2시가 매출이 가장 낮고 오후 5시 경 매출이 가장 높다는 것을 확인할 수 있음


### 지역별 회원 규모 파악 및 멤버십과 쿠폰 효과 분석
- 도시 단위 회원 수 순위도 마찬가지로 원하는 숫자만큼 확인할 수 있음 \
![image](https://github.com/yeeoonoo/project6/assets/110115061/ac603d45-0be2-4e67-ab39-0083e4f2c6c6)

- 막대차트에서 선택한 도시의 멤버십과 쿠폰이 매출에 미치는 효과를 라인차트로 확인할 수 있음
![image](https://github.com/yeeoonoo/project6/assets/110115061/e5965c7b-a84b-4124-b041-3697e818223a)
  - 선택한 Atlanta의 경우 19년 12월, 20년 7, 9월을 제외하면 비회원의 평균 매출이 더 큰 것을 확인 가능
  - 또 쿠폰 사용 여부에 따른 평균 매출은 19년 말과 20년 3, 6, 8월에 격차가 큰 것을 확인 가능. 시즌에 따른 이벤트 효과로 파악됨

- 막대차트에서 선택한 도시의 멤버십과 쿠폰이 매출에 미치는 효과 시간대로도 확인 가능
![image](https://github.com/yeeoonoo/project6/assets/110115061/3745d0a2-833c-42fd-a412-985cc8af94ad)
  - Atlanta는 오후 5시와 오후 8시에 회원 평균매출이 가장 크다는 것을 알 수 있음. 이외는 비회원의 매출도 상당함



---
# 5. 결론 및 한계
- 데이터에 비용 정보가 없어서 매출로 따른 수익을 확인할 수 없음
- 쿠폰을 어떤 기준으로 발급했는지, 멤버십에 따른 혜택에 대한 정보가 데이터에 없어서 추가적인 마케팅 분석이 불가했음
- 하지만 소매업 매출 동향을 전반적으로 확인할 수 있도록 반응형 대시보드를 구성해볼 수 있는 좋은 경험이었음

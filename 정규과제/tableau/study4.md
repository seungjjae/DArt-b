# Fourth Study Week

- 30강: [계층](#30-계층)

- 31강: [집합](#31-집합)

- 32강: [결합집합](#32-결합집합)

- 33강: [계산된 필드](#33-계산된-필드)

- 34강: [행수준계산](#34-행수준계산)

- 35강: [집계계산](#35-집계계산)

- 36강: [테이블계산](#36-테이블계산)

- 37강: [퀵테이블계산(1)](#37-퀵테이블계산1)

- 38강: [퀵테이블계산(2)](#38-퀵테이블계산2)

- [문제1](#문제-1)

- [문제2](#문제-2)

- [문제3](#문제-3)

## Study Schedule

| 강의 범위     | 강의 이수 여부 | 링크                                                                                                        |
|--------------|---------|-----------------------------------------------------------------------------------------------------------|
| 1~9강        |  ✅      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=84)       |
| 10~19강      | ✅      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=75)       |
| 20~29강      | ✅      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=65)       |
| 30~38강      | ✅      | [링크](https://youtu.be/e6J0Ljd6h44?si=nhGbB7GsdOCqj15f)       |
| 39~49강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=45)       |
| 50~59강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=35)       |
| 60~69강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=25)       |
| 70~79강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=15)       |
| 80~89강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=5)        |

<!-- 여기까진 그대로 둬 주세요-->

> **🧞‍♀️ 오늘의 스터디는 지니와 함께합니다.**


## 30. 계층
- 뷰에서 데이터를 'DRILL DOWN'해 값을 세부적으로 찾을 때 유용한 방법이다.  
- 드래그를 통해 변수들 간 계층을 생성할 수 있다.  
- 상위 계층의 데이터버튼을 눌러 하위계층을 자동으로 생성해 데이터를 거시적으로 볼 수 있다.
- 아래는 지역변수들을 합쳐 '위치' 계층을 만든 것이다.
![image](https://github.com/user-attachments/assets/2c0590f8-0f04-494c-b8bd-a0cceedb34bd)

<!-- 계층 구조와 관련된 개념, 사용 방법 등을 적어주세요. -->


## 31. 집합
![image](https://github.com/user-attachments/assets/f727caca-96c4-4271-81b2-622174739bfc)
- 일반탭: 수동으로 데이터를 선택해 묶을 수 있다.  
- 조건탭: 사용자가 설정한 조건이 충족되면 데이터들을 묶어준다.  
- 상위탭: 필드 기준 별로 상위 또는 하위 순서로 데이터를 묶어준다.  
- 색상을 통해 집합 포함 여부를 판단할 수 있다.  
![image](https://github.com/user-attachments/assets/76cd1a70-e410-46c9-89cc-97f16ba49bf9)
<!-- 집합의 정의 및 활용 방법에 대해 알게 된 점을 적어주세요. -->
## 32. 결합집합
- 지정한 조건을 따라 데이터를 구분할 수 있다.EX) 두가지 조건의 집합  
![image](https://github.com/user-attachments/assets/0cfebfbf-0522-46ce-82ac-667702ca57d2)  
먼저 두가지 집합을 통해 각각의 조건을 가지게 만든다. 여기선 매출이 오만이상 수익이 만오천 이상을 각각 집합으로 만들었다.   
![image](https://github.com/user-attachments/assets/2b86d7cd-0901-41e4-85c3-888d2a846723)  
이후 결합집합을 수행하는데 여기서 INNER JOIN, OUTER JOIN ,LEFT JOIN, RIGHT JOIN을 정할 수 있다. 이를 통해 또는, 그리고 와 같이 결합 조건을 정할 수 있다.  
<!-- 결합집합의 개념 및 사용 사례를 적어주세요. -->
## 33. 계산된 필드
- 데이터 원본에 있는 필드를 활용하여 새로운 필드를 만드는 기능
- 기존 데이터 이외에 계산해야 할 데이터가 추가로 필요한할 경우에 계산된 필드를 만들어 사용한다.
<만드는 방법 3가지>
1. 데이터 패널을 통해 생성
2. 분석 탭을 활용해 생성하는 방법
3. 사용하고자 하는 필드 위에 마우스 우클릭해서 만드는 방법
#### 계산된 패널
![image](https://github.com/user-attachments/assets/02fefa37-2664-4363-bfe1-71ffdcfeee36)  
- 직접 함수를 사용하여 계산하고 컬럼을 만든다.
- 여기선 수익률을 계산하기 위해 수익 컬럼을 매출 컬럼으로 나누어 수익률을 계산했다.
![image](https://github.com/user-attachments/assets/e9569b79-dfe3-416c-a57c-6f6c647e91ae)
<!-- 계산된 필드를 사용하는 방법과 예시를 적어주세요. -->

## 34. 행수준계산
#### 기본 계산  
- 행 수준 계산을 데이터의 각 레코드를 통해 계산하는 방식  
![image](https://github.com/user-attachments/assets/fba5cce4-27f4-4e2e-9140-26d46a8bf16d)  
=> 수익률(행 수준)을 모두 더하면 100이 넘는다. 이는 행 수준으로 따로 계산했기 때문이다.  
![image](https://github.com/user-attachments/assets/bb437d0d-0656-4374-8d4c-a79c90f72ead)  
=> SPLIT함수를 통해 고객 이름 변수에서 이름만 분리해냈다.
![image](https://github.com/user-attachments/assets/b353b49c-cf25-41a2-868b-5363646c7ca8)  
=> 수익성 필드를 만들어 수익에 따라 수익성 있음/ 없음/ 평형 상태로 분류했다.  
![image](https://github.com/user-attachments/assets/77e083bf-471d-4aad-add3-abc11433544f)  
=> 주문 처리일수를 만들고 이를 차원으로 바꾸어 각 행에서 계산하여 결과를 나타나게 했다
행수준 계산: 데이터 전체로 보는 것이 아닌 그 행에서의 값을 계산하는 것이다.
적용 방법: sum[변수1]/sum[변수2]처럼 전체 데이터용 함수를 사용하지 않고 [변수1]/[변수2]와 같이 쓰면 그 행에서의 계산 결과를 볼 수 있다.


<!-- 행수준 계산의 의미와 적용 방법을 적어주세요. -->

## 35. 집계계산
집계계산: 현재 뷰에서 보이는 기준으로 계산하는 방법이다.  
tableau는 뷰에서 필드 레벨에 따라 해당 레벨에 관련된 레코드를 통해 계산해서 원한 값을 반환해서 데이터를 확인한다.  
#### 연도별 주문건수를 보는법  
먼저 계산된 필드 만들기를 통해 countd(주문 id)를 입력한다.  COUND: COUNT함수와 다르게 고유값은 한번만 카운트한다. 즉 같은 값이 2개 있으면 1개로 취급한다.
![image](https://github.com/user-attachments/assets/dc11e4ec-b0b8-4536-bcc6-0d45d0143048)  
이후 주문건수를 확인해보면 고유 주문건수는 1393이다.
![image](https://github.com/user-attachments/assets/5a3c7de1-e088-420b-8b4d-0ceab571fff5)  
하지만 주문 행은 2867개로 이는 시킨사람은 1393명이고 총 주문 수는 2867개임을 의미한다.  
![image](https://github.com/user-attachments/assets/dedcc203-1049-43df-803d-e30f9bfc5bac)
<!-- 집계계산의 정의 및 활용 사례에 대해 알게 된 점을 적어주세요. -->

## 36. 테이블계산
테이블계산: 뷰에 보이는 내용을 바탕으로 데이터가 계산된다.  
#### 현재 달과 전 월의 차이 찾기
먼저 테이블계산을 통해 새로운 변수를 찾는다.  LOOKUP: 떨어진 대상 행에서의 값으로 변환하는 함수. 즉 이 함수를 통해 한달 전 데이터를 가져오는 것이다.
![image](https://github.com/user-attachments/assets/7c843589-60b8-4043-a554-74155f9fe925)  
이를 측정값에 넣어 현재월과 전월의 차이를 시각화한다.  
![image](https://github.com/user-attachments/assets/ea15a8be-4470-4e5e-8a8d-1fa981cece32)



<!-- 테이블 계산의 개념 및 사용 방법을 적어주세요. -->

## 37. 퀵테이블계산(1)
퀵테이블계산: 테이블 계산에서 가장 자주 쓰이는 테이블 계산 유형들을 클릭만으로 가능하도록 만들언 놓은 기능이다.
#### 퀵테이블 계산을 통해 누적매출을 생성해 매출과 함께 보여주기  
![image](https://github.com/user-attachments/assets/185f38bf-b939-4e25-88bf-f8614a548b33)  
#### 각 제품에 대한 연도별 매출 차이  
![image](https://github.com/user-attachments/assets/32a76615-2576-4386-8c86-650578636273)  
#### 월별 수익차이(%)  
![image](https://github.com/user-attachments/assets/a2b3c8f4-4ae2-41dd-b250-50f767a61369)  
#### 지역별 매출 순위와 구성비율  
![image](https://github.com/user-attachments/assets/5e89b149-9f3f-4953-ab05-3babcf7a39c0)  
#### 매출이 많은 고객과 적은 고객 
- 매출이 가장 높은 고객을 100%기준으로 표현한다.
![image](https://github.com/user-attachments/assets/bab79b06-ecc8-4452-ac46-d36f8a644dc6)
<!-- 퀵테이블 계산의 원리 및 예제에 대해 알게 된 점을 적어주세요. -->

## 38. 퀵테이블계산(2)
#### 이동평균  
- 이전의 값부터 현재까지 값에 대한 평균을 낼 때 사용. 주식데이터에 자주 사용  
- 이전 값이 없다면 현재 값과 같은 값이 나온다.
![image](https://github.com/user-attachments/assets/10a2af15-d267-4af9-8db7-3ee01559efaf)  
테이블 계산 편집을 통해 어떻게 계산되었는지 알 수 있다. 이 경우엔 현재부터 2번째 전 데이터까지의 평균으로 표현했다.
![image](https://github.com/user-attachments/assets/09a0e650-8df4-4cc5-91ad-baf12cc37f4f)
#### YTD(YEAR TO DATE) 총계  
- 연도보다 하위 필드인 분기 또는 월이 있어야 사용가능하다.  
월별 매출을 누적하여 연 누적매출을 표현하는 방식과 같이 사용 가능하다.
![image](https://github.com/user-attachments/assets/fabe3a49-3217-4eb9-a281-58d5a398328a)  
#### 통합 성장률 
전 분기 대비 성장률을 각 년마다 알 수 있다.  
![image](https://github.com/user-attachments/assets/5b48316f-ae1a-467a-8e9a-4a2f67b67638)    
#### 전년 대비 성장률
- 같은 월을 기준으로 이전 년도 대비 얼마 정도 성장했는지 살펴보는데 활용
![image](https://github.com/user-attachments/assets/d3aca94b-81ee-4104-acb3-13b78b0ddd6a)
#### TEAR TO DATE 성장률  
전년대비 누적 매출액의 성장률을 확인할 수 있다.  
![image](https://github.com/user-attachments/assets/7b4d4388-5391-4322-b462-d3bee60c37e2)
<!-- 이동평균, YTD 총계, 전년 대비 성장률, YTD 성장률 등 본 강의에서 알게 된 점을 적어주세요. -->

## 문제 1.

규석이는 이제껏 매출을 올리는 데에 힘썼었지만, 왠지 모르게 주머니에 들어오는 돈이 없어 속상합니다. 

그래서 매출이 상위 20곳에 속하지만, 수익률(%)이 마이너스인 시/도를 확인하려고 합니다.

> 수익률은 SUM([수익]) / SUM([매출])로 정의합니다.

어떤 집합을 만들었고, 어떤 결합을 하였는지를 중심으로 기술하고, 결과 자료를 첨부해주세요. 

(텍스트 표 형태이며, 색상으로 위 집합을 구분할 수 있게 만들어주세요.)

<!-- 아래 예시 이미지를 삭제하고, 직접 만든 시트 사진을 올려주세요. 시트의 이름은 본인 이름으로 기입해주세요-->

먼저 시/도 매출 상위 20곳 집합을 만든다.  
![image](https://github.com/user-attachments/assets/f868d78c-f46f-460a-b25d-c0856eb05930)  
이후 수익률이 마이너스인 시/도 집합을 만든다.  
![image](https://github.com/user-attachments/assets/d9921e89-3c47-4689-94fa-40dd9f71e15f)  
이후 이 집합들을 합치다. 이때 상위 20곳에 속하면서 수익률이 마이너스인 공통집합부분을 뽑아야한다. 따라서 inner join을 수행한다.  
![image](https://github.com/user-attachments/assets/c863c02b-af99-425c-bdb5-5baf2d6186bc)  
이후 이를 필터에 추가하여 색깔로 구분하게 만든다.
![image](https://github.com/user-attachments/assets/fe10cc01-67a6-4bf2-8a2a-22b282dd2a04)  
## 문제 2.
선희는 주문 Id별로 주문에서 배송까지에 걸리는 날짜 일수가 궁금했습니다. 
그래서 주문 ID별로 주문에서 배송까지 걸리는 일자를 '배송까지 걸린 일수'라는 계산된 필드로 만들고, 이를 마크에 올린 후 확인해보았습니다. 
이때, 계산된 필드의 식은 'DATEDIFF' 함수를 이용하였습니다.

배송까지 걸린 일수 계산을 위한 DATEDIFF 함수 수식을 적어주세요.

```
DATEDIFF('day', [주문 날짜], [배송 날짜])
```

![datediff](https://github.com/yousrchive/BUSINESS-INTELLIGENCE-TABLEAU/blob/main/study/img/4th%20til/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202024-09-30%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%203.47.21.png?raw=true)

그런데 위 그림처럼 '주문 날짜'와 '배송 날짜'를 함께 행에 올려 확인해보니, 주문날짜와 배송날짜의 차이가 '배송까지 걸린 일수'와 다릅니다.

ID-2021-11126을 보니, 11월 26일 배송에 11월 30일 배송이면 4일 차이인데, 12일이 걸렸다고 하네요. 왜 이런 문제가 생긴걸까요?

```
옆을 보면 합계(배송까지 걸린 일수) 라고 쓰여있다. 즉 해당 컬럼은 합계가 나타난 컬럼이어서 12인 것이다.
실제로 해당 id는 4일 걸린 상품을 3개 시켰다.
```
![image](https://github.com/user-attachments/assets/06e17492-71ba-45b3-9156-c5c81b5ce475)

그리고 이를 해결하기 위해서는 어떻게 해야 할까요?

```
합계가 아니라 그 행에서의 결과만 보여줘야 하므로 우클릭 후 차원으로 바꿔준다.
id 11126의 배송날짜가 4일로 바뀐것을 확인할 수 있다.
```
![image](https://github.com/user-attachments/assets/ca40f9b7-85e3-46d8-ad4b-89e5572fdaca)

## 문제 3.

다음은 Tableau의 다양한 계산을 사용할 수 있는 경우를 빈칸으로 두고 문제를 작성한 것입니다. 각 빈칸에 적합한 계산 유형을 채워보세요.

보기
> **누계, 차이, 비율 차이, 구성 비율, 순위, 백분위수, 이동 평균, YTD 총계, 통합 성장률, 전년 대비 성장률, YTD 성장률**

| 계산 유형               | 설명                                                                 | 사용 예시                                                                                          |
|-------------------------|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| 누계          | 데이터의 누적 합계를 계산                                             | 한 기업이 월별 매출 데이터를 누적하여 연간 매출 추이를 보고 싶을 때 사용                                      |
| 차이           | 연속 데이터 포인트 간의 차이를 계산                                    | 한 기업이 월별 매출 데이터에서 전월 대비 매출 증감량을 분석하고 싶은 경우                                        |
| 비율 차이            | 연속 데이터 포인트 간의 비율 변화를 계산                               | 한 기업이 월별 매출 데이터에서 전월 대비 매출 증감률(%)을 분석하고 싶은 경우                                      |
| 구성 비율            | 전체에서 각 데이터 포인트의 비율을 계산                                | 한 기업이 전체 매출에서 각 제품군이 차지하는 비율을 보고 싶을 때 사용                                           |
| 순위            | 데이터의 순위를 매깁니다                                              | 한 기업이 제품별 매출 데이터를 순위별로 정렬하여 상위 10개 제품을 분석하고 싶은 경우                              |
| 백분위수            | 데이터의 백분위를 계산                                               | 한 기업이 고객별 구매 금액 데이터를 백분위수로 나누어 상위 25% 고객을 분석하고 싶은 경우                          |
| 이동 평균            | 일정 기간의 평균을 계산                                               | 한 기업이 주간 매출 데이터에서 4주 이동 평균을 계산하여 트렌드를 분석하고 싶은 경우                              |
| YTD 총계            | 연초부터 현재까지의 총계를 계산                                      | 한 기업이 월별 매출 데이터를 연초부터 현재까지 누적하여 연간 매출 목표 달성 여부를 분석하고 싶은 경우             |
| 통합 성장률            | 일정 기간 동안의 연평균 성장률을 계산                                  | 한 기업이 5년 간 매출 데이터를 바탕으로 연평균 성장률(CAGR)을 계산하고 싶은 경우                                  |
| 전년 대비 성장률            | 전년 동기간 대비 성장률을 계산                                        | 한 기업이 월별 매출 데이터에서 전년 동월 대비 매출 성장률을 분석하고 싶은 경우                                    |
| YTD 성장률            | 연초부터 현재까지의 성장률을 계산                                     | 한 기업이 올해 연초부터 현재까지의 매출이 전년 동기 대비 얼마나 성장했는지 분석하고 싶은 경우                     |

> 사용 예시를 참고하여 실제 경우처럼 생각하며 고민해보아요!

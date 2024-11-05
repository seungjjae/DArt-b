# Fifth Study Week

- 39강: [LOD](#39강-lod)

- 40강: [EXCLUDE](#40-lod-exclude)

- 41강: [INCLUDE](#41-lod-include)

- 42강 : [매개변수](#42-매개변수)

- 43강 : [매개변수 실습](#43-매개변수-실습) 
![링크](https://youtu.be/GJvB8hBqeE8?si=3jIj1iymZHZ7mBam)

- 44강: [매개변수 실습](#44-매개변수-실습)

- 45강: [마크카드](#45-워크시트-마크카드)

- 46강: [서식계층](#46-서식-계층)

- 47강: [워크시트](#47-워크시트-서식)

- [문제1](#문제-1)

- [문제2](#문제-2)

## Study Schedule

| 강의 범위     | 강의 이수 여부 | 링크                                                                                                        |
|--------------|---------|-----------------------------------------------------------------------------------------------------------|
| 1~9강        |  ✅      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=84)       |
| 10~19강      | ✅      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=75)       |
| 20~29강      | ✅      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=65)       |
| 30~38강      | ✅      | [링크](https://www.youtube.com/watch?v=e6J0Ljd6h44&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=55)       |
| 39~47강      | ✅      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=45)       |
| 48~59강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=35)       |
| 60~69강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=25)       |
| 70~79강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=15)       |
| 80~89강      | 🍽️      | [링크](https://www.youtube.com/watch?v=AXkaUrJs-Ko&list=PL87tgIIryGsa5vdz6MsaOEF8PK-YqK3fz&index=5)        |


<!-- 여기까진 그대로 둬 주세요-->

> **🧞‍♀️ 오늘의 스터디는 지니와 함께합니다.**


## 39강. LOD
- LOD는 LEVEL OF DETAIL
- 뷰에 세부 수준을 나타낸다.
- 계산할 수준을 세부적으로 제어 가능하도로 한다.
### FIXED LOD
-현재 뷰에 있는 차원과 상관없이 계산된 필드에서 원하는 차원을 따라 계산한다.  
#### FIXED에서 설정한 차원이 뷰에 포함되어 있을 때
![image](https://github.com/user-attachments/assets/506d2030-6a50-4c29-b637-b3552a44b740)
FIXED에서 설정한 세부 수준인 지역 기준으로 데이터가 계산되어 나타난다.
#### FIXED에서 설정한 차원이 뷰에 포함되어 있지 않을 때
![image](https://github.com/user-attachments/assets/3733f006-d8d2-411d-8b0d-09db49d2b4f3)
뷰에는 포함되어 있지 않은 제품 범주 기준으로 계산해 데이터를 보여준다.
#### QUICK TABLE과의 차이
![image](https://github.com/user-attachments/assets/b6d698b3-7a58-4953-8145-9d3d1aefcbad)
퀵 테이블은 하위 범주를 뷰에서 제외하면 제외된 범주 이외에 하위 범주들을 통해 구성 비율을 계산한다.  
FIXED는 하위 범주를 뷰에서 제외해도 해당 하위 범주들을 포함하여 계산한다.  

<!-- INCLUDE, EXCLUDE, FIXED 등 본 강의에서 알게 된 LOD 표현식에 대해 알게 된 점을 적어주세요. -->


## 40. LOD EXCLUDE
#### EXCLUDE
-현재 뷰에서 특정 차원을 제외하여 계산할 때 사용된다.
![image](https://github.com/user-attachments/assets/436b03b2-0485-4649-8d9e-d1712db0fa21)
EXCLUDE는 뷰에 있는 차원을 따라 계산하기 때문에 필터를 걸면 FIXED와 달리 값이 바뀐다.
#### LOD EXCLUDE
![image](https://github.com/user-attachments/assets/2ca7a15e-dd3c-4089-9320-ef2f6bd46a29)
이를 통해 특정제품(여기선 액세서리)매출을 기준으로 나머지 제품 매출을 표현했다.
  
<!-- INCLUDE, EXCLUDE, FIXED 등 본 강의에서 알게 된 LOD 표현식에 대해 알게 된 점을 적고, 아래 두 질문에 답해보세요 :) -->

> **🧞‍♀️ FIXED와 EXCLUDE을 사용하는 경우의 차이가 무엇인가요?**

```
EXCLUDE는 뷰에 있는 차원을 따라 계산하기 때문에 필터를 걸면 FIXED와 달리 값이 바뀐다.
즉 EXCLUDE는 현재 보이는 변수들만을 계산하여 바뀔 수 있지만 FIXED는 고정된 값으로 처음 설정한 변수들로 계산한다.
```

> **🧞‍♀️ 왜 ATTR 함수를 사용하나요?**

```
특정 값을 기준으로 나머지 값들과의 차이를 표시하기 위해서 사용한다.
```


## 41. LOD INCLUDE
- 현재 뷰에서 특정 차원을 추가하여 계산한다.
- EXCLUDE LOD와 같이 차원 필터를 통해 해당 값을 변경할 수 있다.
![image](https://github.com/user-attachments/assets/837c5dd0-4769-4ed4-853b-aae56474391b)

<!-- INCLUDE, EXCLUDE, FIXED 등 본 강의에서 알게 된 LOD 표현식에 대해 알게 된 점을 적고, 아래 두 질문에 답해보세요 :) -->


> **🧞‍♀️ 그렇다면 어떤 경우에 각 표현식을 사용하나요? 예시와 함께 적어보아요**


```
뷰에 표시되는 값이 차원일때->FIXED LOD 표현식만 사용 가능(FIXED LOD는 차원과 측정값을 반환할 수 있는데 INCLUDE와 EXCLUDE LOD는 측정값만 반환가능하다)
반환 값이 차원 필터에 영향을 받게 될 경우 INCLUDE와 EXCLUDE LOD를 사용해야 한다. 
```

## 42. 매개변수
-태블로에서 말하는 매개변수는 고정된 상수 값이 아닌 동적인 값으로 변경하기 위해서 활용하는 기능으로 매개변수는 반드시 계산식, 필터, 참조선과 함께 사용된다.
### 매개변수 만들기1. 필터
![image](https://github.com/user-attachments/assets/0aada701-fdf4-4227-af08-daa01ecadb16)
필터->필드 기준->새 매개변수 만들기
### 매개변수 만들기2. 필드 위에 우클릭
![image](https://github.com/user-attachments/assets/bdc36bd4-b3ed-4954-96cd-11f7c6533de3)
### 매개변수 만들기3. 데이터패널을 통해 만들기
![image](https://github.com/user-attachments/assets/aafae9a4-794f-475a-9da4-1782ba87b2c4)  
오른쪽 상단의 숫자를 바꿔 실시간으로 상위N개를 뽑을 수 있다.  
<!-- 매개변수에 대해 알게 된 점을 적어주세요 -->

> **🧞‍♀️ 집합에도 매개변수를 적용할 수 있나요? 시도해봅시다**
집합에 매개변수 적용
![image](https://github.com/user-attachments/assets/52f153f0-685a-46fc-a82c-3388d47fe38c)  
![image](https://github.com/user-attachments/assets/c511f636-c449-4195-a34f-42f7e1ee304e)  


## 43. 매개변수 실습
![image](https://github.com/user-attachments/assets/321f7d59-1577-421b-9377-0e489c75f5cf)


## 44. 매개변수 실습
### 참조선 실습
![image](https://github.com/user-attachments/assets/bf4f7df1-690a-45a4-baf4-f0e62e75f8f3)
목표매출 달성했을때와 하지 않았을때 색을 통해 구분한다.
<!-- 매개변수에 대해 알게 된 점을 적어주세요 -->

## 45. 워크시트 마크카드
![image](https://github.com/user-attachments/assets/53510059-66d2-4cc4-83f4-6602841e6057)
마크칸에 있는 다양한 기능들을 사용해봤다.
<!-- 마크카드에 대해 알게 된 점을 적어주세요 -->


## 46. 서식 계층

<!-- 서식계층에 대해 알게 된 점을 적어주세요 -->
![image](https://github.com/user-attachments/assets/1ad16502-7fc1-466e-81b7-52cf591e55b5)

> **🧞‍♀️ 서식계층을 일반적인 것에서 구체적인 것 순서로 기입해보세요**


```
왼쪽에서 오른쪽으로 갈수록 더 구체적이다
워크시트 서식 > 행/열 서식 > 특정 필드 > 필드 레이블 > 도구설명/제목/마크
```


## 47. 워크시트 서식
-글꼴, 맞춤, 음영 서식
![image](https://github.com/user-attachments/assets/9ceb140f-91d0-4cb4-b5a9-8458519f7e01)

<!-- 워크시트 서식에 대해 알게 된 점을 적어주세요!-->



## 문제 리스트



## 문제 1.

```
가장 많이 주문한 사람들은 물건 배송을 빨리 받았을까요?
조건을 준수하여 아래 이미지를 만들어봆시다.
1) 국가/지역별(이하 '나라'로 통칭), 범주별로 배송일자가 다를 수 있으니 먼저, 나라별/범주별로 평균 배송일자를 설정한 뒤,
2) 각 나라에서 가장 많이 주문한 사람의 이름을 첫 번째 열,
3) 그 사람이 주문한 제품 이름을 2번째 열,
4) 각 상품이 배송까지 걸린 날 수를 표현하고
5) 그리고 만약 배송이 각 나라/범주별 평균보다 빨랐다면 '빠름', 같다면 '평균', 느리다면 '느림' 으로 print 해주세요. 
```
![image](https://github.com/user-attachments/assets/db2e4b8e-e371-4cca-a355-e25b86fd3404)  
먼저 배송 소모일을 계산한다.  
![image](https://github.com/user-attachments/assets/4b9f8550-89ef-40cd-8ac7-620baafcb03b)  
이후 나라별/범주별 배송 소모일을 계산한다. 현재 차원형태의 계산을 진행해야 함. 따라서 FIXED사용 (이부분이 어려워서 검색 많이 함)
![image](https://github.com/user-attachments/assets/ec7ae60f-e6e7-4289-8bef-f0e24249b842)  
이후 배송 속도 계산
![이미지주소](https://github.com/yousrchive/BUSINESS-INTELLIGENCE-TABLEAU/blob/main/study/img/2nd%20study/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202024-08-13%20%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB%2010.12.36.png?raw=true)
![image](https://github.com/user-attachments/assets/b8d0f9be-f507-45a7-a8e9-d449a836f150)

<!-- 여기까지 오는 과정 중 알게 된 점을 기입하고, 결과는 시트 명을 본인 이름으로 바꾸어 표시해주세요.-->

## 문제 2.

```
채원이는 태블로를 쓰실 수 없는 상사분께 보고하기 위한 대시보드를 만들고 싶어요. 

제품 중분류별로 구분하되 매개변수로써 수익, 매출, 수량을 입력하면 저절로 각각 지표에 해당하는 그래프로 바뀌도록 설계하고자 해요.

 어떤 값이 각 지표의 평균보다 낮은 값을 갖고 있다면 색깔을 주황색으로, 그것보다 높다면 파란색으로 표시하고 싶어요. 그 평균값은 각 지표별로 달라야 해요.
```
매개변수 생성
![image](https://github.com/user-attachments/assets/128d6fd7-df7d-4b91-b287-836631503145)  
계산된 필드 만들기
![image](https://github.com/user-attachments/assets/c993006b-1112-4b9c-bf6e-e38eb0314b33)
이후 행/열에 집어넣고 색상 단계를 2단계로 낮추었다. 매개변수도 적용시켰다.
![image](https://github.com/user-attachments/assets/5f7bd939-3b3a-4a5b-8986-c8271dd672a8)


![example](https://github.com/yousrchive/BUSINESS-INTELLIGENCE-TABLEAU/blob/main/study/img/2nd%20study/%E1%84%83%E1%85%A1%E1%84%8B%E1%85%AE%E1%86%AB%E1%84%85%E1%85%A9%E1%84%83%E1%85%B3.png?raw=true)

<!-- 예시 사진은 지워주세요-->

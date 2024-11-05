# 4-4. 날짜 및 시간 데이터 이해하기(2)(EXTRACT, DATETIME_TRUNC, PARSE_DATETIME, FORMAT_DATETIME)  
## CURRENT_DATETIME()-현재시간을 확인하기
![image](https://github.com/user-attachments/assets/d51d27ee-c366-4550-a3c0-f2cd333abb6c)  
CURRENT_DATE()와 CURRENT_DATETIME()간의 차이가 존재한다. 전자는 날짜만 나오며 후자는 날짜와 시간초까지 나온다. 괄호안에 'Asia/Seoul'을 입력하면 한국기준 시간이 나온다.  
## EXTRACT함수-DATETIME에서 특정 부분만 추출하고 싶은 경우  
![image](https://github.com/user-attachments/assets/3fcc7786-028d-48aa-8182-92ec5a2644e3)  
YEAR 이외에도 DAY, MONTH, HOUR, MINUTE 등을 통해 다양하게 추출할 수 있다.
### 요일을 추출하고 싶을 경우  
![image](https://github.com/user-attachments/assets/e86635ea-06ca-4113-8508-0eed91a547a2)  
일요일이 1~ 토요일이7로 반환된다. 이를 이용해 요일을 알 수 있다.  
## DATETIME_TRUNC-시간자르기
![image](https://github.com/user-attachments/assets/fce2a6b6-4687-4ca4-8598-b9d10dd36f56)  
기준점 아래를 모두 최소의 수로 만든다 => 월별, 일별로 데이터를 정리하려고 할 때 사용 가능하다
## PARSE_DATETIME-문자열을 DATETIME으로 바꿀때
![image](https://github.com/user-attachments/assets/fd3dc7d4-179e-4470-b2b4-b2dc2abb4c9e)
DATETIME형식을 띄지만 실제론 문자열인 경우 이를 바꿀때 사용한다.  
## FORMAT_DATETIME-DATETIME을 문자열로 바꿀때  
![image](https://github.com/user-attachments/assets/ad75e8e3-c900-4527-bda3-35ac7501150d)  
문자열로 바꾼 결과
## DATETIME_DIFF-날짜의 차이계산
![image](https://github.com/user-attachments/assets/a6d8a7bd-f4b0-4df8-85f2-cdc6217b083d)  
기준은 DAY, MONTH, WEEK 등 직접 설정할 수 있다.  
# 4-5. 시간데이터 연습문제 1~2번  
## 문제1. 트레이너가 포켓몬을 포획한 날짜를 기준으로 2023년 1월에 포획한 포켓몬의 수를 계산해주세요.
![image](https://github.com/user-attachments/assets/f863d0e4-ff7c-4b0c-8821-cf2a372a6c93)  
이 문제에선 데이터타입을 조심해야한다. DATETIME으로 이름이 적혀있지만 실제로는 TIMESTAMP였기 때문에 이를 TIMESTAMP로 변경한 후 쿼리를 진행했다.
## 문제2. 배틀이 일어난 시간을 기준으로 오전6시에서 오후6시 사이에 일어난 배틀의 수를 계산해주세요.
![image](https://github.com/user-attachments/assets/c027e2df-690d-44ff-8ce0-6e26de3bb088)
# 4-5. 시간 데이터 연습문제 3~5번
## 문제3. 각 트레이너별로 그들이 포켓몬을 포획한 첫 날(catch_data)을 찾고, 그 날짜를 DD/MM/YYYY 형식으로 출력해주세요.  
![image](https://github.com/user-attachments/assets/94887510-f407-4ed1-b3b9-fdd7993f23d3)  
## 문제4.배틀이 일어난 날짜(battle_date)를 기준으로 요일별로 얼마나 자주 일어났는지 계산해주세요.  
![image](https://github.com/user-attachments/assets/11d95f8f-aced-4ac8-9c2c-d83b5fcb3dc3)  
## 문제5.트레이너가 포켓몬을 처음으로 포획한 날짜와 마지막으로 포확한 날짜의 간격이 큰 순으로 정렬하는 쿼리를 작성해주세요.  
![image](https://github.com/user-attachments/assets/3f8001d7-d4b7-49c4-af4e-5e3ecf9968b4)  
# 4-6. 조건문(CASE WHEN, IF)  
- 만약 특정 조건이 충족되면 어떤 행동을 하자
- 특정 조건이 참일때 A, 아니면 B
- etc..
## CASE WHEN  
- 여러 조건이 있을 경우 유용  
형식  
SELECT  
  CASE  
    WHEN 조건1 THEN A  
    WHEN 조건2 THEN B  
    ELSE C  
END AS 컬럼이름
## IF  
- 단일 조건일 경우 유용
형식    
SELECT  
  IF(1=1, '동일한 결과', '동일하지 않은 결과') AS result1,  
  IF(1=2, '동일한 결과', '동일하지 않은 결과') AS RESULT2  
# 4-7.  조건문 연습 문제
## 문제1. 포켓몬의 speed가 70이상이면 빠름, 그렇지 않으면 느림으로 표시하는 새로운 컬럼 Speed_Category를 만들어 주세요
![image](https://github.com/user-attachments/assets/51a52872-a3c1-490f-ab6e-f12bcae53f54)  
## 문제2. 포켓몬의 type1에 따라 Water, Fire, Electric 타입은 각각 물, 불, 전기로 그 외 타입은 기타로 분류하는 새로운 컬럼 type_Korean을 만들어주세요.
![image](https://github.com/user-attachments/assets/836d1e49-5873-48e9-bb32-ee4b40714902)  
## 문제3. 각 포켓몬의 총점(total)을 기준으로 300이하면 Low, 301에서 500사이면 Medium, 501이상이면 High로 분류해주세요.  
![image](https://github.com/user-attachments/assets/346f9075-2fca-4b05-ad97-130abfd709d9)  
## 문제4. 각 트레이너의 배지 개수(badge_count)를 기준으로 5개 이하면 Beginner, 6개에서 8개 사이이면 Intermediate, 그 이사이면 Advanced로 분류해주세요. 
![image](https://github.com/user-attachments/assets/c95b92f2-c296-47fb-a0d9-d6c41d191be8)
## 문제5. 트레이너가 포켓몬을 포획한 날짜(catch_date)가 2023-01-01 이후면 Recent 아니면 01d로 분류해주세요.
![image](https://github.com/user-attachments/assets/83823c14-31c6-43e9-8f2f-97d272f2a31b)  
## 문제6. 배틀에서 승자(wineer_id)가 player1_id와 같다면 player1 wins, player2_id와 같다면 player2 wins를 출력하세요.
![image](https://github.com/user-attachments/assets/44b69f9e-f9d2-44ce-83db-d7238860107d)
# 4-8. 정리
모든 문법을 외울 필요는 없다. 자주 쓰는 것은 외우는 걸 추천하지만 그렇지 않은 것들을 그때 그떄 검색하는 습관을 들이자.
# 4-9. BigQuery 공식 문서 확인하는 법
chatgpt나 검색은 최신 업데이트된 정보까지 반영하지 않을 수 있다. 따라서 공식 문서를 읽는 방법을 알아두면 위기의 순간에 활용 가능하다.  
찾는 방법: '기술명+documentation'   EX)BigQuery documentation검색

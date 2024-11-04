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
- 4-5. 시간 데이터 연습문제 3~5번
- 4-6. 조건문(CASE WHEN, IF)
- 4-7.  조건문 연습 문제
- 4-8. 정리
- 4-9. BigQuery 공식 문서 확인하는 법

# 3-4. 오류를 디버깅하는 방법
쿼리를 작성하면서 실행이 안되는 경우를 경험할 것이다  
ex)syntax error  
#### 오류  메세지가 알려주고자 하는 것  
1. 현재 작성한 방식으로 하면 답을 얻을 수 없어요. (길잡이 역할)  
2.  이 부분에 문제가 되어요. (문제 진단)
#### 오류를 바라보는 관점
오류 발생시=> 길잡이가 나를 더 좋은 길로 나아가게 한다.  
좋은 길로 가는 방법=> 오류 메시지를 보면서 더 좋은 길로 나가자  
#### BigQuery Error
대표적인 오류 카테고리: Syntax Error(문법 오류)  
- 문법을 지키지 않아 생기는 오류
- Error Message를 보고 번역 또는 해석한 후, 해결 방법 찾아보기
구글에 검색/ ChatGPT에 질문/ 지인에게 질문(커뮤니티 등)
#### 쉽게 발생할 수 있는 오류
- LIMIT을 맨 끝에 쓰지 않는 경우
- 두 쿼리를 동시에 사용하는데 ;을 붙이지 않은 경우
- 그룹화가 필요한데 하지 않은 경우
- 괄호를 시작했지만 끝마치지 않은 경우
# 4-1. INTRO
#### 데이터 탐색:변환에 대해 다룬다.
자료형에 따른 여러 함수 소개
- 문자열
- 날짜 및 시간 데이터
- 조건문 함수
- BigQuery 공식 문서 확인하는 방법
# 4-2. 데이터 타입과 데이터 변환(CAST, SAFE_CAST)
#### 데이터 타입
숫자/ 문자/ 시간,날짜/ 부울(참, 거짓) 이 존재한다. 이 외에도 몇개가 더 존재하지만 우선 이것부터 공부하는게 좋다.  
#### 데이터 타입이 중요한 이유
<보이는 것과 저장된 것의 차이가 존재>  
- 엑셀에서 보면 빈 값=>""일 수도 있고 NULL일 수도 있다.
- 1이라고 작성된 경우=> 숫자 1일수도 있고 문자 1일 수도 있다.
- 2023-12-31 => DATE일 수도 있고 문자일 수도 있다.
- 따라서 내 생각과 다른 경우 데이터의 타입을 서로 변경해야 한다.
#### 자료 타입 변경하기
자료 타입을 변경하는 함수: CAST  
ex)  
SELECT    
CAST(1 AS STRING) =>숫자 1을 문자 1로 변경  
하지만 정수형 데이터가 포함된 컬럼을 숫자로 바꾸는 것은 불가능하다.  
=> 이 경우 SAFE_CAST를 사용하면 변환이 실패할 경우 NULL을 반환한다. 
SAFE의 경우 SAFE_DIVIDE를 사용하면 3/0과 같이 계산이 불가능할 경우 NULL로 표현한다.
# 4-3. 문자열 함수(CONCAT, SPLIT, REPLACE, TRIM, UPPER)
#### 문자열 함수
- 문자열 붙이기: CONCAT  
- 문자열 분리하기: SPLIT  
- 특정 단어 수정하기: REPLACE  
- 문자열 자르기: TRIM  
- 영어 대문자 변환: UPPER
#### CONCAT
![image](https://github.com/user-attachments/assets/405865b9-54b6-45bf-a840-3bba556755a8)
- CONCAT('문장1', '문장2', '문장3', ...)
- CONCAT 인자로 STRING이나 숫자를 넣을 때는 데이터를 직접 넣어준 것 => FROM이 없어도 실행된다!
#### SPLIT
![image](https://github.com/user-attachments/assets/2952c689-87a3-4e49-8d69-b2ce441541b1)
- SPLIT('문장', '나눌 기준')
- 띄어쓰기도 문자로 인식되므로 이를 인지해서 쿼리를 작성해야 한다.
- 결과가 배열(ARRAY)로 나온다.
#### REPLACE
![image](https://github.com/user-attachments/assets/790068f1-3b38-45c5-a539-1136d4a4e625)
- REPLACE('문장', '바꾸어질 단어', '바꿀 단어')
#### TRIM
![image](https://github.com/user-attachments/assets/ffdca18b-7891-4d10-a254-925fe9330c59)
-TRIM('문장', '자를 단어')
#### UPPER
![image](https://github.com/user-attachments/assets/180d1691-ab4d-450d-8725-b5368072dc45)
- UPPER('문자열 원본') 
# 4-4. 날짜 및 시간 데이터 이해하기(1)(타임존, UTC, Millisecond, TIMESTAMP/DATETIME)
#### 날짜 및 시간 데이터의 핵심
1. 날짜 및 시간 데이터 타입 파악하기: DATE, DATETIME, TIMESTAMP
2. 날짜 및 시간 데이터 관련 알면 좋은 내용: UTC, MILLISECOND
3. 날짜 및 시간 데이터 타입 변환하기
4. 시간 함수(두 시간의 차이, 특정 부분 추출하기)
#### 시간 데이터 다루기
- 시간 데이터도 세부적으로 나눌 수 있다.  
- DATE, DATETIME, TIMESTAMP 등  
- DATE: DATE만 표시하는 데이터(2024-10-06)  
- DATETIME: DATE와 TIME까지 표시하는 데이터, TIME ZONE 정보 없음(2024-10-06-00:55:00)    
- TIME: 날짜와 무관하게 시간만 표시하는 데이터(00:55:00)    
#### TIME ZONE   
UTC: 국제적인 표준 시간/ 한국 시간은 UTC+9 이다.  
(TIME STAMP)  
- 시간 도장  
- UTC부터 경과한 시간을 나타내는 값  
- TIME ZONE 정보가 있다.  
- 2023-12-31 14:00:00 UTC
#### MILLISECOND, MICROSECOND
MILLISECOND(MS): 천분의 1초  
MICROSECOND(US): MILLISECOND의 천분의 1  
![image](https://github.com/user-attachments/assets/a595e24e-3297-4c77-93c2-f7868f4f6585)
- TIMESTAMP는 이상한 정수이지만 거기에 시간이 저장되어 있다.  
- TIMESTAMP <=>DATETIME 변환을 해야할 수 있다.  
#### TIMESTAMP, DATETIME 비교
TIME STAMP  
- UTC라고 나옴  
- 한국시간 -9시간

DATETIME    
- T가 나옴(TIMEZONE의미)  
- 한국 존 사용시 한국 시간과 동일

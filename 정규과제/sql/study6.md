# 5-1. Intro
## JOIN
- 다량의 자료를 연결
# 5-2. JOIN 이해하기
- 서로 다른 테이블을 연결하는 것  
- 쿼리작성->결과->확인(피드백)->다시시도->결과  
- 데이터를 연결할 수 있는  공통 값(KEY)가 필요  
# 5-3. 다양한 JOIN 방법
## INNER JOIN
- 공통적인 요소만 남김(ROW기준)
## LEFT/RIGHT JOIN
- 합칠 때 기준 데이터의 ROW에 합쳐지는 데이터의 컬럼을 넣음. 만약 기준 데이터의 값이 합쳐지는 데이터에 없으면 NULL로 표현
## FULL OUTER JOIN
- 싹 다 합치기.
## CROSS JOIN
- M개의 데이터와 N개의 데이터를 합치면 M*N의 개수로 가능한 모든 경우의수를 출력
# 5-4. JOIN 쿼리 작성하기
## 기본 문법
SELECT    
  A.COL1,  
  A.COL2,  
  B.COL1 1,  
  B.COL1 2  
FROM table1 AS A  
LEFT JOIN table2 AS B  
ON A.KEY = B.KEY
- CROSS JOIN은 ON필요X
## 예시
![image](https://github.com/user-attachments/assets/561e5b90-7588-4fb3-845e-828ca81676c0)  
trainer_pokemon의 trainer_id와 trainer의 id를 key로 LEFT JOIN한 결과  
![image](https://github.com/user-attachments/assets/f55a36c6-9543-4454-9961-cf31b86b3949)  
이단 JOIN사용. 
# 5-5. JOIN을 처음 공부할 때 헷갈렸던 부분
## 1)여러 JOIN중 어떤 것을 사용해야 할까?
- 작업의 목적에 따라 다르다
- 교집합: INEER
- 모두 다 조합: CROSS
- LEFT, RIGHT중에선 LEFT만 계속 사용하는 것을 추천
## 2)어떤 TABLE을 왼쪽에 두고, 어떤 TABLE이 오른쪽에 가야할까?
- LEFT의 경우 기준이 되는 TABLE이 왼쪽에 존재  
- 기준이란 데이터 요소가 빠짐없이 존재하는 데이터  
## 3)여러 TABLE을 연결할 수 있을까?
- JOIN의 개수에 한계는 없음
- 너무 많이 JOIN하고 있는지 확인(문제가 될 수 있음)
## 4)컬럼은 모두 다 선택해야 할까?
- 데이터를 추출해서 무엇을 하고자하는가에 따라 다름
- 사용하지 않을 컬럼은 최종적으로는 선택하지 않는 것을 추천
- ID는 PRIMARY KEY인 경우가 많음
## 5)NULL이 대체 뭐죠?
- 값이 없음
- 0은 데이터가 0으로 존재하는 경우로 존재하지 않는 데이터인 NULL과 차이가 있음.
- 연결할 값이 없는 경우 JOIN에서 나타남.
# 5-6. JOIN 연습문제 1~2번
## 1.트레이너가 보유한 포켓몬들은 얼마나 있는지 알 수 있는 쿼리를 작성해주세요.
![image](https://github.com/user-attachments/assets/9c25f41c-1117-42f9-9e5b-d3f7168edf40)
서브쿼리를 사용해서 ('active', training')상태인 포켓몬들을 먼저 선정하고 이후 카운트 하는 방법.
## 2.각 트레이너가 가진 포켓몬 중에서 'grass'타입의 포켓몬 수를 계산해주세요.(단 편의를 위해 type1 기준으로 계산해주세요.)
![image](https://github.com/user-attachments/assets/420aa21d-e08f-4114-b513-145c064563b5)

- *5-6. JOIN 연습문제 3~5번*
- **5-7. 정리**

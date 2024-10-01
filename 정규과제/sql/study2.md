# 2-3. 데이터 탐색(Select, from, where) 
![image](https://github.com/user-attachments/assets/305f1495-5fc9-4dc8-b4a2-022b4b06e13f)
포켓몬의 정보를 표현한 것이다. 이를 테이블의 형태로 정리하면 아래와 같은 그림이 나온다.
![image](https://github.com/user-attachments/assets/e680fab8-08c7-4b23-9040-56867c5091aa)
#### SQL쿼리 구조
SELECT, FROM, WHERE을 사용해 작성한다.  
EX)
SELECT  =>어떤 컬럼을 출력할 것인가?  
  COL1 AS NEW_NAME,  =>컬럼이름 별칭하기  
  COL2,  
  COL3  
FROM DATASET.TABLE  =>어떤 테이블에서 데이터를 확인할 것인가?  
WHERE COL1=1  =>원하는 조건  

#### 포켓몬 타입이 불인 포켓몬을 찾는 쿼리
SELECT * =>SELECT * 은 모든 컬럼 출력을 의미한다.  
FROM BASIC.POKEMON  
WHERE TYPE1 = 'FIRE'  
#### 데이터가 여러 저장소에 저장되어 있는 경우  
특정 TABLE에 있는 데이터를 각각 추출한 후, 연결하기(JOIN사용)
![image](https://github.com/user-attachments/assets/1b08a527-cf12-4e1f-8d7e-e804e2fbf162)
TABLE A에 있는 데이터와 TABLE B에 있는 데이터를 각각 추출한후 JOIN을 통해 합친다.
#### 데이터 파악
![image](https://github.com/user-attachments/assets/533a0e0e-740d-498f-a084-4aaa4fe4601c)
데이터의 미리보기 항목을 통해 데이터를 파악할 수 있다.  
#### SQL 문법 핵심 정리  
* FROM  
  데이터를 확인할 table명시      
  이름이 너무 길다면 AS '별칭'으로 별칭 지정 가능  
  FROM table1 AS t1  
* WHERE  
  FROM에 명시된 Table에 저장된 데이터를 필터링(조건 설정)  
  Table에 있는 컬럼을 조건 설정  
* SELECT  
  Table에 저장되어 있는 컬럼 선택  
  여러 컬럼 명시 가능  
  col1 AS '별칭'으로 컬럼의 이름도 별칭 지정 가능
  
실행순서 : FROM->WHERE->SELECT
#### 실습
![image](https://github.com/user-attachments/assets/88574430-0625-45c1-82a6-5b5f309412f6)  
# 2-4. SELECT 연습문제(10분)
1. trainer 테이블에 있는 모든 데이터를 보여주는 SQL쿼리를 작성해주세요  
![image](https://github.com/user-attachments/assets/904225a2-62ab-411e-9891-34984d831ace)
2. trainer 테이블에 있는 트레이너의 name을 출력하는 쿼리를 작성해주세요  
![image](https://github.com/user-attachments/assets/8b4471c0-8473-42f6-bd84-e5ccb8bbab4d)
3. trainer 테이블에 있는 트레이너의 name, age를 출력하는 쿼리를 작성해주세요  
![image](https://github.com/user-attachments/assets/90a866c4-6814-4feb-a259-3eaa7a9ec362)
4. trainer의 테이블에서 id가 3인 트레이너의 name, age, hometown을 출력하는 쿼리를 작성해주세요
![image](https://github.com/user-attachments/assets/ec859706-0e14-4428-b197-4f8caa22df55)
5. pokemon 테이블에서 '피카츄'의 공격력과 체력을 확인할 수 있는 쿼리를 작성해주세요
![image](https://github.com/user-attachments/assets/627b492d-27a2-40d6-8173-6aec3d2a6efd)
# 2-5. 집계(Group by + having + sum/count) 
#### 집계와 그룹화
모아서 계산하다 => 그룹화해서 계산하다  
<계산>  
- 더하기, 빼기  
- 최댓값, 최솟값   
- 평균  
- 갯수 세기
#### 집계 : GROUP BY
같은 값끼리 모아서 그룹화한다.    
EX) 포켓몬의 타입별 평균 공격력  
![image](https://github.com/user-attachments/assets/d66e2ad8-4cfd-438b-a67b-88787af08b58)
#### 고유값을 알고 싶은 경우
DISTINCT : 별개의 여러 값 중에 unique한 것만 보고 싶은 경우 사용  
EX) 포켓몬 타입들의 유니크 값  
![image](https://github.com/user-attachments/assets/731a161f-6b0d-4671-b18a-7cb71b04be6c)  
####  GROUP BY 연습문제
1. pokemon 테이블에 있는 포켓몬 수를 구하는 쿼리를 작성해주세요  
![image](https://github.com/user-attachments/assets/88603e34-b8d4-480a-8017-5a5a1a10ea68) 
2. 포켓몬의 수가 세대별로 얼마나 있는지 알 수 있는 쿼리를 작성해주세요
![image](https://github.com/user-attachments/assets/d8330ace-d24d-413f-86cb-c1a5217f10d1)
#### 조건을 설정하고 싶은 경우  
WHERE : Table에 조건을 바로 설정하고 싶은 경우 사용  
HAVING : GROUP BY한 후 조건을 설정하고 싶은 경우 사용  
#### 서브쿼리
<서브쿼리>
- SELECT문 안에 존재하는 SELECT쿼리  
- FROM절에 또다른 SELECT 문을 넣을 수 있음  
- 괄호로 묶어서 사용  
#### 정렬하기
ORDER BY  
DESC: 내림차순 OSC: 오름차순(기본 설정)  
#### 출력개수 제한하기
LIMIT =>쿼리문의 제일 마지막에 작성
#### GROUP BY 연습문제
3.포켓몬의 수를 타입별로 집계하고, 포켓몬수의 수가 10이상인 타입만 남기는 쿼리를 작성해주세요. 포켓몬의 수가 많은 순으로 정렬해주세요
![image](https://github.com/user-attachments/assets/534120da-651a-4f7a-a97f-32d9223a7762)


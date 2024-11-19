# 6-1. Intro
# 6-2. 가독성을 챙기기 위한 SQL 스타일 가이드
## 실수는 언제 발생하는가?
- 문법을 잘못 알고있을 경우 => 문법 공부  
- 데이터를 파악하지 않고 쿼리를 작성하는 경우 => 데이터 파악
- 쿼리가 복잡한 경우 => 쿼리 단순화
## 가독성을 챙기는 법
### 1.예약어는 대문자로 작성
SELECT, FROM, WHERE, 각종 함수 등
### 2.컬럼 이름은 snake_case로 작성
_을 사용하는 것
### 3.명시적인 이름을 사용
Alias 사용시 AS a, As b등 보다는 명시적으로 표현
### 4.기본적으로 왼쪽 정렬을 기준으로 작성  
SELECT  
 col  
FROM table  
WHERE 1=1  
### 5.예약어나 컬럼은 한 줄에 하나씩 권장
컬럼은 바로 주석처리 할 수 있는 장점이 있기에 한 줄에 하나씩 작성
### 6.쉼표는 컬럼 바로 뒤에
이 부분은 의견이 갈리기 때문에(앞vs뒤) 회사 사람들에게 물어보면 좋음
# 6-3. 가독성을 챙기기 위한 WITH 문 & 파티션
## WITH 문
- SQL 쿼리를 작성하다 생긱는 일 => 점점 복잡해짐(가독성 하락) 
- SELECT 구문에 이름을 정해준는 것과 유사 
- 쿼리 내에서 반복적으로 사용 가능  
![image](https://github.com/user-attachments/assets/c766ff87-12e7-4ec9-8a58-77ba51ad5711) 
WITH를 사용해서 쿼리를 sample로 저장하고 이를 다시 불러왔다.
![image](https://github.com/user-attachments/assets/30283fc8-d417-456a-a73c-b941fc7aa74d) 
## PARTITON 장점
1. 쿼리성능 향상 => 전체 데이터를 스캔하는 것보다 파티션을 설정한 곳만 스캔하는 것이 더 빠름
2. 데이터 관리 용이성 => 특정 일자의 데이터를 모두 변경하거나 삭제해야 하면 파티션을 설정해서 삭제할 수 있음
3. 비용 => 파티션에 해당하는 데이터만 스캔해서 비용을 줄일 수 있음
![image](https://github.com/user-attachments/assets/231243e5-09e8-46a7-bd36-1692ac94df4f) 
파티션을 사용하면 오른쪽 위에 사용할 용량이 나타난다.
# 6-4. 데이터 결과 검증 정의
데이터 결과 검증: SQL 쿼리 후 얻은 결과가 예상과 일치하는지 확인하는 과정
1. COUNT(*) : 행 수를 확인. 의도한 데이터의 행 개수가 맞는가?
2. NOT NULL :특정 컬럼에 NULL이 존재하는가? 필수 필드가 비어있지 않는가?
3. DISTINCT : 데이터의 고윳값을 확인해 중복 여부 확인
4. IF문, CASE WHEN : 의도와 같다면 TRUE, 아니면 FALSE   
# 6-5. 데이터 결과 검증 예시
쿼리를 점점 구체화 해나간다.
![image](https://github.com/user-attachments/assets/62e8575a-b1e4-43ca-8275-7584942edf59) 
![image](https://github.com/user-attachments/assets/2a64a838-cdd5-4ec4-8fb5-80f99b7a3a04) 
![image](https://github.com/user-attachments/assets/2ffe27ae-ecb5-4ab8-a97e-f54b3f2e24d9) 
![image](https://github.com/user-attachments/assets/3dae9dfa-3b72-4ea5-8576-20fdd04c8a67) 
# 6-6. 정리

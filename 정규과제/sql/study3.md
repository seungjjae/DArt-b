# 2-6. 연습문제 1~3번 
#### 1.포켓몬 중에 type2가 없는 포켓몬의 수를 작성하는 쿼리를 작성해주세요
힌트: ~가 없다=> IS NULL
![image](https://github.com/user-attachments/assets/8c045de5-5aad-417b-9160-7ca777e038f8)
WHERE절에서 여러 조건을 연결하고 싶은 경우 => AND 조건을 사용  
OR 조건 => ( ) OR ( )  
#### 2.type2가 없는 포켓몬의 type1과 type1의 포켓몬 수를 알려주는 쿼리를 작성해주세요.
단, type1의 포켓몬 수가 큰 수으로 정렬해주세요.  
![image](https://github.com/user-attachments/assets/a3689f98-f21d-47cc-a3ae-3449407c40bd)
#### 3.type2 상관없이 type1의 포켓몬 수를 알 수 있는 쿼리를 작성해주세요
![image](https://github.com/user-attachments/assets/fecf0787-865a-4347-bf7c-4f31ea9dfcd8)
어떤 컬럼은 중복되어 있게 설계된다. 따라서 count(id)와 count(distinct id)를 적절하게 사용
# 2-6. 연습문제 4~6번 
#### 4.전설 여부에 따른 포켓몬의 수를 알 수 있는 쿼리를 작성해주세요.
![image](https://github.com/user-attachments/assets/a41008ce-cc9c-4024-b705-4f9a955a6b52)
GROUP BY 1=> SELECT의 첫 컬럼을 의미  
여기선 GROUP BY 1으로 해도 결과가 같게 나온다.
#### 5.동명 이인이 있는 이름은 무엇일까요?
![image](https://github.com/user-attachments/assets/0cc21721-6b6c-426f-9a62-4daeea49ce14)
HAVING을 사용해 마지막에 조건을 한번 더 걸어 필터링한다.
![image](https://github.com/user-attachments/assets/a3d1ff9a-c006-4cba-b8ca-38456acb98a4)
HAVING이 아닌 서브쿼리를 사용하여 푼방법. 결과는 동일하다.
#### 6. trainer 테이블에서 'Iris' 트레이너의 정보를 알 수 있는 쿼리를 작성해주세요
![image](https://github.com/user-attachments/assets/4a8103ec-1115-449b-98f3-9683f49bbfb2)
# 2-6. 연습문제 7~9번 
#### 7.trainer 테이블에서 'Iris', 'Whitney', 'Cynthia' 트레이너의 정보를 알 수 있는 쿼리를 작성해주세요  (힌트) 컬럼 IN('Iris', 'Whitney', 'Cynthia')
![image](https://github.com/user-attachments/assets/f7d9a7dc-7d0a-48ad-93ad-ae74510b5e4d) 
or절을 사용해서도 풀 수 있다. 하지만 길이가 길어진다.
#### 8.전체 포켓몬 수는 얼마나 되나요?
![image](https://github.com/user-attachments/assets/2cd1d405-c660-4029-b5ba-51f3a5b7d10e)
#### 9. 세대(generation)별로 포켓몬 수가 얼마나 되는지 알 수 있는 쿼리를 작성해주세요
![image](https://github.com/user-attachments/assets/1bda6132-fd70-47fc-bb76-ebd44f571146)
# 2-6. 연습문제 10~12번 
#### 10.type2가 존재하는 포켓몬의 수는 얼마나 되나요?
![image](https://github.com/user-attachments/assets/8ab9f884-cec5-42ec-8d0a-8ca2b30025d5)
#### 11.type2가 있는 포켓몬중에 제일 많은 type1은 무엇인가요?
![image](https://github.com/user-attachments/assets/bd073eec-ff6a-4ae8-9303-edb487416280)
#### 12.단일 타입 포켓몬 중 많은 type1은 무엇일까요?
![image](https://github.com/user-attachments/assets/9a1699a3-aba9-4626-8089-575a9c0237fa)  
# 2-6 연습문제 13~17번 
#### 13.포켓몬의 이름에 '파'가 들어가는 포켓몬은 어떤 포켓몬이 있을까요?  (힌트) 컬럼 LIKE '파%'
![image](https://github.com/user-attachments/assets/e2ca61ce-fa47-4b5b-8965-a23bca2802e0)  
'%파' => 파로 끝나는 단어  
'파%' => 파로 시작하는 단어
'%파%' => 파가 들어가는 단어
#### 14.뱃지가 6개 이상인 트레이너는 몇 명이 있나요?
![image](https://github.com/user-attachments/assets/094288ce-7a67-4146-8bd9-c360bcd92c87)  
#### 15.트레이너가 보유한 포켓몬이 제일 많은 트레이너는 누구일까요?
![image](https://github.com/user-attachments/assets/13e90f16-9b17-45c1-aaf3-a99ac245b090)    
DISTINCT를 사용하여 중복이 있는지 없는지 확인하는 습관을 가지면 좋다
#### 16.포켓몬을 많이 풀어준 트레이너는 누구일까요?
![image](https://github.com/user-attachments/assets/bbb82b61-b40a-4b9d-b0e5-085e89ee0876)  
#### 17.트레이너 별로 풀어준 포켓몬의 비율이 20%가 넘는 포켓몬 트레이너는 누구일까요?  풀어준 트레이너의 비율=(풀어준 포켓몬 수/전체 포켓몬 수)  힌트)COUNTIF(조건)
![image](https://github.com/user-attachments/assets/8f8084e8-70b6-4435-b51a-7aa5cdf3da26)  
COUNTIF(조건) : 조건에 해당하는 것만을 카운팅
# 2-7. 정리 
![image](https://github.com/user-attachments/assets/dccef822-5b52-4c59-9dae-96a338140098)  
조건과 추출, 요약할때 사용하는 쿼리를 배웠다.  
외에도 DISTINCT, LIKE'%파%', IN(), COUNTIF 등을 배웠다.
# 2-8. 새로운 집계 함수
GROUP BY ALL: 따로 GROUP BY '변수1', '변수2'로 쓰지 않고 한번에 모두 그룹화 하는 코드
![image](https://github.com/user-attachments/assets/af67894e-1e6f-4cb9-9945-6b968b583e27)
위의 17번 문제에 적용해봤는데 동일하게 값이 나온다.
# 3-1. INTRO
흐름을 이해해서 쿼리를 깔끔하게 정리하는 방법에 대해 배울것이다.
# 3-2. SQL 쿼리 작성하는 흐름
![image](https://github.com/user-attachments/assets/ae24a169-e2eb-4ae9-aff6-d891f1619223)
쿼리 작성에만 몰두하는 것이 아니라 그 앞뒤 단계 모두를 고려하면서 쿼리를 작성해야 한다.
# 3-3. 쿼리 작성 템플릿과 생산성 도구
#### 쿼리 작성 템플릿  
- 쿼리를 작성하는 목표, 확인할 지표
- 쿼리 계산 방법  
- 데이터의 기간  
- 사용할 테이블  
- join KEY  
- 데이터 특징
=> 위 사항을 습관화하여 항상 고려하면 좋지만 귀찮아서 까먹게됨  
=> 생산성 도구 사용 : Espanso
#### Espanso
특정 단어를 입력하면 원하는 문장(템플릿)으로 변경해 준다.  
즉 특정 단어가 감지되면 정의된 것으로 바꾼다는 것이다.  
함께 사용하면 쿼리 작성에 많은 도움이 된다!

## [전복 나이 예측 대회](https://dacon.io/competitions/official/235877/overview/description)
![image](https://user-images.githubusercontent.com/97036411/190851689-48720f03-5a14-404d-bb11-38d6bc590e23.png)

  
- 데이터 : 전복 성별, 길이, 무게 등에 대한 데이터 (target : 전복 나이)
  - train 1253개, test 2924개 데이터
  - 총 9개의 컬럼 (target 데이터 제외)
  
  
  
📌 **시도한 feature engineering, 점수**
| No | DATE | MODEL | TRY | SCORE | CHECK |
| --- | --- | --- | --- | --- | --- |
| 1 | 3/28 | RandomForest | 이상치 제거 | 0.1539 |  |
| 2 | 3/29 | voting | 성별 합친 후 라벨 인코딩, 이상치 제거 | 0.231 |  |
| 3 | 3/31 | bagging | 성별 합친 후 라벨 인코딩, 이상치 제거, prediction 값 정수로 변환 | 0.160 |  |
| 4 | 3/31 | catboost | 성별 합친 후 라벨 인코딩, 이상치 제거, prediction 값 정수로 변환 | 0.151 |  |
| 5 | 3/31 | voting | 성별 합친 후 라벨 인코딩, 이상치 제거, prediction 값 정수로 변환 | 0.148 |  |
| 6 | 4/1 | voting | 성별 합친 후 라벨 인코딩, 이상치 제거, prediction 값 정수로 변환, target 로그변환 | 0.147 | ✔ |

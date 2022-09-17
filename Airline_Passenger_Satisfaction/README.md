## [항공사 고객 만족도 예측대회](https://dacon.io/competitions/official/235871/overview/description)
![image](https://user-images.githubusercontent.com/97036411/153756631-16de8319-b4d0-4534-9683-e55814d9b0e8.png)
  
  
- 데이터 : 항공사 고객의 정보와 항공사에 대한 만족도 여부 데이터
  - train 3000개, test 2000개 데이터
  - 총 22개의 컬럼 (test 데이터 기준 / train 데이터에는 만족 여부 컬럼까지 총 23개)
---

📌 **시도한 feature engineering, 점수**
| No | DATE | MODEL | TRY | SCORE | CHECK |
| -- | ---- | ----- | --- | ----- | ----- |
| 1 | 2/9 | Random Forest | 라벨인코딩, 상관계수 낮은 feature 제거(+다중공선성) | 0.921 |  |
| 2 | 2/13 | Catboost | 이상치 평균으로 대체 시도, 라벨인코딩, 상관계수 낮은 feature 제거 | 0.934 |  |
| 2 | 2/13 | Random Forest | 이상치 평균으로 대체 시도, 라벨인코딩, 상관계수 낮은 feature 제거 | 0.908 | |
| 2 | 2/13 | LightGBM | 이상치 평균으로 대체 시도, 라벨인코딩, 상관계수 낮은 feature 제거 | 0.924 | |
| 3 | 2/16 | Catboost | 라벨인코딩, 로그변환, 상관계수 낮은 feature 제거 | 0.941 | √ |
| 3 | 2/16 | Catboost | 원핫인코딩, 로그변환, 상관계수 낮은 feature 제거 | 0.94 | |
| 4 | 2/18 | Catboost | 0.941데이터 + score 0 대체 처리 | 0.937 | |
| 5 | 2/18 | Catboost | 0.941데이터 + score 0 대체 처리 + age 구간 나눔, 원핫인코딩 | 0.935 | |

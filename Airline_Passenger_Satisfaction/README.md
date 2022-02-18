# DACON Competition 1
## Airline_passenger_Satisfaction
![image](https://user-images.githubusercontent.com/97036411/153756631-16de8319-b4d0-4534-9683-e55814d9b0e8.png)

| No | DATE | MODEL | TRY | SCORE | CHECK |
| -- | ---- | ----- | --- | ----- | ----- |
| 1 | 2/9 | Random Forest | 라벨인코딩, 상관계수 낮은 feature 제거(+다중공선성) | 0.921 |  |
| 2 | 2/13 | Catboost | 이상치 평균으로 대체 시도, 라벨인코딩, 상관계수 낮은 feature 제거 | 0.934 |  |
| 2 | 2/13 | Random Forest | 이상치 평균으로 대체 시도, 라벨인코딩, 상관계수 낮은 feature 제거 | 0.908 | |
| 2 | 2/13 | LightGBM | 이상치 평균으로 대체 시도, 라벨인코딩, 상관계수 낮은 feature 제거 | 0.924 | |
| 3 | 2/16 | Catboost | 라벨인코딩, 로그변환, 상관계수 낮은 feature 제거, Catboost 첫 사용 | 0.941 | √ |
| 3 | 2/16 | Catboost | 원핫인코딩, 로그변환, 상관계수 낮은 feature 제거 | 0.94 | |
| 4 | 2/18 | Catboost | 0.941데이터 + score 0 대체 처리 | 0.937 | |
| 5 | 2/18 | Catboost | 0.941데이터 + score 0 대체 처리 + age 구간 나눔, 원핫인코딩 | 0.935 | |

## private score
![20220218_161553](https://user-images.githubusercontent.com/97036411/154637416-d8d20b5e-35c4-4c58-8fe6-b763971ed149.png)
첫 대회라 빈약한 부분들이 많이 있다.  
이번 대회는 생각보다 오히려 전처리를 단순하게 했을 때 score가 높은 듯하다.

# DACON Competition 1
## Airline_passenger_Satisfaction
![image](https://user-images.githubusercontent.com/97036411/153756631-16de8319-b4d0-4534-9683-e55814d9b0e8.png)

| No | MODEL | SCORE |
| -- | ----- | ----- |
| 1 | Random Forest | 0.921 |
| 2 | Catboost | 0.934 | 

3번째 시도에 해봐야 할 것 (~ 2/16)
* score 0 처리 (최빈값 또는 다른 방향으로 진행)
* [이상치 처리하기](https://hungryap.tistory.com/69)
* object feature : 0, 1로 변경하여 진행
* Class feature : Eco, Eco Plus 분포 확인하여 하나로 묶기, 묶기 어려우면 One-Hot-Encoding 진행 (+Age)
* 모델 앙상블 진행 ([사이킷런 앙상블](https://teddylee777.github.io/scikit-learn/scikit-learn-ensemble))
** 참고 URL : https://www.kaggle.com/mehmetbicici/airline-passenger-satisfaction-eda-ml

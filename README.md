## Dacon 운동 동작 분류 AI 경진대회 최종 제출 코드입니다.
이 대회는 3축 가속도계(accelerometer)와 3축 자이로스코프(gyroscope)를 활용해 측정된 센서 데이터를 기반으로 운동 동작 분류를 머신러닝으로 해결하고자 한 대회입니다.
순위 평가 기준은 LogLoss입니다.

데이터는 dacon 홈페이지에서 얻을 수 있습니다.
https://dacon.io/competitions/official/235689/data/

#### 대회 참여가 좀 늦었는데  남은 기간이 1/3일 때 참여하였습니다.
처음 단순한 LSTM 모델 베이스라인을 돌려보니 등수가 굉장히 낮았고  
LSTM으로 parameter를 바꿔서 몇 번 돌려봤는데도 점수가 굉장히 낮았습니다.  
그래서 구글에 검색 중에 multivariate time series classification을 검색하여 LSTM-FCN이란 모델을 알게 되었고,  
모델을 만든 결과 성능이 비슷하였습니다.  
그래서 지난 대회를 참고하던 중에 음성 중첩 데이터 분류 AI경진대회를 참고하게 되었습니다.
음성 신호와 가속도계 센서 신호의 시간에 따라 변하고 주기적인 성질을 가지는 공통점에 주목하여
음성 대회와 같은 방법으로 접근하면 어떨까 하여
음성 중첩 데이터 분류 AI경진대회 우승자의 코드 1d-cnn으로 모델을 구현하였습니다.
그 결과 점수는 상위권으로 바뀌었고, 모델 앙상블을 통해 10%안에 들게 되었습니다.



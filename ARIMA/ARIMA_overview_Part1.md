# 성은([vg-rlo](https://github.com/vg-rlo))
## Differencing 부분에서 3차 미분하는 경우는 거의 없고 해당 경우엔 ARIMA 모델이 적합하지 않다고 합니다. 그럼 ARIMA로 모델링할 수 없는 케이스의 Non stationary series data는 어떤 모델을 사용하는지 궁금합니다.

# 이삭([IsaacTips](https://github.com/IsaacTips))

## ARIMA모델을 사용하려면 왜 Stationary 해야 하는가?(내가 잘 이해했는지 확인용 질문ㅋㅋ)

좀 더 찾아볼 예정

# 인유([willowlkim8](https://github.com/willowkim8))

## nonstationary data 를 모델링할 때, AR, MA 등 쓴다고 했는데, 차분 후에는 앞서 말한 모델이 잘 되지 않는건가?

# 민정([miinkang](https://github.com/miinkang))
## 알게된 점
ARIMA모델링 시에 차분을 하는 기준에 대해 알지 못했었는데 데이터의 특성에 따라 차분 횟수를 정하는 기준에 대해 알게 되었다. 
1. 데이터가 일정하게 증가하거나, 감소하는 경향이 있을 경우 : **1차** 차분
2. 복잡한 데이터의 경우 : **2차** 차분
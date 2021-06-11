# 성은([vg-rlo](https://github.com/vg-rlo))
Moving Average 모델과 Auto Regression 모델들의 auto covariance, auto correlation function을 유도하여 해당하는 모델이 h 값의 범위에 따라 cutoff 되는 지점을 찾는 법을 배울 수 있었다. 
앞선 강의에서 ACF(Auto Correlation Function)과 PACF(Partial ..)로 적절한 P, Q, D를 찾는 방법을 공부했는데 이 부분을 수식으로 증명해내는 과정이 어렵게 느껴졌다. 

# 이삭([IsaacTips](https://github.com/IsaacTips))

## 얕은 개념 정리

*모델 뒤에 붙은 숫자는 파라미터수*

* MA : white noise의 linear combination으로 현재 시점을 예측하겠다는 모델
    * MA(2) : 파라미터가 2개. 두 시점 전의 white noise 정보를 가지고 현재 시점을 예측한다
* AR : $X_{t}$를 자기 자신의 과거로 모델링.
    * AR(2) : 두 시점 뒤의 데이터를 가지고 모델링.

# 인유([willowlkim8](https://github.com/willowkim8))

## 시계열에서 화이트 노이즈란?

# 민정([miinkang](https://github.com/miinkang))

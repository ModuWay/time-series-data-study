# 성은([vg-rlo](https://github.com/vg-rlo))
Prediciton Interval(예측구간): 특정한 확률로 y_t가 들어갈 구간을 의미    
ARIMA 모델에 대한 예측 구간에 대한 가정     
* 잔차에 상관관계가 없다. 
* 잔차가 정규분포를 따른다. 

가정을 만족하는지 확인하는 방법 
* ACF
* 잔차의 히스토그램     
[참고자료](https://otexts.com/fppkr/prediction-intervals.html)

# 이삭([IsaacTips](https://github.com/IsaacTips))

## Partial autocorrelation function (PACF)
* PACF는 두 변수사이의 correlation.
* 두개 외의 다른 변수까지 고려한 correlation.

# 인유([willowlkim8](https://github.com/willowkim8))

### 어떻게 예측을 하는지 수식으로 설명

# 민정([miinkang](https://github.com/miinkang))
1부터 t시점까지의 x가 있을 때, 우리는 t+1시점의 x를 예측하고자 한다.    
이때, 예측하기 위해서 실제값과 예측값의 차이인 error를 최소화시킨다.   
최소화시키기 위한 식에서 조건부 기댓값(평균)을 사용한다는 점이 중요하다.   

![image](https://user-images.githubusercontent.com/68461606/124343265-27772900-dc05-11eb-8f5d-282705865888.png)


본 강의에서는 AR, ARMA모델을 이용해 예측하는 과정을 수식으로 증명하고 있다. 

# 성은([vg-rlo](https://github.com/vg-rlo))

##  Q. ~~Time series data를  Regression에  적용하기 위해서~~ Time series data를 ordinary regression으로 분석하기 위해 transformation 해주는데 correlation을 없애주기 위함인지 궁금하다. 
**magnitude of the seasonal swing depends on the level of time series**
=> increasing seasonal variation     
Transformation을 해줄때 Square root transformation과 Log transformation으로 increase한 magnitude를 constant하게 바꿔준다.    
회귀모델링을 하기 위해 평균과 분산은 시점에 의존하면 안된다. 따라서 분산이 일정하지 않은 시계열은 변환을 통해 정상화할 수 있다. 이때, 주로 Log transformation을 사용한다. 공분산(covariance)도 시차에만 의존하고 특정 시점에 의존하지 않는다.     

- 링크 
[시계열분석의 개념](https://analysis-flood.tistory.com/17)
[ADP 시계열 분석](https://ckmoong.tistory.com/7)   

## Q. 오차, 잔차 차이에서모집단/표본집단인 상황이 어떻게 구분되는지와  '회귀모형에서 오차항은 측정할 수 없으므로'라는 부분이 궁금하다. 
모집단과 표본집단
* 대부분의 상황에서 표본집단에서 회귀식을 얻는다. => 강의에서도 표본집단 케이스를 예시로 들음 

오차의 정의
* 모집단에서 회귀식을 얻었다면, 그 회귀식을 통해 얻은 예측값과 실제 관측값의 차이 

잔차의 정의 
* 표본집단에서 회귀식을 얻었다면 그 회귀식을 통해 얻은 예측값과 실제 관측값의 차이 
* 회귀 모형에서 오차항은 측정할 수 없으므로 잔차를 오차항의 관찰값으로 해석하여 오차항에 대한 가정들의 성립 여부를 조사함

## Q. 최소제곱법 왜 사용해주는지 
최소제곱법 
* 일반적으로 회귀모델에서 최소제곱법을 활용한다. 
* 잔차들의 제곱들을 더한 것을 최소로 만들어주는 파라미터(아래 수식에서의 Beta)를 찾는 것이 최적의 회귀식을 찾는 것이다. 
![image](https://user-images.githubusercontent.com/69677950/115814726-962f4d80-a430-11eb-9d4e-32cdabdbd0ed.png)

- 링크 
[최소제곱추정](https://otexts.com/fppkr/least-squares.html)    
[선형대수학 최소제곱법](https://bskyvision.com/236)

# 이삭([IsaacTips](https://github.com/IsaacTips))

## Q. Increasing seasonal variation은 Stationary Regression Model로 핸들링이 어렵다. 그래서, Constant하게 바꿔주고 모델링을 해야하는데, 이 과정에서 데이터의 특징이 사라지지 않을까??
---

강의에서는 공분산이 0이어야 stationary regression 모델을 사용할 수 있다고 하였다.

> Cov(X, Y) = 0 공분산이 0이라면 두 변수간에는 아무런 선형관계가 없으며 두 변수는 서로 독립적인 관계에 있음을 알 수 있다. 그러나 두 변수가 독립적이라면 공분산은 0이 되지만, 공분산이 0이라고 해서 항상 독립적이라고 할 수 없다. [참고](https://destrudo.tistory.com/15)

반면에 Increasing seasonal variation은 magnitude of the seasonal swing이 계속 증가하는 형태이기 때문에, [stationary time series 기준](https://seoncheolpark.github.io/book/_book/17-1-stationary-time-series.html)에 맞지 않다. 

<img src="./image/increasing.png" />
<center>increasing seasonal variation. 갈 수록 증가폭이 커지고 있다.</center>

# 인유([willowlkim8](https://github.com/willowkim8))

회귀 모델
y_t=TR_t+\epsilon_t
위의 식에서 TR은 trend, 추세이다.  
이때 추세가 없는 경우에는 일정한 값으로 예측하거나, prediction interval로도 예측 가능하다.  

Q. alpha가 있을 때 prediction interval 구할 수 있다고 했는데, 이때 alpha는 무엇인가?
>prediction interval(PI)는 confidence interval(CI)와 함께 신뢰구간을 뜻한다.  
100(1-$\alpha$)%로 신뢰구간을 구하는 것이고, $\alpha$는 사용자가 지정하면된다.  

회귀모델을 쓰려면 epsilon들이 서로 다른 시점에서 독립이어야 한다.  
당연히 위배될 가능성이 크다.  
=> Autocorrelation으로 회귀 모델을 쓸 수 있을지 확인 가능하다.  
auto = self, co = two, 이 의미를 통합하면 스스로 2가지를 모양을 하고 관계를 한다는 것이다.  
그 2가지 모양은 original과 shifted 모양이다.  
Autocorrelation이 0이면 일반적인 회귀 모델을 쓸 수 있지만,  
0이 아니라면 최소 제곱 사용할 수 없고 회귀 모델을 쓸 수 없다.

Increasing Seasonal variation은 루트와 로그로 해결하는데, 로그가 더 많이 사용된다.


# 민정([miinkang](https://github.com/miinkang))

- 일반적인 regression 모델을 사용하기 위해서는 다음 가정이 성립해야한다.   
![image](https://user-images.githubusercontent.com/68461606/115803587-28792680-a41c-11eb-8bde-24d3e26be347.png)
두 변수의 공분산이 0, 독립관계여야한다.   
time series data의 경우 해당 가정이 성립하지 않을 확률이 크다.   
시간에 종속되어있는 데이터의 특성상, 시간의 흐름에 따라 다음 값에 영향을 줄 수 있기 때문이다.   
따라서, 해당 가정의 성립여부를 파악하기 위해 autocorrelation이 있는지 확인한다.   
- autocorrealtion이란?    
: x데이터를 time shift를 이용해 x'데이터를 만들어 x, x' 두 변수의 관계를 표현한 측도를 말한다. 
검정 방법 중 대표적인 Durbin-Watson Test를 사용할 수 있다.   

autocorrelation이 없다면, 공분산이 0이라는 가정이 성립하기에 일반적인 회귀모델을 사용할 수 있다. 
그렇지 않다면 사용할 수 없다.   

---

이번 강의에서는 autocorrelation을 확인하는 이유와 검정방법에 대해 알아볼 수 있었다. 

## Q. residual과 error term의 차이점    
**The Difference Between Error Terms and Residuals**     
Although the error term and residual are often used synonymously, there is an important formal difference. An error term is generally unobservable and a residual is observable and calculable, making it much easier to quantify and visualize. In effect, while an error term represents the way observed data differs from the actual population, a residual represents the :way observed data differs from sample population data.    
출처 : [Error Term](https://www.investopedia.com/terms/e/errorterm.asp#:~:text=The%20Difference%20Between%20Error%20Terms%20and%20Residuals&text=In%20effect%2C%20while%20an%20error,differs%20from%20sample%20population%20data)      

- 공유받은 링크    
[오차와 잔차](https://m.blog.naver.com/PostView.nhn?blogId=jmzzang4004&logNo=100050479647&proxyReferer=https:%2F%2Fwww.google.com%2F)    
[잔차 진단](https://otexts.com/fppkr/residuals.html)    
[모집단과 표본집단](https://m.blog.naver.com/PostView.nhn?blogId=istech7&logNo=50151725609&proxyReferer=https:%2F%2Fwww.google.com%2F)    

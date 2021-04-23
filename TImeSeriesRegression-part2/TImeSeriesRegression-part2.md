# 성은([vg-rlo](https://github.com/))
# 이삭([](https://github.com/))
# 인유([](https://github.com/))
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
- error term : 모집단(population)에서 얻은 예측값과 실제 관측값의 차이
- residual : 표본집단(sample)에서 얻은 예측값과 실제 관측값의 차이    
해당 강의에서는 모집단이 없는 경우이기 때문에 error term을 직접 확인할 수 없어서 residual을 통해 autocorrelation을 확인한다고 설명한다.     

**The Difference Between Error Terms and Residuals**     
Although the error term and residual are often used synonymously, there is an important formal difference. An error term is generally unobservable and a residual is observable and calculable, making it much easier to quantify and visualize. In effect, while an error term represents the way observed data differs from the actual population, a residual represents the :way observed data differs from sample population data.    
출처 : [Error Term](https://www.investopedia.com/terms/e/errorterm.asp#:~:text=The%20Difference%20Between%20Error%20Terms%20and%20Residuals&text=In%20effect%2C%20while%20an%20error,differs%20from%20sample%20population%20data)      

- 공유받은 링크    
[오차와 잔차](https://m.blog.naver.com/PostView.nhn?blogId=jmzzang4004&logNo=100050479647&proxyReferer=https:%2F%2Fwww.google.com%2F)    
[잔차 진단](https://otexts.com/fppkr/residuals.html)    
[모집단과 표본집단](https://m.blog.naver.com/PostView.nhn?blogId=istech7&logNo=50151725609&proxyReferer=https:%2F%2Fwww.google.com%2F)    

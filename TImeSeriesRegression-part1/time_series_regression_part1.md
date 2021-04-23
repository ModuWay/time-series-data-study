# 시계열 데이터 
* 시간의 흐름에 따라 순서대로 관측되어 시간의 영향을 받게 되는 데이터 
    - e.g. 일, 달, 분기(Quarterly), 년

## 시계열 데이터 구성요소
* Trends 
* Cycle 
* Seasonal variations 
* Random fluctuation

## Prediction Error(예측오차) 
* MAD(평균절대편차)
* MSE(평균제곱편차)
* MAPE(Mean Absolute Percentage Error)

---
# 질의 응답
#### [miinkang] 데이터 계절성의 종류에서 multiplicative와 additive seasonality가 무엇인지 
시계열 데이터에 대한 예제를 소개하는 강의 앞부분에서, 시간의 흐름에 따라 데이터가 점진적으로 증가한 예시를 multiplicative라고 합니다.  
![image](https://user-images.githubusercontent.com/68461606/114884130-7b614580-9e40-11eb-8dc8-7614544af5de.png)   

서치한 답변!  
The general definition of additive or multiplicative seasonality is: level + seasonal indices, or level x seasonal indices. Effectively, with multiplicative seasonality the width of the seasonal pattern is proportional to the level. For additive seasonality it is independent.    

포인트는   
- additive seasonality = level + seasonal indices
- multiplicative seasonality = level * seasonal indices

#### [vg-rlo] 증가 여부로만 판단하지 않고 additive인지 multiplicative인지는 구성요인간의 독립 여부에 따라 판단합니다. 
[서치한 답변!](https://www.r-bloggers.com/2017/02/is-my-time-series-additive-or-multiplicative/)    
In a multiplicative time series, **the components multiply together** to make the time series. If you have an increasing trend, the amplitude of seasonal activity increases. Everything becomes more exaggerated. This is common when you’re looking at web traffic.    
In an additive time series, the components add together to make the time series. If you have an increasing trend, you still see roughly the same size peaks and troughs throughout the time series. This is often seen in indexed time series where the absolute value is growing but changes stay relative.    
    
[서치한 답변!](https://blog.naver.com/lcs5382/222146079975)    
- additive(가법)는 구성요인간 독립적이라고 가정하고 각 구성요인들을 더합니다. 
	* origin = trend + seasonal + residual 	
- multiplicative(승법)는 구성요인간 상호의존적이라고 가정하고 구성요인들간 곱해줍니다. 
	* origin = trend * seasonal * residual

#### [miinkang] 비트 트레이더 대회에서 분석 및 예측하는 비트코인 데이터는 둘 중 어디에 속할까에 대해 다시 고민해봐야할 것 같습니다. 
이전에 이삭님께 질문했었는데, 계절성은 없지만 점진적으로 증가하는 축에 속할 것 같다라는 답변을 얻었습니다.    

#### [vg-rlo] 가상화폐의 가격 흐름이 seasonal하다면, 가격을 예측하는 경우 트렌드에 맞게 seasonal 데이터를 예측할 수 있는 multiplicative가 적절합니다. 
[시계열 데이터 기초관련 정리 블로그](https://be-favorite.tistory.com/62), [서치한 답변!](https://dodonam.tistory.com/89)
additional/multiplicative 모두 data가 seasonal하다고 전제할 때 Trend와 seasonality가 상호 연관성을 가지는지 여부에 따라 선택하여 사용하게 됩니다. 상호연관성은 데이터의 크기에 따라 계절 패턴 크기가 달라지는 경우를 의미합니다.

* seasonal decomposition으로 non-stationary한지 확인 => trend/seasonality 성분 가질 수 있음 
* seasonality를 가지는지 확인 [확인방법1](https://danielykim.github.io/articles/2016/11/23/ESH-06-04-04-03/), [확인방법2](https://statkclee.github.io/statistics/stat-forecast-automation.html)
* Trend와 Seasonality과 상호 연관성 가지는지에 따라 additive/multiplicative 선택

---


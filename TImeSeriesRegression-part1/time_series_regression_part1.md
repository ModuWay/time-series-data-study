# 데이터 계절성의 종류 
![image](https://user-images.githubusercontent.com/68461606/114884130-7b614580-9e40-11eb-8dc8-7614544af5de.png)   
시계열 데이터에 대한 예제를 소개하는 강의 앞부분이었습니다.  
이렇게 시간에 흐름에 따라 데이터가 점진적으로 증가하는 데이터를 multiplicative라고 합니다.   

서치한 답변!  
The general definition of additive or multiplicative seasonality is: level + seasonal indices, or level x seasonal indices. Effectively, with multiplicative seasonality the width of the seasonal pattern is proportional to the level. For additive seasonality it is independent.    

포인트는   
- additive seasonality = level + seasonal indices
- multiplicative seasonality = level * seasonal indices

대회에서 분석 및 예측하는 비트코인 데이터는 둘 중 어디에 속할까에 대해 다시 고민해봐야할 것 같습니다.   
이전에 이삭님께 질문했었는데, 계절성은 없지만 점진적으로 증가하는 축에 속할 것 같다라는 답변을 얻었습니다.   
함께 토의해보아요! 

---
(구분선 위에 작성해주세요.)


* 본 강의노트는 김성범 교수님의 유투브 강의를 바탕으로 작성했음을 밝힙니다.
* 강의 링크: youtu.be/7Do_hixXCpc


# 시계열 데이터 
* 시간의 흐름에 따라 순서대로 관측되어 시간의 영향을 받게 되는 데이터 
    - e.g. 일, 달, 분기(Quarterly), 년

## 시계열 데이터 예시 
강의 0:50 ~ 7:25

## 시계열 데이터 구성요소  
> **"영어로 알자"**
* Trend(추세변동)
    - e.g. 올라가거나, 내려가는 모양
* Cycle(순환변동)
    - e.g. 올라갔다 내려온 한 주기 
* Seasonal variations(계절변동): Cycle의 일부분, 계절에 따라 Cycle이 형성된 것 
* Random fluctuation(우연변동)

## 시계열 데이터 구성요소
* Trends: 시간이 경과함에 따라 관측값이 지속적으로 증가(upward) 혹은 감소(downward)하는 Trend(추세)를 갖는 경우의 변동을 의미한다. 주로 경제 관련 데이터에서 발생한다. 
* Cycle: 주기적인 변화를 가지나 계절에 의한 것이 아니고 주기가 긴 경우의 변동을 의미한다. 
* Seasonal variations: 주별, 월별, 계절별과 같이 주기적인 요인에 의한 변동 
* Random fluctuation: 시간에 따른 규칙적인 움직임과는 무관하게 램덤한 원인에 의해 나타나는 변동
    - e.g. White Noise(백색 잡음): 평균이 0이고, 분산이 일정한 시계열 데이터 

#### Quiz
* Q. Seanal variations와 Cycle 차이점? 
* Q. 데이터에서 Trend와 Seasonal variations 요소를 제거하면 어떤 성분이 남을까?     
    - A: Random fluctuation 

## Prediction Error(예측오차) 
* t에서의 실제값 = t에서의 예측값 (t: 특정시점) 
* 오차가 양수와 음수 모두 될 수  있으므로 단순히 차이를 더한 값은 0에 가까운 수가 된다.
* 오차의 부호 보다 amount of difference(정도)가 중요하다. 

### MAD(평균절대편차)
* 일반적으로 많이 쓰이는 지표 

### MSE(평균제곱편차) 
* MAD 수식에서 절대값 대신 제곱 취해줌

#### MAD  vs MSE
* 아래 표에서 위 모델과, 아래 모델간의 MAD와 MSE의 평가가 다르다. 
* MSE는 특별하게 잘못된 예측치에 대해 예민하다. 두 모델 케이스를 보더라도, 아래 모델 같은 경우 Squarred Error가 36이기 때문에 1, 2 케이스에서 Squared Error가 적게 나왔어도 MSE로 Error를 평가하면, 아래 모델이 더 큰 Error를 가진다. 

### MAPE(Mean Absolute Percentage Error)
* 분수식 형태이기 때문에 실제값이 0일때 계산할 수 없다. 
* 실제값이 매우 작으면 예측값과 실제값의 차이와 상관없이 Error 계산 결과가 매우 크기 나온다. 
* 예측값보다 실제값보다 작은 경우에 대해 Biased하다. 아래 그림처럼 차이값이 같은 케이스임에도 불구하고 더 작은 MAPE가 나온다. 

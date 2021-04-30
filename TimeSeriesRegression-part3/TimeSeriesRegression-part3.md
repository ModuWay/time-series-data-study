# 성은([vg-rlo](https://github.com/vg-rlo))

## Growth Curve Models 수식에서 log 변환을 취해줌으로서 모델링할 수 있어진다는 점이 식의 구성?에서의 선형조건이 성립된 것인지 궁금합니다. 

![image](https://user-images.githubusercontent.com/69677950/116641272-596ed380-a9a7-11eb-9163-d23cc18912df.png)



# 이삭([IsaacTips](https://github.com/IsaacTips))
# 인유([willowlkim8](https://github.com/willowkim8))

전처리가 끝나면 시범적인 모델을 찾아봐야한다.

**graphical method** : 주관적이지만 [왜 주관적이지??-> cut off, dying out 를 판단하는게 주관적일 수 있다!]

MA or AR or ARMA 중에 고르기

그에 맞는 파라미터도 정해야한다.  



1에서 cut off → MA(1) 적합

근방 모델 찍어보기 → 수동으로 찾기

AIC 젤 작은거 → 최종은 아님   



**Diagnosis**

최종으로 확인하는 단계

Residual을 가지고 ACF(autocorrelation)하는거

40개 중에서 2-3개 나가는 것까지는 OK (육안으로 확인했을 때)

→최종 모델로 선정   



**Seasonal ARIMA Model(SARIMA)**

월별 계절성 s=12, 분기별 계절성 s=4

# 민정([miinkang](https://github.com/miinkang))
## 삼각함수를 이용한 시계열 데이터 예측 
*강의 중 해당 내용에 대해 더 찾아본 후 정리하였습니다.*    
![image](https://user-images.githubusercontent.com/68461606/116641026-d8afd780-a9a6-11eb-9af2-7d7c67f1f8b4.png)
- 데이터가 갖고 있는 반복적인 패턴을 모델링하기 위해 사용되는 기법. 
- 데이터의 계절성을 민감하게 반영할 경우 overfitting문제가 발생할 수 있다. 
- 이를 해결하기 위해 sin, cos을 이용해 smoothing시킨다.    
- sin, cos 두 패턴 중 어떤 패턴이 해당 데이터에 적합한 지 눈으로 파악할 수 없기 때문에, 모두 공식에 넣어 **통계적으로 유의미한 것**을 사용한다.    
ref. [삼각함수를 이용한 시계열 예측](https://blog.naver.com/PostView.nhn?blogId=ibuyworld&logNo=222021695385&parentCategoryNo=&categoryNo=&viewDate=&isShowPopularPosts=false&from=postView)

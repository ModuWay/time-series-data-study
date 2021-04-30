# 성은([vg-rlo](https://github.com/vg-rlo))
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

# 성은([vg-rlo](https://github.com/vg-rlo))

## 알게된 점

* auto_arima 라이브러리가 실제 사용했을 때, AIC가 낮은 파라미터를 찾아내지 못해서 문제가 있는 라이브러리가 생각했으나, 함수의 argument를 graphical한 방법으로 초기값을 잘 줘야한다는 점을 알았다.
* 실습과정에서 itertools로 전체 케이스를 적용하는 방법으로 검증할 수 있다.  auto_arima로 최적 파라미터 구하는 과정을 시간 효율성을 확보할 수 있다.

# 이삭([IsaacTips](https://github.com/IsaacTips))

## 알게된 점

* SARIMA에서 seasonal parameter도 탐색의 대상이 된다.

# 인유([willowlkim8](https://github.com/willowkim8))

(배운 내용의 흐름을 정리할 수 있는 강의)

## 알게된 점

+ 그래프 판단할 때, 주관적인 판단이 많이 들어가서 모델 선정하는 데 있어 많은 경험이 있으면 좋을 것 같다.

# 민정([miinkang](https://github.com/miinkang))
## 알게된 점 
- 차분 후 결측치를 제거해야한다. 
- 파라미터 p, q를 정하는 기준(노하우)이 필요한 것 같다. → 실습에서는 경우의 수를 모두 살펴봄 
- 그리드 서치 시간이 많이 소요되어서 autoarima를 사용하지만 일반적으로 성능이 좋지 않다고 했는데 실습에서는 잘 되었다.. 확인 필요! 

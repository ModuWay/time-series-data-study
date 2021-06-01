# 성은([vg-rlo](https://github.com/vg-rlo))
# 이삭([IsaacTips](https://github.com/IsaacTips))

## 대체로 많이 사용하는 모수들이 있던데, 그 값들은 어떻게 나오게 된걸까?(노드에서 언급)

p 와 q 에 대해서는 통상적으로 p + q < 2, p * q = 0 인 값들을 사용하는데, 이는 p 나 q 중 하나의 값이 0이라는 뜻이다. 이렇게 하는 이유는 실제로 대부분의 시계열 데이터는 자기회귀 모형(AR)이나 이동평균 모형(MA) 중 하나의 경향만을 강하게 띠기 때문이다. 

d는 차분이기 때문에, 1이나 2를 해서 직접 찍어보고 안정되었는지 확인하여 결정한다.

강의에서는 for문으로 모든 경우의 수를 해보는 것이 좋다고 말했다.


# 인유([willowlkim8](https://github.com/willowkim8))
# 민정([miinkang](https://github.com/miinkang))
## 알게된 점 - 파라미터 설정방법
- d(차분)의 경우, 데이터의 특성에 따라 1 or 2로 결정한다.   
- 차분후 ACF를 이용해 stationary하게 변함을 확인해야한다.    
- p, q : 1~20으로 그리드 서치를 진행한 후 AIC가 낮은 모수를 선택한다. 

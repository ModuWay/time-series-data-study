# 성은([vg-rlo](https://github.com/vg-rlo))

## Growth Curve Models 수식에서 log 변환을 취해줌으로써 모델링할 수 있어진다는 점이 식의 구성?에서의 선형조건이 성립된 것인지 궁금합니다. 

![image](https://user-images.githubusercontent.com/69677950/116641272-596ed380-a9a7-11eb-9163-d23cc18912df.png)



# 이삭([IsaacTips](https://github.com/IsaacTips))
## Seasonal Factor를 Binary 변수로 바꿔주는 이유?

Binary 변수로 바꿔주는 것을 하나의 표현 방식이라고 생각하자.

<img src="./image/binary.png" />

t시점에서 season이 일치하다면 1이고 아니면 0으로 표현. 

<img src="./image/binary.jpg" />

예시를 보면 169는 8년째의 1월이기 때문에 $x_{1}$에 169, $x_{2}$에 1을 넣고 나머지는 전부 0이 된다. 

__결론__
* Binary 변수로 바꿔주는 것은 하나의 표현 방식인데, t 시점이 그 season이라면 1을 아니면 0으로 표현하여, 예측모델 수식에 넣는다.

# 인유([willowlkim8](https://github.com/willowkim8))

## 성장커브에서 비선형은 모델링이 어려워서 Linear 파라미터로 바꿔준다고 했는데 그 이유는?


# 민정([miinkang](https://github.com/miinkang))
## 삼각함수를 이용한 시계열 데이터 예측 
*강의 중 해당 내용에 대해 더 찾아본 후 정리하였습니다.*    
![image](https://user-images.githubusercontent.com/68461606/116641026-d8afd780-a9a6-11eb-9af2-7d7c67f1f8b4.png)
- 데이터가 갖고 있는 반복적인 패턴을 모델링하기 위해 사용되는 기법. 
- 데이터의 계절성을 민감하게 반영할 경우 overfitting문제가 발생할 수 있다. 
- 이를 해결하기 위해 sin, cos을 이용해 smoothing시킨다.    
- sin, cos 두 패턴 중 어떤 패턴이 해당 데이터에 적합한 지 눈으로 파악할 수 없기 때문에, 모두 공식에 넣어 **통계적으로 유의미한 것**을 사용한다.    
ref. [삼각함수를 이용한 시계열 예측](https://blog.naver.com/PostView.nhn?blogId=ibuyworld&logNo=222021695385&parentCategoryNo=&categoryNo=&viewDate=&isShowPopularPosts=false&from=postView)
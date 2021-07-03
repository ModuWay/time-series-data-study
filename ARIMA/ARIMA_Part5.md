# 성은([vg-rlo](https://github.com/vg-rlo))

## x_t의 조건식을 정리해나갈 때 왜 다 무한등비급수 꼴이 되는가?
AR, ARMA, ARIMA 모델 등에서 Stationary한 시계열의 경우에서도 lag가 커져도 천천히 ACF가 급감할 뿐, 수렴하지 않고 무한대로 발산한다.     
따라서 x_t의 조건식도 유리수의 거듭제곱으로 인해 무한등비급수의 형태로 표현 가능하다.    
[참고자료](https://m.blog.naver.com/estpublic/221766903723)

# 이삭([IsaacTips](https://github.com/IsaacTips))

## Q. 강의에서 Forward shift operator는 많이 사용하지 않는다라고 언급했다. 어느때 사용하는 것일까?

* 모르겠음. 그냥 안쓸 것 같다.... 이전 데이터(backward)를 활용해서 예측하는데, 현재의 forward는 미래여서 사용 못하는 것 같다는 생각....

[참고자료](https://blog.naver.com/estpublic/221766516237)

# 인유([willowlkim8](https://github.com/willowkim8))

### h값에 따른 ARIMA 모델의 분산을 구하는 

# 민정([miinkang](https://github.com/miinkang))

![image](https://user-images.githubusercontent.com/68461606/124343164-73759e00-dc04-11eb-9b56-3fd527fc50b2.png)   
AR모델에서의 white noise를 수식 내에 있는 **함수**에 통과시키면 어떤 특정한 패턴을 갖고 있는 ar p process가 된다. 

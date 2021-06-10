# 성은([vg-rlo](https://github.com/vg-rlo))

## 구간 평균법이 적절한 case에 대해 설명할때, "일정 패턴없이 변하는 level"이 시계열 요소 중 어떤 요소만 있는 경우를 말하는 것인지 궁금하다 . cycle인지 아니면 random한건지?

## 이중지수 평활법 설명하는 부분에서 예시에서 Y절편을 유도하는 식이 아래와 같은 등비급수를 통해 유도되는데, 관련 블로그 설명에서 확인했을 때 시정수(타우)를 의미하는 것인가?
![image](https://user-images.githubusercontent.com/69677950/117383106-f0dda480-af1a-11eb-9b98-262f79dd5a43.png)

* [참고링크1](https://support.minitab.com/ko-kr/minitab/18/help-and-how-to/modeling-statistics/time-series/how-to/double-exponential-smoothing/methods-and-formulas/methods-and-formulas/)    
* [참고링크2](https://datalabbit.tistory.com/76?category=1146956)    

# 이삭([IsaacTips](https://github.com/IsaacTips))

## Q. 주식시장에서는 왜 지수이동평균선(지수 평활법)을 많이 사용할까? (이동평균은 단순을 많이 보지만, 다른 지표들을 구할때 지수이동평균이 많이 사용된다.)

지수 이동평균이 가장 많이 쓰이는 이유는 주식의 관성을 볼 수 있기 때문이다. 주식은 큰 시세를 주기 전에 매집이 있고 매집이 끝났다는 신호가 있으며, 그 이후에 시세가 터지기 시작하면 올라가는 각도가 계속 높아지는 현상을 볼 수 있다. 이런 주식의 특성때문에 지수 이동평균이 가장 많이 쓰인다.

* 단순 이동평균
    - 단점: 추세의 반전을 빠르게 확인할 수 없다.
* 가중 이동평균
    - 단점: 힘이 강하지 않을 때 큰 이점이 없다.

[참고링크1](https://envestlife.tistory.com/37)

# 인유([willowlkim8](https://github.com/willowkim8))
- 구간 평균법

***

예측 값(forcast) = last level calculated(마지막 평균으로 쭉) → 이게 한계

유일한 하이퍼파라미터 = N

trend나 seasonal variation 이 없을 때 이용할 수 있다.

- 지수 평활법

------

y자체로 y를 예측한다

단순 평균이 아닌 가중 평균 이용

지수분포 모양에 근거한 가중치 결정

최근 데이터에 가중치를 더 두고 과거로 갈수록 가중치를 줄어들게

그 기준은 지수분포에 근거하겠다 → 지수 평활법

- 단순 지수 평활법 ( 알파 = 0.1 )

------

큰 알파 → 최근 데이터에 가중

작은 알파 → 과거 데이터에 가중

대부분 소프트웨어에서 최적의 알파값을 자동적으로 계산

한계 → 예측값이 모두 동일한 점

- 이주지수평활법

------

트렌드가 있을 때 적합

growth rate추가

- Holt-Winter 지수평활법 (삼중 지수 평활법)

------

Constant SV → additive

Increasing SV → multiplicative

# 민정([miinkang](https://github.com/miinkang))

## Q. 이중지수 평활법이 왜 단순지수 평활법을 2번 적용하는 기법인지?
## 단순지수 평활법, 이중지수 평활법 수식 비교
![image](https://user-images.githubusercontent.com/68461606/117387458-ea075f80-af23-11eb-85c7-b4f0e7512d21.png)
![image](https://user-images.githubusercontent.com/68461606/117387507-fbe90280-af23-11eb-94d2-226b16d45f27.png)   
이중지수 평활법은 단순지수 평활법에서 trend를 고려할 수 있는 가중치를 부가하면서 보다 현실 데이터에 가까운 예측이 가능하게 한다.      

- 풀어볼 수 있는 연습문제 : [링크](https://m.blog.naver.com/PostView.nhn?blogId=sigmagil&logNo=221502514892&proxyReferer=https:%2F%2Fwww.google.com%2F)
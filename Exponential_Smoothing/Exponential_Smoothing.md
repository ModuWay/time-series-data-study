# 성은([vg-rlo](https://github.com/vg-rlo))
# 이삭([IsaacTips](https://github.com/IsaacTips))
# 인유([willowlkim8](https://github.com/willowkim8))
- 구간 평균법

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

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2a9ebf40-fdaa-42db-86a2-63cd92df6bda/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2a9ebf40-fdaa-42db-86a2-63cd92df6bda/Untitled.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e1c52053-be24-4751-8bad-7d5e132df1a8/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e1c52053-be24-4751-8bad-7d5e132df1a8/Untitled.png)

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
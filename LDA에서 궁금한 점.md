## LDA에서 궁금한 점.

 

doc-topic distribution, word-topic distribution $\hat{\phi}, \hat{\theta}$  얘네들은 이터레이션을 돌리고 각 이터레이션별에서 추정한 애들의 평균일까? 아니면 final state에서 계산한 값들일까? CGS를 처음 제안했던 Griffiths and Steyvers의 논문인 finding scientific topic에서는 아래와 같이 나와있다.

<img width="545" alt="image" src="https://user-images.githubusercontent.com/36855000/83155057-cf394200-a13b-11ea-81f9-9bd42852eb81.png"> style="zoom:50%;" />

평균을 때린다는 얘기는 없으니까 final state에서 얘네들을 추정하는게 맞는 것 같다.



collapsed gibbs sampling은 이해하기가 쉽고 알고리즘이 나름 intuitive하여서 implement하기가 좋다. 그래서 얘로 입문을 했는데 얘는 시간이 많이 걸린다고 한다. (online variational inference 논문)

근데 또 LDA 논문을 읽다보면 VI를 이용한 것보다는 gibbs sampling을 이용한 것이 많긴 하다. 시간이 된다면 VI 쪽도 한번 구현을 해보는 것도 좋을 것 같다. 하지만 나의 우선적인 목표는 고성능 언어로 이터레이션을 빨리 돌리는 것으로 하자. (이번 방학 목표)
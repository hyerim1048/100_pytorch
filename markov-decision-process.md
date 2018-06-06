# markov decision process 

(S,A,P,r,R)  튜플  set 를 의미함.

## S Lstate

  set 를 의미하며 가능한 상태나 환경 등을 의미한다.

  * world-state : huge and not available to the agent
  * agent-state 
  
## A 

* action  들의  set 를 의미. 자동차를 어떻게 control 할 수 있는지

## P(s,a)

* state  의   transition probability,  특정  state 에서 action 을 취했을 때 다음  s 에 대한 확률

## R : S x A -> R( 실수 공간)

* 특정  state 에서 액션을 했을 떄 얻게 되는  rewward. function

## r

reward 의  discount factor.  시간이 지날수록  R 의 가치를 떨어뜨리고  처음받은 reward  가치를 더 키워줌
그럼 역할은 빠르게 통과할수록, 보상이 커지는 방향으로 움직이겠다!!

## http://sanghyukchun.github.io/76/
   
   


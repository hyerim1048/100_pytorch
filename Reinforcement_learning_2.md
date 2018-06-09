## Reinforcement Learning

## 1.  최적의  value function  찾기

### monte-carlo simulation 
각  state 에서  action  을 통해 얻은  reward 의 실제 평균값을  action value function 으로 사용함.
 이  value 가 가장 높은 액션을 선택.
 
 
 ###  TD Method
 
agent 가  return 값을 얻을때까지 기다리지 않고  time-step 마다 학습하는 방법
 Q(s,a) (현재  state 에서 얻어진 보상)과  Q(s',a')  다음 상태의 가치의 합으로 업데이트

 * Sarsa (state-action-reward-state-action) : agent 가 실제로 경험한  a' 를 사용함.  on-policy method
 * Q-learning(greedy trasition) : Q(s',a') 값은 최대가 되는  a' 만 사용, off-policy

### 강화학습
* 강화학습은 시간의 개념을 포함하는 학습방법이다.
* action value function 과  state value function 의 관계는  bellmann 으로 나타낼 수 있다.

### DQN?
* 강화학습에서  value function approximation 방법으로 뉴럴 네트워크를 사용하는 방법으로
* Q value 를 예측하기 때문에  deep Q network 라고 부른다.
* 참고로,  Q 는  action-value-function 식을 의미한다.
* deeplmind  의  Playing Atari with Deep Reinforcement Learning 에서 소개되었다.

### 어떻게 딥러닝과 강화학습은 서로 협력할까?

* deepmind paper 에서 4개의  screen shot 을  state 정보로 사용함
*  RGB 값은  Q value 계산에 도움이 되지 않아 흑백으로 전환
*  pixel 수의 경우의 수 중  neural network 를 통해서 이미지 정보에서  feature ㄷ르을 찾아낼 수 있음.
*  Q network -  이미지 정보를  state 로 받아  action 에 대한  Q-value 를 구하는 네트워크
* 이 논문에서는  3 cnn layers 와  2 fc layers 로 구성되어 있으며 기존의  CNN 과 달리 
*  정보의 손실이 있는  pooling layer 는 사용하지 않음.

 ### Q-network weight updates
 * Q value 를 구하기 위해서는  loss function 정의가 필요함
 * 모든  action a 에 대한  action-value 값을  Q network forward pass ㄹ를 수행해서 얻어낸다.
 *  
 

### 참고 자료

* https://legacy.gitbook.com/book/dnddnjs/rl/details
* https://jay.tech.blog/2017/01/10/deep-q-network-dqn/




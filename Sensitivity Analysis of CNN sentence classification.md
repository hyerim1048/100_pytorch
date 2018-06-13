이론보다는 시뮬레이션을 한 논문
https://arxiv.org/pdf/1510.03820.pdf

abstract

one-layer cnns 로 문장 분류하기
cnn one layer로 svm과 logistic을 이겨보겠다

introduction

CNN은 머신러닝 모델보다 느리지만 성능이 좋음
하지만, hyperparameter 와 architecture setting이 어려움

	* 
input word vector representa-tions; 
	* 
filter region size(s); 
	* 
the number of feature maps; 
	* 
the activation function(s); 
	* 
the pooling strat-egy; 
	* 
and regularization terms (dropout/l2).



경험적인 setting을 알려주려는 것이 목적

Conclusions


	* 
input vector는 중요하다. task마다 성능이 조금씩 다르긴 하지만 문장 분류에서는 w2v나 Glove가 one hot vector보다 성능이 좋았다.
	* 
filter region size도 중요하다
	* 
number of feature map 도 중요하다. 근데 수가 증가하면 training이 느려진다.
	* 
다른 pooling stretegies보다 1-max pooling이 제일 성능이 좋다
	* 
Regularization 이 크게 성능에 영향을 주지는 않았다.



Specific advice to practitioners


	* 
table 2에 있는 parameter로 맞춰서 학습을 하고, distributed vector모델로 pretraining을 하되 너무 데이터가 크면 one hot으로 explore 해라
	* 
filter region 은 1 ~ 10 이면 된다. 하지만 너무 긴 데이터 셋이면 더 큰 region이 필요할수도 있다. 가장 성능이 좋은 single region size를 고른 후에 다른 필터들과 조합해서 좋은 성능을 찾아보자
	* 
the number of feature maps for each fil-ter region size 를 100에서 600까지 바꿔보자. 그 이상으로 바꿔봤자 효용이 적다.
	* 
다양한 activation function을 이용해보지만 Relu와 tahn이 일반적으로 좋다.
	* 
그냥 1-max pooling을 쓰자 . 다른거 해봤자다
	* 
피처맵 수가 성능에 영향을 줄 때 regularization을 해보자
	* 
cross - fold validation



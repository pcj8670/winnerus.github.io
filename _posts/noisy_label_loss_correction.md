# Making Deep Neural Networks Robust to Label Noise: a Loss Correction Approach
## 개요
논문은 Noisy Label 환경에서 딥뉴럴넷을 잘 학습시키는 방법에 대한 논문입니다.
많은 Noisy Label을 다루는 논문이 있지만, 매우 쉬운 방법을 통해 괜찮은 성능을 내는 방법 같습니다.

논문은 데이터셋에 포함된 Noise 정보 Label Transition Matrix를 안다는 가정하에 이를 이용해서 Cross Entropy loss의 최적화 방향을 True label방향으로 살짝 바꾸어줍니다.
논문은 총 3가지 내용을 얘기하는데, 
1. Backward Correction
2. Forward Correction
3. Transition Matrix Estimation 방법

Backward Correction은 loss를 먼저 계산한 후, Transition Matrix의 inverse를 곱해줍니다.
논문에서는 

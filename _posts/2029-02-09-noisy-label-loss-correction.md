


# Making Deep Neural Networks Robust to Label Noise: a Loss Correction Approach
## 개요
논문은 Noisy Label 환경에서 딥뉴럴넷을 잘 학습시키는 방법에 대한 논문입니다.
많은 Noisy Label을 다루는 논문이 있지만, 매우 쉬운 방법을 통해 괜찮은 성능을 내는 방법 같습니다.

논문은 데이터셋에 포함된 Noise 정보 Label Transition Matrix를 안다는 가정하에 이를 이용해서 Cross Entropy loss의 최적화 방향을 True label방향으로 살짝 바꾸어줍니다.
여기서 Label Transition Matrix란 클래스 개수가 C 일때, C x C 크기의 Matrix이며, C_12는 라벨1이 라벨2로 바뀌어있을 확률을 나타내는 행렬입니다.
논문은 이 Transition Matrix를 중점적으로 활용하여 loss를 교정합니다.

논문은 총 3가지 내용을 얘기합니다.
1. Backward Correction
2. Forward Correction
3. Transition Matrix Estimation 방법


1. Backward Correction은 loss를 먼저 계산한 후, Transition Matrix의 inverse를 곱해줍니다.
논문에서는 Theorem 1을 통해 이것이 $x$


$$
y
$$


(현재가진 노이즈라벨)이 아닌 True Label에 대한 loss값과 같음을 증명해줍니다.


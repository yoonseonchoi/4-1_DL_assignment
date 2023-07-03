# DL_Assignment
4학년 1학기 <딥러닝및응용> 과목에서 진행한 Assignment

## Data
Flower102

## Model
CNN architecture만을 사용하여 End-to-end Autoencoder 모델을 구현하여 이미지를 예측하였다. 모델의 구조는 다음과 같다.
![image](https://github.com/yoonseonchoi/DL_Assignment/assets/102509278/29d7bb19-5927-4800-afe6-c6277b14f30e)
pytorch의 convtranspose2d를 사용하지 않고 decoder를 구현해야 했기에, pooling을 두껍게 주어 이미지 크기를 복원하였다.

encoder를 통해 학습된 feature map을 classifier에 통과시켜 이미지를 최종 예측하도록 하였다.
![image](https://github.com/yoonseonchoi/DL_Assignment/assets/102509278/d312611a-42fa-4c1c-93be-d4ffa0823d1a)
### Hyperparameter Tuning
padding을 두껍게 설정하였기 때문에 정확도가 매우 낮았다. 따라서 정확도를 조금이나마 높이기 위해 epoch size, learning rate, optimizer를 바꾸어 가며 실험을 진행하였다.

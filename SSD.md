# 1. Single Shot Multibox Detector (SSD)
```
tensorflow==1.0.0, keras==1.2.2, opencv-python==3.1.0.4
```
Input shape: (300 ,300)

Output: 8732x(21+4) = priors x (channels x offsets)

## 특징
![SSD_architecture](https://user-images.githubusercontent.com/67774946/152835312-e696b723-d2cd-44ce-bfc1-0a4ece6360aa.png)

1. Time과 Accuracy의 trade-off 문제를 해결함.

2. 다양한 scale의 feature map을 예측에 사용하고 다양한 scale의 default box를 사용한다.

3. VGG-16의 input size를 (300, 300)으로 바꾸고, FC layers를 CNN layers로 바꾸고 feature map을 추가했다.

4. Auxiliary Convoultions(점점 작아지는 feature map) 사용
5. Priors 좌표와 실제 Box의 offsets의 차이로 loss를 구해 regression한다.

## 개념

1. MultiBox: Box가 Object를 포함하고 있는가? Box안 scores for various object types?
2. Prior: Box가 존재 할 수 있는 모든 위치를 미리 계산해 구한 고정된 box. Feature map마다 측면 비율, 스케일 등이 다르다. 구하면 8732개의 boxes가 구해진다.
3. Non-Maximum Suppression(NMS): 겹치는 Box를 IOU 계산을 통해 제거해주는 알고리즘.
## Reference

SSD for Vehicle Detection and Tracking: https://github.com/mohammedamarnah/vehicle-detection

Pre-trained model: https://github.com/rykov8/ssd_keras

Research paper: https://arxiv.org/abs/1512.02325

참고: https://herbwood.tistory.com/15

https://github.com/sgrvinod/a-PyTorch-Tutorial-to-Object-Detection

*moviepy오류 - brew reinstall ffmpeg


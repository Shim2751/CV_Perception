# CV_Perception
## 1. Single Shot Multibox Detector (SSD)
```
tensorflow==1.0.0, keras==1.2.2, opencv-python==3.1.0.4
```
Input shape: (300 ,300)

Pipeline: Process_frame(img), Decode_output(out_put, threshold)

Output: 

### 특징
![SSD_architecture](https://user-images.githubusercontent.com/67774946/152835312-e696b723-d2cd-44ce-bfc1-0a4ece6360aa.png)

1. Time과 Accuracy의 trade-off 문제를 해결함.

2. 다양한 scale의 feature map을 예측에 사용하고 다양한 scale의 default box를 사용한다.

### Reference

SSD for Vehicle Detection and Tracking: https://github.com/mohammedamarnah/vehicle-detection

Pre-trained model: https://github.com/rykov8/ssd_keras

Research paper: https://arxiv.org/abs/1512.02325

참고: https://herbwood.tistory.com/15

*moviepy오류 - brew reinstall ffmpeg


## 2. Monodepth2
https://github.com/nianticlabs/monodepth2

## 3. 3D Bounding Box Estimation Using Deep Learning and Geometry
https://github.com/skhadem/3D-BoundingBox

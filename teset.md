KITTI(Karlsruhe Institute of Technology and Toyota Technology Institute)는 자동차의 주행에 대한 영상을 포함한 다양한 센서로 수집된 정보들을 수집 및 가공해서 제공한다. 상업적 용도로 사용하는 경우 별도의 라이센스를 획득해야 하지만 상업적 용도가 아니라면 회원가입을 통해 자유롭게 다운받고 사용할 수 있습니다.

이는 모바일 로봇 공학 및 자율 주행에서 사용하기에 가장 인기 있는 데이터 세트 중 하나로, 고해상도 RGB, 그레이스케일 스테레오 카메라 및 3D 레이저 스캐너를 포함한 다양한 센서 양식으로 기록된 몇 시간의 주행 시나리오로 구성됩니다. 데이터 세트 자체에는 의미론적 분할을 위한 실측 자료가 포함되어 있지 않습니다. 그러나 다양한 연구자들이 데이터 세트의 일부에 필요에 맞게 수동으로 주석을 달았습니다.

알바레즈는 도로, 수직 및 하늘의 세 가지 클래스를 사용하여 도로 탐지 대회에서 323개 이미지에 대한 실측 자료를 생성했습니다.

Zhang 등은 건물, 하늘, 도로, 식물, 보도, 자동차, 보행자, 자전거, 표지판/폴 및 울타리의 10개 객체 범주에 대한 추적 챌린지에서 252개(훈련용 140개, 테스트용 112개) 획득 – RGB 및 벨로다인 스캔에 주석을 달았습니다. 

Ros 등은 건물, 나무, 하늘, 자동차, 표지판, 도로, 보행자, 울타리, 기둥, 보도 및 자전거의 11개 클래스로 170개의 훈련 이미지와 46개의 테스트 이미지를  레이블로 지정했습니다.

[※ Colab 활용 Yolo v8 예제 코드 링크(클릭)](https://velog.io/@jjanggu84/YOLOv8-Kitti-Dataset-Training)



**※  KITTI 데이터셋은 객체 탐지, 객체 추적, 의미론적 분할 ,뎁스 맵, 시각적 주행기록계 등에 사용되는 데이터셋을 모두 포함하고 있습니다.**



### 데이터 이미지 예시 

![이미지](https://www.cvlibs.net/datasets/kitti/images/header_depth.jpg)

![이미지](https://www.cvlibs.net/datasets/kitti/images/header_tracking.jpg)

![이미지](https://www.cvlibs.net/datasets/kitti/images/header_road.jpg)

![이미지](https://www.cvlibs.net/datasets/kitti/images/header_odometry.jpg)

### 이미지 카테고리
| 작업 |이름| 클래스 |개수|
|:---:|:---:|:---:|:---:|
| 도로/차선 검출 |Road/Lane Detection Evaluation 2013  | 3 Classes| train : 289 <br> test: 290|
| 객체 탐지    |Object Tracking Evaluation (2D bounding-boxes) | 8 Classes|  train: 21 sequences <br> test: 29 sequences|
| …       | …     |…|…



#### 데이터 사이즈

| 형식 | 내용 |
|:---:|:---:|
| 압축파일 | 수 MB 에서 수 GB까지 다양함  |


Caltech101 데이터 세트는 101개의 카테고리(헬리콥터", "코끼리", "의자" 등)의 이미지와 101개 카테고리가 아닌 이미지를 포함하는 배경 범주가 포함되어 있습니다. 각 객체 범주에 대해 약 40에서 800개의 이미지가 있는 반면 대부분의 클래스에는 약 50개의 이미지가 있습니다. 이미지의 해상도는 약 300x200 픽셀입니다. 

[※keras 예제 코드 링크](https://github.com/tilemmpon/Caltech_101_object_classification/blob/master/Caltech_101_split_dataset_and_first_NN.ipynb)

#### 데이터 이미지 예시 
![이미지](https://user-images.githubusercontent.com/26833433/239366386-44171121-b745-4206-9b59-a3be41e16089.png)

#### 이미지 카테고리
| 클래스        | 개수                                                                                                 |
|:--------------:|:-----------------------------------------------------------------------------------------------------------:|
| Faces         | 435 Samples                                    |
| Faces_easy        | 435 Samples                                                         |
| Leopards      | 200 Samples  |
| Motorbikes | 798 Samples |
| object       | pole · pole g                                                        
|    …   |…                                                                                                   |
| yin_yang         | 60 Samples                                             |




#### 데이터 구조 :
| 속성명 | 내용 |
| --- | --- |
| text |한국어 문장|
| pair |영어 문장|


#### 데이터 예시 :
| text | pair | 
| --- | --- | 
|  개인용 컴퓨터 사용의 상당 부분은 "이것보다 뛰어날 수 있느냐?" |Much of personal computing is about "can you top this?"
| 토론에 참여한 사람들은 법 집행과 국가 ... | Those involved in the discussions do take seriously ... | 
 |세계 에서 가장 강력한 수퍼컴퓨터를 1년... | After keeping the world's most powerful supercomputer ...|

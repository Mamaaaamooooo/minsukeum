KITTI(Karlsruhe Institute of Technology and Toyota Technology Institute)는 자동차의 주행에 대한 영상을 포함한 다양한 센서로 수집된 정보들을 수집 및 가공해서 제공한다. 상업적 용도로 사용하는 경우 별도의 라이센스를 획득해야 하지만 상업적 용도가 아니라면 회원가입을 통해 자유롭게 다운받고 사용할 수 있습니다.<br/><br/>
이는 모바일 로봇 공학 및 자율 주행에서 사용하기에 가장 인기 있는 데이터 세트 중 하나로, 고해상도 RGB, 그레이스케일 스테레오 카메라 및 3D 레이저 스캐너를 포함한 다양한 센서 양식으로 기록된 몇 시간의 주행 시나리오로 구성됩니다. 데이터 세트 자체에는 의미론적 분할을 위한 실측 자료가 포함되어 있지 않습니다. 그러나 다양한 연구자들이 데이터 세트의 일부에 필요에 맞게 수동으로 주석을 달았습니다.<br/><br/>
알바레즈는 도로, 수직 및 하늘의 세 가지 클래스를 사용하여 도로 탐지 대회에서 323개 이미지에 대한 실측 자료를 생성했습니다.<br/>
Zhang 등은 건물, 하늘, 도로, 식물, 보도, 자동차, 보행자, 자전거, 표지판/폴 및 울타리의 10개 객체 범주에 대한 추적 챌린지에서 252개(훈련용 140개, 테스트용 112개) 획득 – RGB 및 벨로다인 스캔에 주석을 달았습니다. <br/><br/>
Ros 등은 건물, 나무, 하늘, 자동차, 표지판, 도로, 보행자, 울타리, 기둥, 보도 및 자전거의 11개 클래스로 170개의 훈련 이미지와 46개의 테스트 이미지를  레이블로 지정했습니다.<br/><br/>
[※ Colab 활용 Yolo v8 예제 코드 링크(클릭)](https://velog.io/@jjanggu84/YOLOv8-Kitti-Dataset-Training)<br/><br/><br/>



__※  KITTI 데이터셋은 객체 탐지, 객체 추적, 의미론적 분할 ,뎁스 맵, 시각적 주행기록계 등에 사용되는 데이터셋을 모두 포함하고 있습니다.__



### 데이터 이미지 예시 

![이미지](https://www.cvlibs.net/datasets/kitti/images/header_depth.jpg)<br/>
![이미지](https://www.cvlibs.net/datasets/kitti/images/header_tracking.jpg)<br/>
![이미지](https://www.cvlibs.net/datasets/kitti/images/header_road.jpg)<br/>
![이미지](https://www.cvlibs.net/datasets/kitti/images/header_odometry.jpg)<br/>

### 이미지 카테고리
| 작업 |이름| 클래스 |개수|
|:---:|:---:|:---:|:---:|
| 도로/차선 검출 |Road/Lane Detection Evaluation 2013  | 3 Classes| train : 289 <br/> test: 290|
| 객체 탐지    |Object Tracking Evaluation (2D bounding-boxes) | 8 Classes|  train: 21 sequences <br/> test: 29 sequences|
| …       | …     |…|…



#### 데이터 사이즈

| 형식 | 내용 |
|:---:|:---:|
| 압축파일 | 수 MB 에서 수 GB까지 다양함  |


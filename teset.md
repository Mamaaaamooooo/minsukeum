# 데이터 <sup>설명<sup/>~ <sub>하하<sub/>

Cityscapes 시티스케이프는 도시 거리 이미지의 의미론적 이해에 초점을 맞춘 대규모 데이터베이스이다. 데이터는 8개 범주(평면, 인간, 차량, 구성, 객체, 자연, 하늘 및 공백)로 그룹화된 30개 클래스에 대한 의미론적, 객체별 주석을 제공한다. 데이터 세트는 약 5,000개의 상세 주석이 달린 이미지와 20,000개의 간략한 주석이 달린 이미지로 구성된다. 데이터는 50개 도시에서 주간의 좋은 기상 조건에서  촬영되었다. 



※현재  ttps://www.cityscapes-dataset.com/ 에서 데이터를 직접 다운로드 받으려면 회사 또는 학교 계정 인증이 필요합니다. kaggle, pytorch, tensorflow 등의 데이터셋 클래스에서 다운받는 것을 추천합니다.

### 데이터 이미지 예시 
![이미지](https://www.cityscapes-dataset.com/wordpress/wp-content/uploads/2015/07/zuerich00-1024x510.png)

### 데이터 라벨 예시 
| Group        | Classes                                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------------------|
| flat         | road · sidewalk · parking<sup>+</sup> · rail track<sup>+</sup>                                            |
| human        | person<sup>*</sup> · rider<sup>*</sup>                                                                    |
| vehicle      | car<sup>*</sup> · truck<sup>*</sup> · bus<sup>*</sup> · on rails<sup>*</sup> · motorcycle<sup>*</sup> · bicycle<sup>*</sup> · caravan<sup>*+</sup> · trailer<sup>*+</sup> |
| construction | building · wall · fence · guard rail<sup>+</sup> · bridge<sup>+</sup> · tunnel<sup>+</sup>                |
| object       | pole · pole group<sup>+</sup> · traffic sign · traffic light                                              |
| nature       | vegetation · terrain                                                                                      |
| sky          | sky                                                                                                       |
| void         | ground<sup>+</sup> · dynamic<sup>+</sup> · static<sup>+</sup>                                             |

#### 데이터 사이즈

| 종류 | 행렬 차원 |데이터 종류 |개수 |
| --- | --- |--- |--- |
| train |784(28*28 크기) | 학습용 이미지 데이터| 55,000 개|
| train_label |10(0~9 클래스)  | 학습용 라벨 데이터| 55,000 개|
| val |784(28*28 크기  |검증용 이미지 데이터| 5,000개|
| val_label |10(0~9 클래스)  | 검증용 라벨 데이터|5,000개|
| test | 784(28*28 크기  |테스트용 이미지 데이터| 10,000개|
| test_label | 10(0~9 클래스) | 테스트용 라벨 데이터| 10,000개|

# 데이터 설명

한영 병렬 말뭉치는 한국어 원문과 영어로 번역된 영문 텍스트의 한 쌍으로 이루어져 있습니다. 데이터 정보는 다음과 같습니다.


#### 데이터 사이즈 
 
| 종류 | 내용 |
| --- | --- |
| train | 94,123 pairs  |
| dev(val) |1,000 pairs  |
| test | 2,000 pairs  |



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

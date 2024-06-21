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

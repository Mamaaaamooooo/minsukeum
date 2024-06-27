MS COCO Captions 데이터셋의 영문 Caption 을 한국어 문장으로 번역. MS COCO 데이터셋 중 약 12만장에 해당하는 이미지의 설명문을 번역하였다. __※ [MS COCO 데이터셋 참고 (클릭)](https://cocodataset.org/#home)__

<br><br><br><br>
__※   [aihub 공식사이트(클릭)](https://dancetrack.github.io/) 에서 직접 다운로드 받을 수 있음.__



### 데이터 이미지 예시 

![이미지](https://private-user-images.githubusercontent.com/135937372/343135660-a5c1e18b-cab7-4772-92dc-80efa800a0c4.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk0MDEyMjUsIm5iZiI6MTcxOTQwMDkyNSwicGF0aCI6Ii8xMzU5MzczNzIvMzQzMTM1NjYwLWE1YzFlMThiLWNhYjctNDc3Mi05MmRjLTgwZWZhODAwYTBjNC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNjI2JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDYyNlQxMTIyMDVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT02Y2E3NDViMWE3N2Q5YmI0YTJmZGFkY2YxZmQzNTU2YWJkYTdmMjAxOTRjNjFlN2NhZDk1ZTNjMmE1NTIxYWQxJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.gSjs2vmI71d1Gx59sTdmzEhjwjRCUUiRwnhR6cegMuE)

### 이미지 카테고리
| 대분류 | 소분류 | 내용 |
|:---:|:---:|:---:|
| Person | person | 사람 |
| Animal | bird | 새|
|  | cat | 고양이|
| 3 | cow | 소|
| 4 | dog |개|
| … | … |…|
| Vehicle | aeroplane | 비행기 |
|  | bicycle | 자전거|
| … | … | … |
| Indoor | tv/monitor | TV/모니터 |

#### 데이터 구조 
| 내용 | 비고 |
| :---: | :---: |
| 주석형식 | XML 포맷|
| 어노테이션 | 바운딩박스(xmin-top left, ymin-top leff, xmax-bottom right, ymax-bottom right) |
| 평균 객체 수 | 2.4개 |
| 평균 클래스 수 | 1.4개 |



### 데이터 사이즈 
| 연도  | 클래스수 | 내용  | 개수 | 
|:---:|:---:|:---:|:---:|
| 2012  | 20  | train |5,717 Samples | 
| 2012  | 20 |test|5,823 Samples | 
| …  | …   | …  |…  | 
| 2007  | 22 |train|5,011 Samples | 
| …  | …   | …  |…  | 
| 2005  | 4 |train|1,578 Samples | 
| 2005  | 4 |test|654 Samples |

### 연도별 특징
| 연도 | 통계 | 달라진 점 | 비고 |
|------|-------------|-------------------|-------|
| [2005](http://host.robots.ox.ac.uk/pascal/VOC/voc2005/index.html) | 오직 4개의 클래스: 자전거, 자동차, 오토바이, 사람. 학습/검증/테스트: 1578개의 이미지에 2209개의 주석이 달린 객체가 포함됨. | 두 개의 대회: 분류 및 탐지 | 이미지는 주로 기존의 공개 데이터셋에서 가져왔으며, 이후 사용된 플리커 이미지만큼 도전적이지 않았습니다. 이 데이터셋은 더 이상 사용되지 않습니다. |
| [2006](http://host.robots.ox.ac.uk/pascal/VOC/voc2006/index.html) | 10개의 클래스: 자전거, 버스, 자동차, 고양이, 소, 개, 말, 오토바이, 사람, 양. 학습/검증/테스트: 2618개의 이미지에 4754개의 주석이 달린 객체가 포함됨. | 이미지 출처: 플리커와 Microsoft Research Cambridge (MSRC) 데이터셋 | MSRC 이미지가 플리커보다 쉬웠으며, 사진은 종종 관심 객체에 집중되었습니다. 이 데이터셋은 더 이상 사용되지 않습니다. |
| [2007](http://host.robots.ox.ac.uk/pascal/VOC/voc2007/index.html) | 20개의 클래스: <ul><li><i>사람:</i> 사람</li><li><i>동물:</i> 새, 고양이, 소, 개, 말, 양</li><li><i>차량:</i> 비행기, 자전거, 보트, 버스, 자동차, 오토바이, 기차</li><li><i>실내:</i> 병, 의자, 식탁, 화분, 소파, TV/모니터</li></ul> 학습/검증/테스트: 9963개의 이미지에 24640개의 주석이 달린 객체가 포함됨. | <ul><li>클래스 수가 10개에서 20개로 증가</li><li>세분화 테스트 추가</li><li>사람 레이아웃 테스트 추가</li><li>주석에 절단 플래그 추가</li><li>분류 대회의 평가 척도가 ROC-AUC에서 평균 정밀도로 변경됨</li></ul> | 이 해에 20개의 클래스가 설정되었으며, 이후 고정되었습니다. 이 해가 테스트 데이터의 주석이 공개된 마지막 해입니다. |
| [2008](http://host.robots.ox.ac.uk/pascal/VOC/voc2008/index.html) | 20개의 클래스. 데이터는 (평소와 같이) 약 50% 학습/검증과 50% 테스트로 나뉩니다. 학습/검증 데이터는 4340개의 이미지에 10363개의 주석이 달린 객체가 포함됨. | <ul><li>주석에 가림 플래그 추가</li><li>테스트 데이터 주석이 더 이상 공개되지 않음</li><li>세분화 및 사람 레이아웃 데이터셋에 VOC2007 세트의 이미지 포함</li></ul> |  |
| [2009](http://host.robots.ox.ac.uk/pascal/VOC/voc2009/index.html) | 20개의 클래스. 학습/검증 데이터는 7054개의 이미지에 17218개의 ROI 주석이 달린 객체와 3211개의 세분화가 포함됨. | <ul><li>이제부터 모든 작업의 데이터는 이전 해의 이미지에 새로운 이미지를 추가하여 구성됩니다. 이전에는 매년 분류/탐지 작업을 위한 완전히 새로운 데이터셋이 공개되었습니다.</li><li>추가함으로써 매년 이미지 수가 증가하고, 테스트 결과를 이전 해의 이미지와 비교할 수 있게 됩니다.</li><li>세분화가 표준 대회로 승격됨 (테스터에서 승격)</li></ul> | <ul><li>추가된 이미지에 대해 어려운 플래그가 제공되지 않았음 (누락).</li><li>테스트 데이터 주석이 공개되지 않음.</li></ul> |
| [2010](http://host.robots.ox.ac.uk/pascal/VOC/voc2010/index.html) | 20개의 클래스. 학습/검증 데이터는 10103개의 이미지에 23374개의 ROI 주석이 달린 객체와 4203개의 세분화가 포함됨. | <ul><li>액션 분류 테스터 추가</li><li>ImageNet을 기반으로 한 대규모 분류에 대한 관련 대회 추가</li><li>아마존 메커니컬 터크를 초기 주석 단계에 사용</li></ul> | <ul><li>AP 계산 방법이 변경됨. 이제는 모든 데이터 포인트를 사용하여 계산됨 (TREC 스타일 샘플링 대신)</li><li>테스트 데이터 주석이 공개되지 않음.</li></ul> |
| [2011](http://host.robots.ox.ac.uk/pascal/VOC/voc2011/index.html) | 20개의 클래스. 학습/검증 데이터는 11530개의 이미지에 27450개의 ROI 주석이 달린 객체와 5034개의 세분화가 포함됨. | <ul><li>액션 분류 테스터가 10개의 클래스 + "기타"로 확장됨</li></ul> | <ul><li>레이아웃 주석이 이제 완전하지 않음: 사람만 주석이 달렸으며 일부 사람은 주석이 달리지 않을 수 있음.</li></ul> |
| [2012](http://host.robots.ox.ac.uk/pascal/VOC/voc2012/index.html) | 20개의 클래스. 학습/검증 데이터는 11530개의 이미지에 27450개의 ROI 주석이 달린 객체와 6929개의 세분화가 포함됨. | <ul><li>세분화 데이터셋의 크기가 상당히 증가함.</li><li>액션 분류 데이터셋의 사람은 신체의 참조 포인트로 추가 주석이 달림.</li></ul> | <ul><li>분류, 탐지 및 사람 레이아웃에 대한 데이터셋은 VOC2011과 동일함.</li></ul> |



### 이미지 카테고리
| 작업 |이름| 클래스 |개수|
|:---:|:---:|:---:|:---:|
| 도로/차선 검출 |Road/Lane Detection Evaluation 2013  | 3 Classes| train : 289 <br> test: 290|
| 객체 탐지    |Object Tracking Evaluation (2D bounding-boxes) | 8 Classes|  train: 21 sequences <br> test: 29 sequences|
| …       | …     |…|…

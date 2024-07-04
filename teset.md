AI HUB '상담음성' 데이터셋은 웹 기반 등 다양한 방식으로 상담센터에 연락하여 상담하는 내용을 녹음한 음성 데이터입니다.

한국인의 음성을 문자로 바꾸어 주고, 문맥을 이해하는 한국어 음성 언어처리 기술 개발을 위하여 AI 학습용 한국어 음성 DB를 구축하였습니다. 

교육, 금융, 통신판매 등 다양한 도메인에서 AI 상담센터용 음성인식 학습데이터로 활용 가능한 3,000시간의 가상 시나리오 기반한 크라우드 소싱 녹취 데이터를 수집하였으며, wav 음원파일, txt 전사 텍스트 파일, json 형식의 메타데이터 파일이 제공됩니다.

본 데이터셋은 AI상담센터를 위한 음성상담, 음성인식기술 및 언어이해, 언어생성연구 및 서비스 개발에 활용될 수 있습니다.

__※ [AIHUB 음성, 텍스트 데이터 전처리 참고 자료(클릭)](https://blog.naver.com/sooftware/221821797852)__

__※  AIHUB의 전사 규칙을 참고하여, 상기 사이트의 데이터 전처리과정을 정독하는 것을 추천합니다.__

### 데이터 사이즈
|  데이터 종류| 수집시간   | 제공방식  |
|:---:|:---:|:---:|
| 교육 | 1000시간   | wav 음원파일<br>txt 전사파일<br>json 메타파일    |
| 금융   | 1000시간  |  wav 음원파일<br>txt 전사파일<br>json 메타파일   |
| 통신판매 | 1000시간 |  wav 음원파일<br>txt 전사파일<br>json 메타파일 |


### 데이터 요약 이미지 
  ![이미지](https://github.com/Mamaaaamooooo/minsukeum/blob/main/%EC%83%81%EB%8B%B4%EC%9D%8C%EC%84%B1_data.png?raw=true)

__또는 [Kaggle(링크)](https://www.kaggle.com/datasets/namhocayai/voxceleb1)에서 .wav 파일과 .txt 파일을 다운 받을 수 있음__

### 음성파일 디렉토리 구조
-------------------------------------------------
```
<원천 데이터>
    |
    .- KtelSpeech.../
    |           |
                .- J91/
                |
                    .- S00007727/
                            |    |
                            .- 0001.wav
                            |    |
                            .- 0002.wav
                            |    |
                            .- 0003.wav 
                            |    |
                            |    ...
                    .- S00007728/
                            |    |
                            .- 00001.wav
                            |    ...
                .- J92/
                |
                ...
```
__※여기서 폴더명은 각 대화 . 가령, 1zcIwhmdeo4 폴더의 경우 원본 동영상의 링크는 https://www.youtube.com/watch?v=1zcIwhmdeo4가 됩니다.__


### 전사텍스트 파일 디렉토리 구조
-------------------------------------------------
```
<라벨링 데이터>
    |
    .- KtelSpeech.../
    |           |
                .- J91/
                |
                    .- S00007727/
                            |    |
                            .- 0001.txt
                            |    |
                            .- 0002.txt
                            |    |
                            .- 0003.txt 
                            |    |
                            |    ...
                    .- S00007728/
                            |    |
                            .- 00001.txt
                            |    ...
                .- J92/
                |
                ...
```
### 메타데이터 JSON 파일 예시
```JSON
{
	"dataSet": {
		"version": "1.0",
		"date": "20210110",
		"typeInfo": {
			"category": "교육",
			"subcategory": "교육",
			"place": null,
			"speakers": [
				{
					"id": "10614",
					"gender": "여",
					"type": "상담원",
					"age": "30대",
					"residence": "서울"
				},
				{
					"id": "qpccbzaz",
					"gender": "여",
					"type": "고객",
					"age": "30대",
					"residence": "경기"
				}
			],
			"inputType": "모바일"
		},
		"dialogs": [
			{
				"speaker": "10614",
				"audioPath": "KtelSpeech/D60/J91/S00007727/0001.wav",
				"textPath": "KtelSpeech/D60/J91/S00007727/0001.txt"
			}
			...
}
```
### 각 카테고리 설명

| ID  | 키 명 | 타입  |  키 설명 |
|---|---|---|---|
|  | dataSet        | Dict  |  데이터셋               |                                           |
| 1   | version         | String | 데이터셋 버전       |                                           |
| 2   | date            | String | 녹취된 날짜         |                                           |
| 3   | typeInfo        | Dict   | 음원 데이터 상세 정보 |                                           |
| 3-1 | category        | String | 음원 카테고리 정보  |                                           |
| 3-2 | subcategory     | String | 음원 서브 카테고리  |                                           |
| 3-3 | place           | String | 음원 녹취 장소      |                                           |
| 3-4 | speakers        | List   | 화자 목록           |                                           |
| 3-4-1 | id            | String | 화자 아이디         |                                           |
| 3-4-2 | type          | String | 화자 유형: 고객, 상담원 |                                           |
| 3-4-3 | age           | String | 나이대: 20대, 30대, 50(추정), null(알수없음) 등 | |
| 3-4-4 | gender        | String | 화자 성별: 남, 여   |                                           |
| 3-4-5 | residence     | String | 거주지역: 서울, 대전, 부산, 광주, null(알수없음) 등 | |
| 3-5 | inputType       | String | 입력형식: 방송, 유선, 모바일, 인터넷 등 |  |
| 4   | dialogs         | List   | 전사 데이터 목록: 묵음 기준으로 나누어진 발화 단위로 생성 | |
| 4-1 | speaker         | String | 화자 아이디: speakers에 등록된 id |            |
| 4-2 | audioPath       | String | 발화 단위 RAW 데이터 경로 |                                    |
| 4-3 | textPath        | String | 발화 단위 TEXT 데이터 경로 |                                    |


### 데이터 사이즈 
 
| 종류 | 내용 |
|:---:|:---:|
| train | 약 99 GB  |
| dev(val) | 약 1.2GB  |
| 총 용량 | 약 100 GB |

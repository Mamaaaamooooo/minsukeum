AI HUB '구음장애 음성인식' 데이터셋은 병원(한림대 강남성심병원, 동탄성심병원 등), 청각 센터(한림대 청각학과 졸업생 네트워크 활용)에서 최소 1,200명(총 5,000 시간 이상 5,250시간 이하)의 원시데이터를 확보하여 다양한 나이, 지역, 성별, 질환으로부터 정제된 발화 데이터 추출 및 질환 분류 인공지능 데이터셋 구축하였습니다.

학습 데이터 셋은 녹음한 음성 파일이며, 전사데이터는 txt 기반의 데이터 셋 목록 및 메타정보로 구성되어 있습니다. 

메타정보를 담고 있는 JSON 파일은 환자관리번호, 질병, 나이, 성별, 거주지, 녹음장소, 음원파일이름, 음원의 Sampling Rate, 말소리 시작지점, 말소리 종료지점, 총 재생 시간, 음원 데이터 크기, 말소리, 환자관리번호, 질병, 나이, 성별, 거주지, 녹음장소, 녹음파일이름 등의 카테고리로 어노테이션 되어 있습니다.


__※ [해당 데이터 전처리 참고 자료(클릭)](https://ysg2997.tistory.com/52)__

__※ [해당 데이터 시각화 및 특성 추출 참고 자료(클릭)](https://ysg2997.tistory.com/51)__


__※  추가적으로 AIHUB의 데이터 설명서 및 활용가이드를 읽어 보는 것을 추천합니다.__



### 데이터 카테고리
--------
| 항목 | 인원 | 녹음 시간|
|:---:|:---:|:---:|
| 뇌신경장애 | 1,200명 | 1,750 시간 이하|
| 언어 및 청각장애 | 1,200명 | 1,750 시간 이하|
| 후두장애 | 1,200명 | 1,750 시간 이하|
| 소계 | 1,200명 |5,000시간 ~ 5,250 시간|

### 데이터 사이즈
--------
| 종류 | 용량량 |
|:---:|:---:|
| Train | 약 381 GB  |
| Val | 약 75 GB  |

### 데이터 포맷 
--------
| 데이터 종류 | 형식 |
|:---:|:---:|
| 오디오 | .wav  |
| 라벨링(음성 전사) | .json  |

### JSON 데이터 예시 
------
```JSON
{
	"playTime": 744.3171201814059,
	"Transcript": "문 열어. 문 열어? 나무가 많아. 나무가 많아? 내일 만나. 내일 만나? 이제 내려. 이제 내려? 머리 말려. 머리 말려? 여기 놔요. 여기 놔요? 나비가 날아요. 나비가 날아요? 엄마가 노래해. 엄마가 노래해? 머리 말려요. 머리 말려요? 여기 놨어요. 여기 놨어요? 여기 놔. 여기 놔? 여기 놔요. 여기 놔요? 머리 말려. 머리 말려? 머리 말려요. 머리 말려요? 여기 놨어요. 여기 놨어요? 머리 말렸어요. 머리 말렸어요? 여기 놓을 거예요. 여기 놓을 거예요? 밥 먹었죠. 밥 먹었죠? 집에 아무도 없겠지. 집에 아무도 없겠지? 발이 얼었어요. 발이 얼었어요? 길이 많이 막혀요. 길이 많이 막혀요? 선생님이 하셨어요. 선생님이 하셨어요? 거기 갈래. 거기 갈래? 그렇게 될 리가 없지. 그렇게 될 리가 없지? 전화 왔어요. 전화 왔어요? 여기까지 걸어 왔어요. 여기까지 걸어 왔어요? 방이 추운 거 같애. 방이 추운 거 같애? 날씨가 추워요. 날씨가 추워요? 음악 켜. 음악 켜? 날씨가 더워요. 날씨가 더워요?",
	"File_id": "ID-02-25-N-KSM-02-02-M-45-JL.wav",
	"FileSize": 1561,
	"Disease_info": {
		"Type": "02",
		"Subcategory1": "",
		"Subcategory2": "25",
		"Subcategory3": "",
		"Subcategory6": ""
	},
	"Meta_info": {
		"Language": "Korean",
		"Version": "v.0.1",
		"RecordingDate": "",
		"FilingDate": "",
		"RevisionHistory": "",
		"SamplingRate": 48000,
		"Frequency": "",
		"StartPos": 0,
		"EndPos": 744.3171201814059,
		"PlayTime": 744.3171201814059,
		"DataSize": "",
		"RecordingEnviron": "silent room",
		"NoiseEnviron": "",
		"RecordingDevice": "audio recorder",
		"DirectoryPath": "",
		"FileFormat": "wav"
	},
	"Patient_info": {
		"SpeakerName": "",
		"Sex": "M",
		"Age": "45",
		"Area": "JL"
	},
	"Test_info": {
		"TestMethod": "Read aloud scripts"
	}
}
```

### 데이터 카테고리
-----
| 대분류              | 속성 표기                    | 의미                | 타입   | 필수여부 | 예시                         |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 기본 정보 (Meta Info) | meta.Language               | 언어                | string | Y        | "KOR"                        |
| 기본 정보 (Meta Info) | meta.Version                | 버전                | string | Y        | "1.0v"                       |
| 기본 정보 (Meta Info) | meta.RecordDate             | 녹음날짜            | string | Y        | “2021-05-21”                 |
| 기본 정보 (Meta Info) | meta.FillingDate            | 수정날짜            | string |          | “2021-05-22”                 |
| 기본 정보 (Meta Info) | meta.RecordHistory          | 수정기록            | string | Y        | “2021-05-22”                 |
| 기본 정보 (Meta Info) | meta.Distributer            | 수행기관            | string | Y        | “한림대학교 평촌병원”        |
| 기본 정보 (Meta Info) | meta.FileName               | 음원파일이름        | string | Y        | “ID0001.mp3”                 |
| 기본 정보 (Meta Info) | meta.SampRate               | 음원의 SamplingRate | number | Y        | 44100(Hz)                    |
| 기본 정보 (Meta Info) | meta.Frequency              | 주파수              | number | Y        | 16bps                        |
| 기본 정보 (Meta Info) | meta.StartPos               | 말소리 시작지점     | number | Y        | 10(ms)                       |
| 기본 정보 (Meta Info) | meta.EndPos                 | 말소리 종료지점     | number | Y        | 4000(ms)                     |
| 기본 정보 (Meta Info) | meta.PlayTime               | 총 재생 시간        | number | Y        | 5000(ms)                     |
| 기본 정보 (Meta Info) | meta.DataSize               | 음원 데이터 크기    | number |          | 5.2(Mbyte)                   |
| 기본 정보 (Meta Info) | meta.RecordingEnv           | 녹음 환경           | string | Y        | "Chamber"                    |
| 기본 정보 (Meta Info) | meta.NoiseEnv               | 노이즈 환경         | string | Y        | "N/A"                        |
| 기본 정보 (Meta Info) | meta.RecordDevice           | 녹음 장치           | string | Y        | "MIC"                        |
| 기본 정보 (Meta Info) | meta.FileCategory           | 파일 종류           | string |          | "Audio"                      |
| 기본 정보 (Meta Info) | meta.DirectoryPath          | 파일 위치           | string |          | “./Auditory/Train/”          |
| 기본 정보 (Meta Info) | meta.FileFormat             | 파일 포맷           | string | Y        | "PCM"                        |
| 기본 정보 (Meta Info) | meta.NumberOfRepeat         | 반복 차수           | string |          | "3"                          |
| 기본 정보 (Meta Info) | meta.Distance               | 녹음 거리           | string |          | "50"                         |
| 기본 정보 (Meta Info) | meta.QualityStatus          | 품질 상태           | string |          | "Available"                  |
| 환자 정보 (Patient Info) | patient.SpeakerName       | 환자 이름           | string |          | "HJH"                        |
| 환자 정보 (Patient Info) | patient.Gender            | 성별                | enum   | Y        | 0 : 남, 1 : 여               |
| 환자 정보 (Patient Info) | patient.Age               | 나이                | number | Y        | 27                           |
| 환자 정보 (Patient Info) | patient.Geo               | 거주지              | string | Y        | “안양시”                     |
| 질병 정보 (Disease Info) | Disease.Disease           | 질병 타입           | enum   | Y        | 0 : 뇌졸중, 1 : 퇴행성 뇌질환, 2 : 말초성 뇌신경장애, 3 : 기타/복합 |
| 질병 정보 (Disease Info) | Disease.Subcategory1      | 뇌질환 카테고리     | enum   |          | 0 : 경도 등급, 1 : 중등도 등급, 2 : 고도 등급 |
| 질병 정보 (Disease Info) | Disease.GradeCategory1    | 뇌질환 장애 등급 카테고리 | enum   |          | 0 : 언어, 1 : 청각, 2 : 기타/복합 |
| 질병 정보 (Disease Info) | Disease.Subcategory2      | 언어·청각 카테고리  | enum   |          | 0 : 경도 등급, 1 : 중등도 등급, 2 : 고도 등급 |
| 질병 정보 (Disease Info) | Disease.GradeCategory2    | 언어·청각 장애 등급 카테고리 | enum   |          | 0 : 기능성, 1 : 후두, 2 : 구강, 3 : 기타/복합 |
| 질병 정보 (Disease Info) | Disease.Subcategory3      | 후두 카테고리       | enum   |          | 0 : 경도 등급, 1 : 중등도 등급, 2 : 고도 등급 |
| 질병 정보 (Disease Info) | Disease.GradeCategory3    | 후두 장애 등급 카테고리 | enum   |          | 0 : 경도 등급, 1 : 중등도 등급, 2 : 고도 등급 |
| 검사 정보 (Test Info) | Test.TestMethod            | 검사 방법           | enum   | Y        | 0 : 단어, 1 : 문장, 2 : 문단, 3 : 준자유발화, 4 : 자유발화 |
| 검사 정보 (Test Info) | Test.Transcript            | 발화 텍스트         | string | Y        | “크리스마스는 0월 0일입니다.” |



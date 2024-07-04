AI HUB '립리딩(입모양) 음성인식' 데이터셋은 다양한 환경에서 복잡한 음성인식 기반 서비스 제공을 위해 음향 외 시각 정보를 활용하여 입모양 인식을 위한 다양한 각도 및 소음환경에서 녹화된 오디오 및 비주얼 데이터로 구성된 융합 데이터셋입니다.

본 데이터셋은 영상 및 음성에 대한 노이즈가 심한 환경에서 음성인식 성능을 보완할 수 있는 입모양 인식이 가능한 형태의 오디오 및 비주얼 데이터를 포함하고 있습니다.

음성데이터는 5분 내외로 정제되었으며, 수집 영상 속 얼굴 및 입술 영역의 바운딩 박스는 OpenCV Face/Lip Detection 알고리즘(dlib 사용)을 통해 68개의 랜드마크로 오토라벨링 되었습니다. 

### 얼굴 랜드마크 예시
---
![이미지](https://github.com/Mamaaaamooooo/minsukeum/blob/main/dlib_landmark.jpg?raw=true)


__※ [dlib 라이브러리 관련 자료(클릭)](https://prlabhotelshoe.tistory.com/4)__

__※ [ 한국어 립리딩 관련 유사 프로젝트 예시 (클릭)](https://github.com/dnwjddl/LipReading_Korean/tree/master)__

__※  추가적으로 AIHUB의 데이터 설명서 및 활용가이드를 읽어 보는 것을 추천합니다.__


### 데이터 구축 규모
--------
| 데이터 종류 | 데이터 형태 | 데이터 규모|
|:---:|:---:|:---:|
| 원천데이터-영상 | .mp4 | 5,750 시간|
| 원천데이터-음성| .wav | 1,150 시간|
| 원천데이터-텍스트 | .json | 66,420 개|


### 데이터 사이즈
--------
| 종류 | 용량 |
|:---:|:---:|
| Train | 약 18 TB  |
| Val | 약 2 TB  |

### 영상(mp4) 데이터 예시
---
![이미지](https://github.com/Mamaaaamooooo/minsukeum/blob/main/%EC%9E%85%EB%AA%A8%EC%96%91_image.png?raw=true)

__※초상권 보호를 위해 영상 속 인물의 얼굴은 모자이크 처리하였습니다.__
### JSON 데이터 예시 
------
```JSON
{
	 {
        "dataSet": {
            "description": "AI HUB Voice and motion data_Lip voice",
            "url": "https://aihub.or.kr/",
            "version": 1.0,
            "year": "2021"
        },
        "Video_info": {
            "video_Name": "lip_J_1_F_02_C032_A_011.mp4",
            "video_Format": "MP4",
            "video_Duration": "0:05:07",
            "FPS": 30,
            "Resolution": "1920*1080"
        },
        "Audio_info": {
            "Audio_Name": "lip_J_1_F_02_C032_A_011.wav",
            "Audio_Format": "wav",
            "Audio_Duration": "0:05:07",
            "Sampling_rate": "48Khz",
            "Channel(s)": 2
        },
        "Audio_env": {
            "Noise": 1
        },
        "Video_env": {
            "env": "indoor_light",
            "Angle": "A"
        },
        "Sentence_info": [
            {
                "ID": 1,
                "topic": "health/diet",
                "sentence_text": "교통사고로 큰 부상을 겪고 난 뒤 외출하기가 너무 힘들어져서 너무 외로워.",
                "start_time": 3.712,
                "end_time": 9.770666666666667
            },
            {
                "ID": 2,
                "topic": "health/diet",
                "sentence_text": "지난달부터 남편이 소화가 잘 안 되고 가끔 헛구역질도 난다고 해서 엊그제 병원에 다녀왔었어. 남편이 걱정돼.",
                "start_time": 12.714666666666666,
                "end_time": 22.698666666666668
            ],
        "speaker_info": {
            "speaker_ID": "C032",
            "Specificity": "C",
            "Gender": "F",
            "Age": 2,
            "Accent": "N"
        },
        "Bounding_box_info": {
            "Face_bounding_box": {
                "xtl_ytl_xbr_ybr": [
                    [
                        211,
                        712,
                        865,
                        1366
                    ],
                    [
                        211,
                        711,
                        865,
                        1366
                    ],
                }
            }
    }
}
```

### 데이터 카테고리
-----
| 번호 | 항목                      | 타입    | 필수여부 | 영문명                   | 한글명                    |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 1    | dataset                   | object  | Y        | dataset                  | 데이터셋                  |
| 1-1  | description               | string  | Y        | description              | 데이터 정보               |
| 1-2  | url                       | string  | Y        | url                      | 데이터셋 url (AIHUB 홈페이지) |
| 1-3  | version                   | number  | Y        | version                  | 데이터 버전               |
| 1-4  | year                      | string  | Y        | year                     | 연도                      |
| 2    | video_info                | object  | Y        | video_info               | 영상 정보                 |
| 2-1  | video_name                | string  | Y        | video_name               | 영상 파일명               |
| 2-2  | video_format              | string  | Y        | video_format             | 영상 포맷                 |
| 2-3  | video_duration            | string  | Y        | video_duration           | 영상 길이                 |
| 2-4  | FPS                       | number  | Y        | FPS                      | 프레임                    |
| 2-5  | resolution                | string  | Y        | resolution               | 해상도                    |
| 3    | audio_info                | object  | Y        | audio_info               | 음성 정보                 |
| 3-1  | audio_name                | string  | Y        | audio_name               | 음성 파일명               |
| 3-2  | audio_format              | string  | Y        | audio_format             | 음성 포맷                 |
| 3-3  | audio_duration            | string  | Y        | audio_duration           | 음성 길이                 |
| 3-4  | sampling_rate             | string  | Y        | sampling_rate            | 오디오 샘플링레이트       |
| 3-5  | channel(s)                | number  | Y        | channel(s)               | 오디오 채널 수            |
| 4    | audio_env                 | object  | Y        | audio_env                | 음성 환경                 |
| 4-1  | noise                     | number  | Y        | noise                    | 소음환경                  |
| 5    | video_env                 | object  | Y        | video_env                | 영상 환경                 |
| 5-1  | env                       | string  |          | env                      | 촬영환경                  |
| 5-2  | angle                     | string  | Y        | angle                    | 촬영각도                  |
| 6    | sentence_info             | array   | Y        | sentence_info            | 문장정보                  |
| 6-1  | id                        | string  | Y        | id                       | 문장 ID                   |
| 6-2  | topic                     | string  | Y        | topic                    | 발화주제                  |
| 6-3  | sentence_text             | string  | Y        | sentence_text            | 발화내용                  |
| 6-4  | start_time                | number  | Y        | start_time               | 발화 시작 시간            |
| 6-5  | end_time                  | number  | Y        | end_time                 | 발화 종료 시간            |
| 7    | speaker_info              | object  | Y        | speaker_info             | 발화자 정보               |
| 7-1  | speaker_ID                | string  | Y        | speaker_ID               | 발화자 ID                 |
| 7-2  | specificity               | string  | Y        | specificity              | 특성                      |
| 7-3  | gender                    | string  | Y        | gender                   | 성별                      |
| 7-4  | age                       | number  | Y        | age                      | 연령대                    |
| 7-5  | accent                    | string  | Y        | accent                   | 사투리                    |
| 8    | bounding_box_info         | object  | Y        | bounding_box_info        | 바운딩박스 정보           |
| 8-1  | Face_bounding_box         | array   | Y        | Face_bounding_box        | 얼굴 영역 바운딩박스      |
| 8-1-1| xtl_ytl_xbr_ybr           | number  | Y        | xtl_ytl_xbr_ybr          | 얼굴 영역 좌표값          |
| 8-2  | Lip_bounding_box          | array   | Y        | Lip_bounding_box         | 입술 영역 바운딩박스      |
| 8-2-1| xtl_ytl_xbr_ybr           | number  | Y        | xtl_ytl_xbr_ybr          | 입술 영역 좌표값          |


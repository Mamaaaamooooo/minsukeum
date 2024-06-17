# 데이터 설명

KorNLI는 카카브레인에서 만들어 공개한 데이터로, 자연어 이해(Natural Language Understanding), 자연어 추론(Natural Language Inference) 등의 작업에 활용할 수 있습니다. 데이터 정보는 다음과 같습니다.


#### 데이터 사이즈 

| 종류 | 내용 |
| --- | --- |
| multinli_train <br/> (Multi-Genre NLI) |   392,702 &nbsp; examples |
| snli_train <br/> (Standard NLI)  |    550,152 &nbsp; examples |
| Xnli_dev <br/> (Cross-lingual NLI)  |   2,490 &nbsp; examples |
| xnli_test  |  5,010 &nbsp; examples |

#### 데이터 구조 :
| 속성명 | 내용 |
| --- | --- |
| text | 문장 |
| pair | text와 쌍이 되는 문장 |
| label | text, pair 사이의 관계 |


### 예시: 
| Example   | English Translation                                          | Label         | 
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------- |  
| P: 저는, 그냥 알아내려고 거기 있었어요.<br />H: 이해하려고 노력하고 있었어요. | I was just there just trying to figure it out.<br />I was trying to understand. | Entailment    |  
| P: 저는, 그냥 알아내려고 거기 있었어요.<br />H: 나는 처음부터 그것을 잘 이해했다. | I was just there just trying to figure it out.<br />I understood it well from the beginning. | Contradiction |  
| P: 저는, 그냥 알아내려고 거기 있었어요.<br />H: 나는 돈이 어디로 갔는지 이해하려고 했어요. | I was just there just trying to figure it out.<br />I was trying to understand where the money went. | Neutral       |

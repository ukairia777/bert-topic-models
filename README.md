# Korean Contextualized Topic Models
## 모델 소개
BERT 기반의 문맥을 반영한 한국어 토픽 모델입니다. 모델은 CombinedTM을 사용합니다.

* 토크나이저로는 형태소 분석기 Mecab을 사용.
* BERT로는 다국어 SBERT인 'sentence-transformers/xlm-r-100langs-bert-base-nli-stsb-mean-tokens'를 사용.

## High-level sketch of CombinedTM
![image](https://user-images.githubusercontent.com/73151616/154487038-aa4f1edb-4bf7-484f-a2ac-76b2aa9d2e06.jpg)

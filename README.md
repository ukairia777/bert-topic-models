# Korean Contextualized Topic Models
## 모델 소개
BERT 기반의 문맥을 반영한 한국어 토픽 모델입니다. 모델은 CombinedTM을 사용하고 한국어에서 사용할 수 있도록 토크나이저와 SBERT를 수정하였습니다.

* Paper : https://arxiv.org/abs/2004.03974
* 토크나이저로는 형태소 분석기 Mecab을 사용.
* BERT로는 다국어 SBERT인 'sentence-transformers/xlm-r-100langs-bert-base-nli-stsb-mean-tokens'를 사용.
* 토픽의 수는 임의로 50으로 결정.
* 별도 불용어 제거 등의 추가 전처리는 진행하지 않았음. (진행할 경우 더 좋은 결과를 얻을 수 있을 것으로 기대.)
* 실험을 위해 Vocab size는 3,000을 사용. (단, 원본 Repo에 따르면 Vocab size는 2,000 단어 이하를 권장.)

## 시각화 결과
![topic model](https://user-images.githubusercontent.com/73151616/154489860-678b23bb-7959-4587-bc96-1309a4ea1493.PNG)

## High-level sketch of CombinedTM
* CombinedTM은 Bag of Words 문서 벡터와 SBERT로부터 얻은 Contextualized Embedding을 concat하여 사용하는 모델입니다.

![image](https://user-images.githubusercontent.com/73151616/154487038-aa4f1edb-4bf7-484f-a2ac-76b2aa9d2e06.jpg)

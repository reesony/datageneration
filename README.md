# DataGeneration

This repository contains the code of DataGeneration using nlpaug and python library.
This data utilized SNIPS dataset and the link is as follows:
https://github.com/LeePleased/StackPropagation-SLU

## KONKUK graduation project
- bibleqa
  - bibleqa dataset is from bible.
  - use LDA(latent dirichlet allocation) and tf-idf to extract keyword of bible and extract sentence using keyword of bible
  - tf-idf is a method of weighting words according to frequency statistics. And LDA(latent dirichlet allocation) is a statistical modeling technique used to distinguish text in documents according to specific meanings.
  - consisted of 4000 sentences.
- playmedia
  - from SNIPS dataset using label which is PlayMusic or AddToPlaylist
  - be extracted randomly
- generalqa
  - from SNIPS dataset using label which is not PlayMusic or AddToPlaylist
  - be extracted randomly

### data_augmentation
- how to augmentate data
  * domain classification 모델을 학습하기 위한 데이터셋 구축
  * nlpaug 라이브러리를 활용하여 각 sentence별로 몇몇 단어를 synonym으로 대체
  * bibleqa/playmedia/generalqa로 구분하기 위한 데이터셋 구축 코드
  * 하나의 클래스만 데이터가 상대적으로 많을 시 classifier를 통한 회귀 과정시 majority class에 가깝도록 회귀가 되므로 데이터 불균형 문제가 생기지 않도록 각각 4000여개 정도의 데이터셋 비율을 맞춤

### make_dataset_keyword
- how to make dataset of keyword
  * keyword_extraction 모델을 학습하기 위한 데이터셋 구축
  * snips 데이터셋을 가공하여 재사용함
  * sentence label은 제거한 뒤 token별 label만 활용함

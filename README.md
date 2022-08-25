# DataGeneration

This repository contains the code of DataGeneration using nlpaug and python library.
This data utilized SNIPS dataset and the link is as follows:
https://github.com/LeePleased/StackPropagation-SLU

## KONKUK graduation project
- bibleqa
  - bibleqa dataset is from bible.
  - use LDA(latent dirichlet allocation) and tf-idf to extract keyword of bible and extract sentence using keyword of bible
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
  * 각각 4000여개 정도의 데이터셋 비율을 맞춤

### make_dataset_keyword
- how to make dataset of keyword
  * keyword_extraction 모델을 학습하기 위한 데이터셋 구축
  * snips 데이터셋을 가공하여 재사용함
  * sentence label은 제거한 뒤 token별 label만 활용함

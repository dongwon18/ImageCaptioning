# ImageCaptioning
- basic Image Captioning model using flickr-8k from kaggle
- since the result is not sufficient, parameter file is not included.

## Parameters
- image size: 256 x 256
- batch size: 32
- threshold for word: 4
- epoch: 20

## Encoder
- use pretrained resnet101 as mentioned in the referencing paper
- remove the last layer FC layer for making latent vector
- add intermediate FC layer

## Decoder
- use LSTM for decoder(referencing the paper)
- for output layer, add Dense layer

## Result
- captions as predicted result are not understandable.

## 배운점
- Encoder에서 이미지를 압축한 내용을 latent_vector의 형식으로 저장한다. 이 때 CNN 모델 중 하나인 Resnet101을 사용한다.
- Decoder에서 해당 이미지에 해당하는 captions의 내용을 분석하여 latent_vector에 알맞은 caption을 학습한다.
- Dataset을 원하는 방식으로 가공하여 사용할 수 있게 되었다.

## 한계점
- 결과를 분석하기 위해 BLEU score를 사용하여 정량적으로 평가하는 것이 바람직할 것이다.

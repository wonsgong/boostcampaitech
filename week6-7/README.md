
# [[Week 6-7] CV / Data Visualization ]
> 여기엔 매일매일의 간단한 내용과 느낌점을 두서없이 적어놓습니다.  
> 수업 필기는 `goodNotes` 앱을 활용해서 따로 폴더에서 확인.(수업 ppt는 가려둠.)  
> 피어세션 :    
> 과제    : 개인 코랩에 올려놓는 중.  

## Lecture
### Day25.  
> CV : Image Classification 1, Annotation Data Efficient Learning.  
> Data Visualization : Polar Coordinate, Pie Charts, 다양한 시각화 라이브러리.  
> 과제 : VGG-11 구현 및 Fine-tuning.  
1. CV   
    1강에선 이미 배웠던 내용들을 복습한 느낌이었다.  
    2강에서 배운 `Knowledge Distillation` 과 `Self-Learning` 에 대한 내용은 상당히 흥미로웠다.  
    일정이 생각보다 여유로워 내일은 직접 구현에 도전해봐야겠다.  
2. Data Visualization  
    극 좌표계를 사용한 시각화는 마스터님 말씀처럼 EDA 보단 보여주기용인듯 하다.  
    이번 내용보다는 다음에 배울 인터렉티브 시각화를 얼른 배우고 싶었다.  
    `Waffle Chart` 를 인포그래픽 만들 때 잘 활용해봐야겠다.  
3. 과제  
    `VGGNet` 같은 경우는 너무 유명해서 간단한 CNN 모델 구현 시에 일부 레이어 모습을 종종 사용했었다.  
    `Fine-tuning` 에 경우도 지난 `P-stage` 에서 많이 사용해봤기 때문에 어려움 없이 과제를 수행했다.  
    확실히 `Transfer learing` 이 수렴 속도가 빠르다는 걸 느꼈다.    
```
! 하루 마무리 : level1 에서 많은 양을 짧은 시간동안 배워서 그런지 첫날엔 여유로웠다.  
```

### Day26.  
> CV : Image Classification 2.  
> Data Visualization : Interactive Visuailization.  
1. CV   
    backbone 으로 사용할 수 있는 다양한 cnn 모델들을 배웠다.  
    내일은 `self-learning` 논문을 읽고 P-Stage 에서 사용한 데이터셋을 활용해 구현해봐야겠다.  
2. Data Visualization  
    라이브러리가 잘 되어있어서 문법의 큰 차이 없이 할 수 있다는 점을 느꼈다.  
    확실히 정적 시각화보다는 느리고 꼭 필요할 때만 사용해야겠다.      
```
! 하루 마무리 : 안주하지말고 더 공부하자.  
```

### Day27.  
> CV : Baseline 구축.  
> Data Visualization : Custom Matplotlib Theme, Image & Text Visualization Techniques.  
> 과제 : Data Augmentation.  
1. CV  
    `Self-learning` , `RandAugment` 논문을 읽으며 하루를 보냈다.  
    피어세션에서 나온 개인 Baseline 구축을 `P-Stage` 에서 진행한 코드 기반으로 하고 있다.  
    `P-Stage` 코드를 어떻게 정리해서 git에 올릴까 했는 데 나의 Baseline 으로 사용할 수 있게금 해서 올려야겠다.  
2. Data Visualization  
    주로 darkmode를 쓰는 데 이번 `Matplotlib` 테마를 다크모드로 바꾸는 것을 보고 바로 모듈화했다.  
    주피터 환경에서 진행 시에 항상 설정하고 사용해야겠다.  
3. 과제  
    `torchvision.transforms` 을 사용해서 `Data Augmentation` 를 해줬다.  
    과제에서 제시된 내용들을 수행해보니 역시 데이터에 대한 이해가 있어야 증강도 하겠구나 싶었다.  
    아니면 `RandAugment` 사용이 맞는듯 하다.  
    `Albumentations` 를 이번에 사용해봤는 데 더 빠르고 다양한 방법에다가 `bbox` 를 함께 고려해준다는 점에서 큰 매력을 느꼈다.  
    그래서 baseline 짤 때는 `Abumentations` 을 이용해서 할 예정이다.  
```
! 하루 마무리 : 뜻을 세웠으면 우직하게 밀고 나가자. 흔들리지말고.  
```

### Day28.  
> CV : Semantic Segmentataion.  
> 과제 : Classification to Segmentation.  
1. CV  
    이번 강의에서는 모델을 위주로 소개를 해주셔서 학습 방식과 추론 방법에 대한 부분을 따로 공부했다.  
    reference로 주어진 논문을 읽어보니 큰 흐름 이해에 도움이 되었다.  
    머리로만 이해하고 넘어가지말고 직접 구조를 시각화해보거나, 구현해보는 노력을 해보니 어떤 부분을 제대로 이해하지 못했는 지
    알 수 있어서 좋았고, 직접 해보는 게 역시나 중요했다.  일단 해보자.  
2. 과제  
    VGG11의 `fully connected layer` 를 `fully convolution layer` 로 변경하는 건 어렵지 않았다.  
    과제에선 한번에 `upsampling` 을 진행하는 데 `U-Net` 과 같은 방식으로 구현해보다가 오늘 하루가 다갔다.  
    `skip connection` 에서 어떻게 `copy-crop` 할 지에 대한 고민이 남아있었는 데 슬랙에 올라온 내용이 도움이 되었다.  
    아직 미완성이니 내일 마무리해야겠다.  
```
! 하루 마무리 : 강의나 과제 자체의 난이도는 높지 않으나 하나하나 이해하고 적용하려니 난이도가 급 상승이다. 재밌다.  
```

### Day29.  
> CV : Object Detection.  
> 과제 : Classification to Segmentation.  
1. CV  
    `Object Detection` 의 큰 흐름을 이해할 수 있었다.  
    요즘의 트렌드로 알려주신 `DETR` 나 `CenterNet` 같은 경우는 그런게 있다 정도로만 넘어갔다.  
    논문을 읽어보고 구현해봤어야 하는 데 팀원 구하느라 못해봤다 주말에 도전해야겠다.  
2. 과제  
    `skip connection` 에서 `copy-crop` 을 `U-Net` 코드에서 도움을 얻어서 진행했다.  
    다만 `backbone.fc_out.weight` 의 shape 이 달라서 주어진 모델 대신  
    shape 이 같은 모델로 학습시켜서 테스트해봤다.  
```
! 하루 마무리 : 공부보다 팀원 구하는데 더 많은 시간을 썼던 하루였다.  얼른 구하고 공부하자.  
```

### Day30.  
> CV : CNN Visualization, AutoGrad.  
1. CV  
    CNN 모델의 시각화는 모델이 왜 그런 결정을 내렸는 지에 대한 부분만 생각해봤었는데,  
    모델의 결과를 시각화하는 부분이 있다라는 걸 알게되었다.  
    그중에서도 `Class Visualize` 를 활용한다면 CNN 모델이 현실 세계의 객체들을  
    어떻게 생각하고 있는 지 시각화할 수 있을 거라는 생각에 상당한 흥미를 느꼈다.  
    오늘 하루는 팀원을 구하느라 복습과 구현을 해보지 못했지만, `Class Visualize` 는 꼭 구현해봐야겠다.  
    선택과제도 내일 도전해야겠다.  
```
! 하루 마무리 : 팀원 구합니다. 사실 친구 구해요.  
```

### Day31.  
> CV : Instance/Panoptic Segmentation and Landmark Localization.  
> 과제 : Human Pose Estimation Using Hourglass Network.  
1. CV  
    강의 마지막에 해주신 마스터님의 이야기(다양한 task들이 유사한 디자인 패턴으로 이루어져있다.)를 바탕으로 복습했다.  
    원하는 task 를 명확하게 정의하고 구현하는 것이 중요하다는 걸 다시한번 느꼈다.  
2. 과제  
    `Hourglass Net` 에 경우 학습 시에는 쌓여있는 `Hourglass` 에서 나온 모든 결과를 가지고 loss 를 구하고,  
    추론 시에 마지막 결과값만을 가지고 하면 된다는 것을 알았다.  
    `heatmap` 에서 `Landmark` 좌표값을 얻을 때 일정 값의 `threshold` 을 적용해서 구하는 방법과,  
    `np.unravel_index` 을 이용해 구하는 방법을 적용해서 해봤는데 역시나 큰 차이는 없었다.  
    이번 오피스아워를 잘 들어봐야겠다.  
```
! 하루 마무리 : 팀을 잘 마무리해서 다행이다. 이제 좀 더 집중해서 공부하자.  
```

### Day32.  
> CV : Conditional Generative Model.  
> 과제 : Conditional GAN.  
1. CV  
    이미지 생성 모델에 대한 발전 흐름을 알수 있었다.  
    `generator` 와 `discriminator` 의 `loss` 를 구하는 방법과 컨셉을 배웠다.  
2. 과제  
    `cGAN` 논문을 구현하는 방식으로 진행되었는 데, real_label 의 shape 을 어떻게 맞춰줄 지가 고민이었다.  
    `one-hot` , `Embedding` 두 가지를 고민하고 둘다 적용해봤지만, 제대로 학습이 되지 않았다.  
    과제 내용을 추가해서 올려주신다고 하니 논문을 좀 더 읽어보고, 올라온 과제를 마무리해야겠다.  
```
! 하루 마무리 : 생성 모델이 생각보다 많은 곳에 쓰일 수 있음에 좀 더 공부해봐야겠다는 걸 느낀 하루였다.  
```

### Day33.  
> CV : Multi-modal Learning, Image Captioning.  
> 과제 : Conditional GAN.  
1. CV  
    `Multi-modal` 수업을 듣고나니 `CV`뿐만 아니라 다른 도메인에 대한 지식도 공부해야겠다는 걸 느꼈다.  
    추석 기간 `NLP` 강의를 들어야겠다.  
2. 과제  
    `QuickDraw` 데이터를 이용했을 때는 생각보다 잘 생성이 되지않아,  
    `MNIST`를 이용해봤다. 둘다 흑백 이미지지만, `QuickDraw`는 `(3,255,255)` 라서 제대로 되지 않은 느낌을 받았다.  
    `grayscale` 로 변환해서 학습 시에는 좀 전보다는 나아졌지만, 그래도 잘 모르겠다.  
    `Paper with Code` 에 있는 코드로 내일 해볼 예정이다.  
```
! 하루 마무리 : 공부를 하면 할 수록 더 공부를 해야겠다는걸 느낀 하루였다.  
```

### Day34.  
> CV : 3D Understanding.  
> 과제 : De-focusing Using Depth Map.  
1. CV  
    `Multi-modal` 에 이어서 실제 세상에 적용할 수 있는 도전적인 과제였다.  
    좀 더 실제 문제를 들여다보고 적용해볼 수 있는 시야를 배웠다.  
2. 과제  
    `Depth Map` 을 통해서 이미지의 어떤 영역으로 구분이 가능한 지 파악하고,  
    블러를 통해서 구분해보는 과제였다.  
    단순한 이미지 처리라는 느낌을 받았고, 논문을 읽어봐야겠다.  
```
! 하루 마무리 : 이제 연휴인데 NLP수업과 CV 복습을 해야겠다.  
```

## Week 6 마무리.
CV 개론을 들은 한주였다.  
생각해볼 주제를 던져주시는 강의와 과제를 진행하다보니 명확하게 공부한것 같지는 않아서 아쉽다.  
그래도 논문을 읽어보고 토론 주제를 고민하고 적용하면서 공부를 할 수 있어서 좋았다.  
언제나 답이 있는 문제를 풀수는 없으니 왜 이런 결론을 내렸는 지에 대한 근거를 명확하게 생각하는 것이 중요하다는 걸 다시 한번 느낀 한주였다.  

## Week 7 마무리.
지난주 보다 좀 더 현실의 문제, 도전적 과제를 받아든 느낌을 받았다.  
마스터클래스를 통해서 `내가 왜 딥러닝을 공부하게 되었는 지` 를 다시 한번 떠오르게 되었다.  
사회의 여러가지 문제를 풀기 위해서 공부하게 된 만큼, 사회의 문제에 대한 정의와 접근법을 항상 고민하고 공부해야겠다.  
지난 level1 에 비해 성장하지 못하고 있다는 생각에 조금 힘들었지만, 초심을 생각하고 다시 차근차근 공부하자.  



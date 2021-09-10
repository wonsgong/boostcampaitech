
# [[Week 6] CV / Data Visualization ]
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
## 한주 마무리.
CV 개론을 들은 한주였다.  
생각해볼 주제를 던져주시는 강의와 과제를 진행하다보니 명확하게 공부한것 같지는 않아서 아쉽다.  
그래도 논문을 읽어보고 토론 주제를 고민하고 적용하면서 공부를 할 수 있어서 좋았다.  
언제나 답이 있는 문제를 풀수는 없으니 왜 이런 결론을 내렸는 지에 대한 근거를 명확하게 생각하는 것이 중요하다는 걸 다시 한번 느낀 한주였다.  
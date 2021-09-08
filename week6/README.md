
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
## 한주 마무리.

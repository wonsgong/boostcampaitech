# [Week 12-14] Semantic Segmentation

> 여기엔 매일매일의 간단한 내용과 느낌점을 두서없이 적어놓습니다.  
> 수업 필기는 `goodNotes` 앱을 활용해서 따로 폴더에서 확인.(수업 ppt는 가려둠.)  
> 피어세션 : https://www.notion.so/BoostCamp-CV-5-5ec79e6fc8854e5b905f94314823c1ed
> 과제    : 개인 코랩에 올려놓는 중.  

## Lecture
### Week12
----------------
### Day50
> Semantic Segmentation : Introduction, Competition Overview, Semantic Segmentation의 기초와 이해.  
> Special Mission : FCN8, FCN16, FCN32.  
> Competition : EDA, Baseline 모듈화.  
1. Semantic Segmentation.  
    지난 CV에서 배운 내용을 좀 더 자세하게 설명해준 강의였다.  
    복습한다는 생각으로 다시 들었고, Competition 에 대한 내용은 EDA 시에 도움이 되었다.  
2. Special Mission.  
    `skip connection` 을 구현해볼 수 있는 과제였다.  
    이 역시 큰 어려움 없이 강의자료에서 제공하는 이미지를 보면서 맞춰 진행했다.  
3. Competition.  
    `연구 일지` 를 따로 적긴 하지만 그래도 간단하게 남기는 게 좋을 것 같아 기록하기로 했다.  
    지난번 대회와 같은 데이터셋이라 EDA 를 간단하게 하려고 했는데 보여지는 이미지가 다른 것 같아서  
    지난번 했던 내용에 좀 더 추가해서 EDA를 진행했다.  
    이번엔 `train/valid set` 을 나눠서 제공했기 때문에 이게 얼마나 좋은 지 확인을 더 했다.  
    이번 대회도 목적과 근거를 찾아가며 공부해보자.  
```
! 하루 마무리 : 제출 횟수를 남긴다고 아쉬워 말고 하나를 제대로 해보자.  
```

### Day51
> Semantic Segmentation : FCN의 한계를 극복한 모델 1,2,  Unet 계열 모델.   
> Competition : Baseline 공유, Unet 학습, EDA, valid set 검증.  
1. Semantic Segmentation.  
    성능 향상을 어떤 방식으로 이뤄냈는 지를 나눠서 설명해주셔서 접근하기 좋았다.  
    구조 변경도 있지만, `loss`,`augment` 관점에서 설명해준 것도 좋았다.  
    이번 대회에 적용하면 좋을 것들을 얻을 수 있었던 수업이었다.  
2. Competition.  
    어제 `valid set` 이 잘 나눠져 있다는 것을 확인했는데,  
    LB 상에서의 차이가 크게(0.05 이상) 나서 왜 그럴까를 분석해봤다.  
    아직 표본이 적지만, LB 데이터에 배터리가 적을 것이라는 가설을 가지고 분석해보고 있다.  
    `Unet` 계열을 base 로 잡고 실험을 해야겠다.  
```
! 하루 마무리 : 이론과 실습을 동시에 하기가 쉽지 않네.  
```

### Day52
> Semantic Segmentation : 대회에서 사용하는 방법 1,2.  
> Competition : Loss 적용, Augmentation 실험, draw mask 문제.  
1. Semantic Segmentation.  
    아직 해보기엔 조금 이른 방법론을 많이 소개해주셨다.  
    확실히 뒤로 갈수록 적용해봐야 할 것들이다 보니 미리 고민할 수 있어서 좋았다.  
    뭘 해보면 좋을 지 적어놓고 진행하자.  
2. Competition.  
    `Focal-Dice loss`, `Tversky loss` 를 테스트해보고,  
    `elastic` , `griddropout` 을 실험해봤다.  
    좀 더 일반화된 학습이 될 것이라 생각했는데, 세팅을 잘못했는지 과도하게 학습이 되지않아서 해결중이다.  
    `coco format` 이 어떻게 mask 를 생성하는 지 조금 더 찾아봐야겠다.  
    안에 겹쳐지게 되는 경우 그릴때 든 의문을 슬랙에 올렸으니 내일 확인하고 이후 학습에 반영해야겠다.  
```
! 하루 마무리 : 급 할일이 많아진 느낌이다. 차근차근 하나씩 해보자.  
```

### Day53
> Competition : Data Imbalance,  MMSegmentation 이용.  
1. Competition  
    `Data Imbalance` 문제를 해결하기 위해서 지난 대회에서 사용했던  
    `mosaic` 기법을 이용해서 배터리 : 옷 = 2 : 2 로 이미지를 만들어서 진행했다.  
    이미지 안에 객체가 배터리,옷 만 있는 경우로 진행했다.  
    해당 데이터를 이용했더니 성능이 확실하게 올라가서 다른 부족한 데이터에도 적용했는데 큰 차이가 없었다.  
    좀 더 개선할 수 있는 것이 뭘지 더 고민하고 진행해야겠다.  
```
! 하루 마무리 : 큰 모델에 적용하기 전에 데이터 증강으로 성능이 올라서 기분이 좋다.  
```

### Day54
> Competition : MMSegmentation, SOTA모델, 데이터 전처리.  
1. Competition  
    MMSegmentation 사용 시에 제대로 학습이 되지 않아서 해결중이다.  
    제대로 이해하고 사용하자.  
    데이터 전처리에 경우 오늘 들은 `마스터 클래스` 에서 소개해준 방법들을 적용해보자.  
```
! 하루 마무리 : 오늘 하루는 큰 성과가 없어서 아쉽다.
```

## Week13
----------------
### Day55
> Semantic Segmentation : Semantic Segmentation 연구 동향 1,2.  
> Competition : efficientnetv2, heavyaug, data balance.  
1. Semantic Segmentation  
    `HRNet` 이 왜 등장했고, 어떻게 좋은 성능을 낼 수 있었는 지 이해할 수 있었다.  
    지금 좋은 모델들에 적용해서 실험해봐야겠다.  
    `WSSS` 에 경우 이렇게 학습할 수도 있구나 정도로만 이해하고 넘어갔다.  
2. Competition  
    `Unet` 을 베이스로 진행하고 있고, 백본 교체로 좋은 성능을 가져올 수 있었다.  
    이후 `OneOf` 를 이용해서 좀 더 헤비한 augmentation 을 적용하고 실험중에 있다.  
    데이터의 불균형을 줄이고자 많은 건 줄이고, 부족한 건 늘려서 균형을 맞춰본다면 어떨까라는 아이디어로 현재 실험중에 있다.  
    균일하게 학습이 되겠지만, 데이터 증강을 통해 늘어난 카테고리가 과적합될 것 같기도해서 결과를 봐봐야 될 것 같다.  
    좀 더 의미있는 실험을 진행하자.  
```
! 하루 마무리 : 보다 제너럴하게 학습시킬 수 없을까?
```

### Day56
> Competition : HRNet, pseudo labeling.  
1. Competition  
    어제 진행한 데이터 균형 맞춰서 한 건 큰 성과가 없었다.  
    `HRNet` 을 백본으로 `upernet` 을 학습시킨 결과가 현재 좋은 성능을 보이고 있어서  
    이를 기반으로 좀 더 발전시켜 나가야겠다.  
    `pseudo label` 에 경우, LB 기준 가장 좋은 모델을 가지고 `threshold = 0.9` 로 진행했다.  
    내일 멘토링에서 도움을 좀 더 받아서 더 진행해보자.  
```
! 하루 마무리 : 대회 절반이 지나가고 있으니까 다시 한번 차분히 돌아보는 시간을 가져보자.  
```

## Week 12 마무리.
아무래도 한번 더 보는 데이터다 보니 좀 더 빠르게 감을 잡을 수 있었다.  
내 모델이 뭘 못하고 있는 지, 내가 해결해야할 과제가 무엇인지 정하고,  
우선 순위를 정해서 해결하라는 마스터님의 말씀을 생각하고  
주말 동안 다음주에 무엇을 해야할 지 고민하고 정리해야겠다.  
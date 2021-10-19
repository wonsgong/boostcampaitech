# [Week 12-14] Semantic Segmentation

> 여기엔 매일매일의 간단한 내용과 느낌점을 두서없이 적어놓습니다.  
> 수업 필기는 `goodNotes` 앱을 활용해서 따로 폴더에서 확인.(수업 ppt는 가려둠.)  
> 피어세션 : https://www.notion.so/BoostCamp-CV-5-5ec79e6fc8854e5b905f94314823c1ed
> 과제    : 개인 코랩에 올려놓는 중.  

## Lecture
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
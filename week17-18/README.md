# [Week 15-16] Model Optimization

> 여기엔 매일매일의 간단한 내용과 느낌점을 두서없이 적어놓습니다.  
> 수업 필기는 `goodNotes` 앱을 활용해서 따로 폴더에서 확인.(수업 ppt는 가려둠.)  
> 피어세션 : https://www.notion.so/BoostCamp-CV-5-5ec79e6fc8854e5b905f94314823c1ed
> 과제    : 개인 코랩에 올려놓는 중.  

## Lecture
### Week17
----------------
### Day75
> Model Optimization : 최적화 소개 및 강의 개요, 대회 및 데이터셋 소개.
1. Model Optimization.
    최적화 방법에 대한 이론을 공부하고 대회 task을 이해한 하루였다.  
    강의만 듣고 최종 프로젝트에 집중했다.  
    꼭 주말에 내용 복습해야겠다.  
```
! 하루 마무리 : 스케줄 관리를 잘해보자.  
```

### Day76
> Model Optimization : AutoML 이론, AutoML 실습.  
1. Model Optimization.
    `AutoML` 의 수학 베이스가 어떤 지 알수 있었고,  
    컨셉과 방법에 대해서 개념적으로만 이해하고 넘어갔다.  
    `Optuna` 를 이용한 실습에서는 대회 task 에 맞게 진행했다.  
    내일 완료되면 확인하고 결과 분석을 해봐야겠다.  
    최종 프로젝트 데이터셋을 만들고 있는 데 어느정도 잘 되고 있는 데 해상도를 높일 수 있는 방법을 찾아봐야겠다.  
```
! 하루 마무리 : 룰루, 즐겁게 하자
```

### Day77
> Model Optimization : Data Augmentation, AutoML 결과분석.  
1. Model Optimization.
    `RandAugment` 대한 컨셉과 구현 방법에 대해 배웠다.  
    이미 배웠던 내용이라 어렵지 않게 이해하고 넘어갈 수 있었다.  
    결과 분석에 대해서는 그래프를 이해하고, 상황에 맞는 모델을 선정하면 되는 거라 생각했다.  
    `Optuna` 를 좀 더 공부하고 다시 모델 구조를 찾아봐야겠다.  
    최종 프로젝트 데이터셋은 이제 문제랑도 겹치게 `handwriting` 을 합성해서 테스트해봐야겠다.  
```
! 하루 마무리 : 계획을 잘 세워서 하루를 보내자.  
```

### Day78
> Model Optimization : CV 경량화 기법.  
1. Model Optimization.
    CV 분야에서 사용하는 경량화 기법에 대해서 `prune` 과 `knowledge distillation` 에 대해서 배웠다.  
    관련 논문을 하나하나 읽어봐야 제대로 이해할 수 있을 것 같다.  
    실제 사용 시에 관련 개념을 기억하고 공부해서 사용해봐야겠다.    
```
! 하루 마무리 : 나는 상위 1% 만큼의 노력을 하고 있을까?
```

### Day79
> Model Optimization : 모델 경량화.  
1. Model Optimization.
    경량화 transformer 모델인 `mobilevit` 를 구현해서 학습을 진행했다.  
    성능은 좋게 나왔지만, inference time 이 너무 오래걸려서 경량화를 다시 진행하고 있다.  
    최종 프로젝트에 사용하기 위한 데이터도 pdf 파일만 있으면 알아서 만들수 있도록 코드 변경을 해야겠다.  
```
! 하루 마무리 : 두 마리 토끼를 잡아보자.
```

## Week 17 마무리.
명확하게 무엇을 해야 할 지 이해하지 못하고 공부를 했던 한 주였다.  
경량화 기법과 방법론은 알지만, 감을 잡지못하고 이것저것 해봤다.  
이번주 아쉬웠던 점들을 보강해서 다음주는 좀 더 의미있는 일주일을 보내면 좋겠다.  

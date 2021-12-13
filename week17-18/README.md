# [Week 17-18] Model Optimization

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

### Day80
> Model Optimization : Tensor Decompostion.  
1. Model Optimization.
    수식에 대한 명확한 이해보다는 개념을 이해하려고 노력했다.  
    사실 몸 상태가 좋지 않아서 강의만 듣고 뭘 더 못해서 다시 공부해봐야겠다.  
```
! 하루 마무리 : 건강 중요해.
```

### Day81
> Model Optimization : Quantization.  
1. Model Optimization.
    인턴을 하면서 삽질을 이미 경험해봤던 내용이라 그래서 그랬구나라는 생각을 가지고 강의를 들었다.  
    지금 생각해보면 좀 더 할수있었겠다는 생각이 들었다.  
    학습 단계에서부터 할 수 있는 `QAT` 를 해봐야겠다.  
```
! 하루 마무리 : 어느덧 12월!
```

### Day82
> Model Optimization : TensorRT, DALI
1. Model Optimization.
    간단한 사용방법에 대한 강의였어서 크게 어렵지 않았다.  
    `nvidia` 플랫폼을 사용하게 되면 적용해봐야겠다.  
```
! 하루 마무리 : 최종 프로젝트에 좀 더 집중하자.  
```

### Day84
> Model Optimization : 최종프로젝트.  
1. Model Optimization.
    최종 프로젝트 데이터 파트를 맡아서 진행하고있다.  
    좀 더 실제와 같은 데이터 제작과 전처리를 고민하고, 버전관리를 하고있다.  
    데이터 제작 파트 수업에서 들었던 내용들을 복습하면서 해야겠다.  
```
! 하루 마무리 : 제대로 해보자.  
```
## Week 17 마무리.
명확하게 무엇을 해야 할 지 이해하지 못하고 공부를 했던 한 주였다.  
경량화 기법과 방법론은 알지만, 감을 잡지못하고 이것저것 해봤다.  
이번주 아쉬웠던 점들을 보강해서 다음주는 좀 더 의미있는 일주일을 보내면 좋겠다.  

## Week 18 마무리.
경량화에 대한 내용 중 `Target Device` 가 무엇인지에 대한 내용이 기억이 남았다.  
`Target Device` 에 대한 명확한 이해를 바탕으로 경량화 전략을 세워야 겠다는 것을 배웠다.  
최종 프로젝트에 좀 더 힘을 많이 쓴 한주였고, 이제 어느정도의 결과물을 내야할 때니까 좀 더 열심히 집중해서 해야겠다.  
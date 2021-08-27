
# [[Week 4-5] Image Classification ]
> 여기엔 매일매일의 간단한 내용과 느낌점을 두서없이 적어놓습니다.  
> 수업 필기는 `goodNotes` 앱을 활용해서 따로 폴더에서 확인.(수업 ppt는 가려둠.)  
> 피어세션 : https://drive.google.com/drive/folders/10awg6wJGwb6Xu-jHX5kLvl8_CmDx3b_0  
> 과제    : 개인 코랩에 올려놓는 중.  

## Overview
> 주제  : 마스크 착용 상태 분류, 카메라로 촬영한 사람 얼굴 이미지의 마스크 착용 여부를 판단하는 Task.  
> 데이터 : 남여(20-70대) 4,500명. 1명 당 7장(마스크 5, 오착용 1, 미착용 1)의 (384,512) Image.  

## Lecture
### Day15.  
> Image Classification : Competition with AI Stages, Image Classification & EDA.  
> Special Mission : EDA.  
1. Image Classification  
	첫 날 강의는 인트로에 느낌이라 쉽게 쉽게 듣고 학습했다.  
	`EDA` 에 대한 개념을 잡을 수 있었다.  
2. Special Mission  
	`EDA` 에 대한 내용은 강의대로 내가 궁금하고 학습이 잘 될 방법을 생각하며 진행했다.  
	제출 한번 해보고 싶어서 조금만 하고 제출해봤다.  
```
! 하루 마무리 : EDA는 정답이 없다는 걸 다시 한번 느꼈고, 좀 더 자세히, 다양한 접근접으로 데이터를 이해해봐야겠다.  
```

### Day16.  
> Image Classification : Dataset, Data Generation.  
> Special Mission : Dataset, Data Generation.  
1. Image Classification  
	Dataset에 대한 transforms을 왜 하는지, 하고나서 어떻게 나올지에 대한 고민을 우선하고 해야겠다.  
	`Pytorch Dataset` 강의 내용과 유사해서 어렵진않았다.  
2. Special Mission  
	`dataset.ImageFolder` 를 활용해서 train dataloader 를 만들었다.  
	이후 `StratifiedShuffleSplit`로 라벨별로 균형있게 나눠서 `train/val dataset` 구현.   
```
! 하루 마무리 : 데이터를 좀 더 많이 들여다보고 이것저것 할때 이유를 가지고 해야겠다.  
```

### Day17.  
> Image Classification : Model 1, Model 2.  
> Special Mission : Model.  
1. Image Classification  
	지난번에 공부했던 Transfer Learning 에 대해 좀 더 자세히 배웠다.  
	구현보다는 어떤 모델을 고르고, 어떻게 학습을 시킬지 에 대한 내용에 좀 더 중점적으로 학습했다.  
2. Special Mission  
	보여준 모델이 `Darknet 53` 이라서 구현되어있는 모델을 참고하면서 구현해보려고 노력했다.  
```
! 하루 마무리 : 파라미터 튜닝을 지난주에 배운 `Ray` 를 써봐야겠다.  
```

### Day18.  
> Image Classification : Training & Inference.  
> Special Mission : Training & Inference.  
1. Image Classification  
	이미 실습에서 하고 있는 부분이었는데 베이스라인과 process를 다시 한번 더 이해할 수 있었다.  
	역시나 문제 정의와 그 문제에 맞는 적절한 메소드를 이용하는 것이 중요했다.  
2. Special Mission  
	제시된 방법들을 적용하고 바꿔가며 학습을 진행해봤다.  
	이 역시 문제에 맞는 방법론을 이해하고 적용하는게 필요했다.  
```
! 하루 마무리 : 개인제출 기간에 할 수 있는 건 다양하게 해본 것 같다. 내일부터 팀전이니 좀 더 생각하고 튜닝해야겠다.  
```


### Day19.  
> Image Classification : Ensemble, Experiment Toolkits & Tips.  
> Data Visualization : seaborn
> Special Mission : Ensemble / Experiment Toolkits.  
1. Image Classification  
	ensemble을 단순히 모델을 여러개 쓴다고 생각했는데 좀 더 다양한 방법론이 있다는 걸 배웠다.  
	마지막에 이야기해주신 내용들(tips) 을 잘 생각하며 다음주 대회에 참여해야겠다.  
2. Data Visualization  
	`seaborn` 에 대한 내용을 딥러닝 입문 때 배웠었는데 그땐 그냥 아 그렇구나 하고 넘어갔는데  
	더 공부하고 다시 공부하니까 어디다가 적용할 수 있겠구나를 느꼈다.  
	역시 아는 만큼 보인다. 내가 알아야 남에게 보여줄 시각화가 가능하다.  
3. Special Mission  
	`Stratified K-fold` 을 이용해서 `train/val dataset` 을 분리해서 학습시켜봤다.   
```
! 하루 마무리 : 백신 맞고 생각보다 괜찮은거 같아서 좀 앉아있었더니 머리아팠다.  일단 쉬고 주말에 더 공부하자.  
```

## 한주 마무리.
모델을 향상시키면서 이것저것 해볼 수 있는 일주일이었다.  
여태까지 중에 제일 일주일이 빨리갔다고 느낄정도로 재밌게 공부했다. 이래서 사람들이 컴페티션에 참여하는 가보다.  
이번주 아쉬웠던 점들을 주말동안 보충해서 다음주 팀에 많은 도움이 되었으면 한다.  


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


## 한주 마무리.
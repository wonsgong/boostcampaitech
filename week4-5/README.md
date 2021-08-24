
# [[Week 4-5] Image Classification ]
> 여기엔 매일매일의 간단한 내용과 느낌점을 두서없이 적어놓습니다.  
> 수업 필기는 `goodNotes` 앱을 활용해서 따로 폴더에서 확인.(수업 ppt는 가려둠.)  
> 피어세션 : https://drive.google.com/drive/folders/10awg6wJGwb6Xu-jHX5kLvl8_CmDx3b_0  
> 과제    : 개인 코랩에 올려놓는 중.  

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

## 한주 마무리.
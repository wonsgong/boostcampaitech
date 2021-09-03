
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

### Day20.  
> Image Classification : MTCNN 활용 모델 고도화.  
> Special Mission : 모듈화, Multi Classification 문제 정의.  
1. Image Classification  
	MTCNN 활용해서 얼굴 검출 후 crop 해서 학습 데이터로 활용.  
	Dataloader 에 추가한거라 모델에도 추가해서 추론 진행 예정.  
	베이스라인 코드처럼 모듈화를 해서 github 에 올려야겠다.  
2. Special Mission  
	모듈화는 현재 진행중이고, 문제에 대한 부분은 mask,age,gender 세 개를 따로 학습시킨 후,
	앙상블해서 추론을 진행해보려고 하는데 데이터의 불균형이 심해서 과적합이 많이 된다.  
	좀 더 균형을 맞춰서 다시 진행해봐야겠다.  
```
! 하루 마무리 : 이젠 방향을 정하고 결과를 내야 할 때이다. 문제정의를 다시 한번 생각하고 학습하자.  
```

### Day21.  
> Image Classification : MTCNN 활용 모델 고도화.  
> Special Mission : 모듈화, Multi Classification 문제 정의.  
1. Image Classification  
	MTCNN - Retinaface 로 face-crop loader 구현했다.  
	Retinaface 가 상당히 오래걸려 학습 시 시간이 오래걸린다.  -> 파일로 저장 후 재활용.  
	우리조의 베스트 모델을 디폴트로 학습을 시켜야겠다.  
	파일 저장 중 서버 연결이 끊겨서 재저장했는데 log를 남겨놨으면 끊긴 시점부터했을텐데 그러지 않아서 시간을 낭비했다.  
	항상 log를 남기는 습관을 들이자.  
```
! 하루 마무리 : 남은 이틀 좀 더 고민해서 성능을 올려보자.  
```

### Day22.  
> Image Classification : Face-crop 이미지 활용 학습, 모듈화.  
1. Image Classification  
	전날 저장한 face-crop 이미지를 활용해서 학습했다.  
	부족한 이미지 augment 적용해서 학습해보니까 성능 향상이 되었다.  
	우리 조의 베스트 모델을 좀 더 향상 시켜볼수 있을 것 같다.  
```
! 하루 마무리 : 모듈화를 하니 역시 학습 돌릴때 편하다.  
```

### Day23.  
> Image Classification : 팀 모델 고도화.    
1. Image Classification  
	`ray` 를 활용해서 파라미터 튜닝을 진행했다.  
	이해가 부족해서 고생을 하다가 잘 맞췄다. 다음엔 삽질 안하도록 baseline 화 해야겠다.  
	앙상블 모델을 만들어서 하니까 확실히 성능이 올랐다.  
	모여서 하니까 바로바로 피드백이 되서 좋았고, 결과도 좋게 나와서 마무리가 깔끔했다.  
```
! 하루 마무리 : 팀은 역시 모여서 하는게 소통과 피드백이 좋다.  마무리가 좋아서 만족스러운 대회였다. 코드와 리포트 정리 잘하자.  
```

### Day24.  
> Image Classification : 랩업 리포트, 코드 정리.  
1. Image Classification  
	코드 제출을 하기 위해 `ipynb` -> `py` 로 변환 작업.  
	주피터에서 코드를 짤 때도 모듈화를 고려하고 하면 좋을 것 같다.  
```
! 하루 마무리 : 블랙잭 팀과 마지막 날이었는데 리포트쓰느라 제대로 대화를 못해서 아쉽다.  
```
## 한주 마무리.
1주차.  
	모델을 향상시키면서 이것저것 해볼 수 있는 일주일이었다.  
	여태까지 중에 제일 일주일이 빨리갔다고 느낄정도로 재밌게 공부했다. 이래서 사람들이 컴페티션에 참여하는 가보다.  
	이번주 아쉬웠던 점들을 주말동안 보충해서 다음주 팀에 많은 도움이 되었으면 한다.  
2주차.  
	오프라인 모임을 통해서 협업을 하니까 확실히 효율도 좋고 즐겁게 했다.  
	좋은 팀원들과 재밌게 공부하고 결과까지 좋게 잘 나와서 기분 좋게 마무리 할 수 있었다.  
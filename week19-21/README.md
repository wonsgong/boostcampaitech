# [Week 19-21] Product Serving

> 여기엔 매일매일의 간단한 내용과 느낌점을 두서없이 적어놓습니다.  
> 수업 필기는 `goodNotes` 앱을 활용해서 따로 폴더에서 확인.(수업 ppt는 가려둠.)  
> 피어세션 : https://www.notion.so/BoostCamp-CV-5-5ec79e6fc8854e5b905f94314823c1ed  
> 과제    : 개인 코랩에 올려놓는 중.  

## Lecture
### Week19
----------------
### Day85
> Product Serving : MLOps 개론, Model Serving, ML Project life cycle  
> Final Project : 평가원 문제 크롭 및 bbox.  
1. Product Serving.
    `Product Serving` 에 대한 가장 기본적인 내용을 배웠다.  
    가장 기억에 남는 건 첫 competition 부터 지금까지 모든 마스터님들이 강조한 내용인 `문제 정의`다.  
    최종 프로젝트 진행할 때도 `life cycle` 을 고려해서 진행해야겠다.  
2. Final Project.
    평가원 문제 크롭을 간단하게 작업해서 빠르게 진행했었는 데,  
    좀 더 정확하고, 주관식 문제까지 가능하도록 진행했다.  
    이 데이터로 다시 학습 진행해야겠다.  
```
! 하루 마무리 : 빡코딩, 빡집중해서 프로젝트 잘해보자!
```

### Day86
> Product Serving : 프로토타이핑(Voila, Streamlit).  
> Final Project : 모델 학습.  
1. Product Serving.
    아주 간단하게 프로토타입을 만들 수 있는 라이브러리를 배웠다.  
    실습했을 땐 정말 적은 코스트로 적절한 결과물을 얻을 수 있었다.  
    뭔가를 디스플레이 해줘야 할 땐 이 라이브러리들을 먼저 고려해야겠다.  
2. Final Project.
    `Synthetic data` 로 학습하다보니 실제 데이터에서는 좋은 결과가 나오지 못했다.  
    `Slding Window` , `Augmentation` 을 이용해서 학습을 해보고, 또 더 해봐야겠다.  
```
! 하루 마무리 : 좋은 라이브러리를 알게 되어서 좋구만.  
```

### Day88
> Product Serving : Linux & Shell Command, Cloud, Github Action 이용한 CI/CD.  
> Final Project : 모델 학습 및 서빙.  
1. Product Serving.
    `Github Action` 을 이용해서 `CI/CD` 을 직접 실습해봤다.  
    `GCP` 에서 `streamlit` 을 이용해 웹을 띄우고, 코드 수정 후 자동 배포되도록 진행했다.  
    이쪽으로는 잘 알지 못했는 데 생각보다 재밌겠다는 생각과 함께 Test Code 를 어떻게 짜야할 지에 대한 생각이 들었다.  
    이것저것 직접 해보면서 감을 잡아봐야겠다.  
2. Final Project.
    모델 학습을 진행과 동시에 `GCP` 를 이용해서 서빙을 할 수 있을 지 확인해봤다.  
    최종 결과물에 대한 고민을 좀 더 하고 명확하게 정해야겠다.  
```
! 하루 마무리 : 모델에 집중 할 지, 결과물에 집중 할 지, 어렵다. 
```

### Week20
----------------
### Day90
> Product Serving : FastAPI.  
> Final Project : dataloader refactoring, 모델 학습.  
1. Product Serving.
    `FastAPI` 의 기본 사용법과 함께 백엔드에 대한 기초적인 부분을 알 수 있었다.  
    `flask`,`Django` 를 가볍게 사용해봤었는 데 이게 좀 더 간단하고 직관적인 느낌이었다.  
    `swagger` 를 자동으로 해주는 것도 좋았다. 최종 프로젝트가 끝나고 좀 더 공부해봐야겠다.  
2. Final Project.
    알고보니 오류투성이던 `dataloader` 를 고치고, 좀 더 이해하기 싶고, 좋은 구조로 고쳤다.  
    이를 이용해서 `AttentionGAN` 을 학습 중인데 해당 내용은 좀 더 공부해봐야겠다.  
```
! 하루 마무리 : 남은 2주동안 열심히 달려봅시다.  
```

### Day92
> Product Serving : Docker.  
> Final Project : segmentation model 학습.  
1. Product Serving.
    `Docker` 의 기본 사용법에 대해서 공부했다.  
    자주 이미지를 만들고 배포해봐야 익숙해질 것 같다.  
2. Final Project.
    현재 결과가 좋은 segmentation model 학습으로 역할을 맡고 진행중이다.  
    학습 시에 background 에 다르게 handwriting 이 그려질 수 있게 수정해서 학습했다.  
    실제 데이터에도 잘 될 수 있게 다양한 augment 를 고민해봐야겠다.  
```
! 하루 마무리 : .
```

### Day93
> Product Serving : logging, MLFlow.  
> Final Project : 데이터 제작 및 segmentation 학습.  
1. Product Serving.
    수업을 들을수록 모델 학습하는데 있어서 불편했던 것들을 하나씩 해결하는 법을 배우는 것 같다.  
    실습을 제대로 해보지 못하고 있는 데 꼭 따라서 해봐야겠다.  
2. Final Project.
    모델 결과분석을 통해서 데이터를 추가 제작해서 학습을 진행중이다.  
    역시 실제 데이터에 잘 되도록 하는게 어렵다.  
    더 잘해봐야겠다.  
```
! 하루 마무리 : 고민해보자 어떻게 하면 좋을지!
```

### Day94
> Product Serving : BentoML.  
> Final Project : segmentation 학습.  
1. Product Serving.
    이번 수업 내용도 개념과 뭘 하고자 했는 지에 대한 이해만 하고,  
    실습은 잠시 뒤로 미뤄놨다.  
    어떻게 하면 더 효율적으로 할 수 있을 지를 항상 고민해야하는 것 같다.  
2. Final Project.
    `sliding window` 방식으로 inference 을 할 때, 실제 이미지를 2배로 확대해서 하는 게  
    더 좋은 결과를 보여주고 있다. 글씨 픽셀이 작다보니까 키운게 좋은 결과로 이어진 것 같다.  
    남은 주말동안 더 집중해서 해야겠다.  
```
! 하루 마무리 : 막판 스퍼트!
```

## Week 19 마무리.
해야할 것들(강의,최종프로젝트,면접)이 많아서 바쁘고 피곤한 한주였다.  
시간 관리를 잘해서 균형있게 진행해야겠다.  

## Week 20 마무리.
최종 프로젝트의 결과물이 어느정도 모습이 보이고 있어서 뿌듯한 느낌이다.  
어떤 문제를 만났고, 어떻게 해결했고, 왜 그렇게 했는 지에 대한 물음과 답을 잘 정리해서 발표해야겠다.  
남은 한 주동안 우리의 결과물을 잘 포장해서 우리가 만족하는 결과물을 얻을 수 있도록 노력해야겠다.  


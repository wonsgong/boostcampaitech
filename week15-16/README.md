# [Week 15-16] Data Annotation

> 여기엔 매일매일의 간단한 내용과 느낌점을 두서없이 적어놓습니다.  
> 수업 필기는 `goodNotes` 앱을 활용해서 따로 폴더에서 확인.(수업 ppt는 가려둠.)  
> 피어세션 : https://www.notion.so/BoostCamp-CV-5-5ec79e6fc8854e5b905f94314823c1ed
> 과제    : 개인 코랩에 올려놓는 중.  

## Lecture
### Week15
----------------
### Day65
> Data Annotation : 데이터 제작의 중요성 1,2.  
1. Data Annotation.
    Data 관점에서 왜 데이터가 중요한지 배울 수 있었던 강의였다.  
    이번에 진행될 대회도 데이터를 얼마나 잘 가공하느냐가 중점인 만큼 집중해서 들었다.  
    이후 제공된 `annotation tool` 을 이용해 annotation 을 진행해봤다.  
    확실히 비용이 많이 들겠다는 점과 명확한 가이드가 정말 중요하다는 것을 느꼈다.  
```
! 하루 마무리 : 이력서를 써야하는 시기가 와버렸다.
```

### Day66
> Data Annotation : 데이터 소개, annotation guide, tool.  
1. Data Annotation.
    `OCR` task 를 위한 데이터셋에 대한 소개를 들었고, 제공된 가이드와 툴을 활용해 라벨링 작업을 진행했다.  
    가이드가 있음에도 내 의도가 어느정도는 반영이 되는구나 라는 걸 느끼고 그만큼 가이드의 중요성을 다시 한번 느꼈다.  
    데이터셋 EDA를 진행하면서 python 내에서 한글을 이미지에 적는 방법을 배울 수 있었다.  
    오늘 멘토링에서 팩폭을 많이 맞았다... 뭐라도 하나 배우고 잠드는 매일매일이 되면 좋겠다.   
```
! 하루 마무리 : 천천히, 꾸준히, 제대로, 열심히.
```

### Day67
> Data Annotation : OCR Technology & Service, Text Detection, 성능평가방식.  
1. Data Annotation.
    `OCR` 이 어떤 방식으로 동작하는 지, 내부 동작과 실제 어떤 서비스에서 이용하는 지 알 수 있었던 강의였다.  
    대회에서 진행될 베이스모델 이해와 성능 평가를 어떻게 하는 지도 알 수 있었다.  
    우리가 사용하는 task에 필요한 성능 평가 방식이 무엇인지 제대로 알고 써야겠다는 걸 느꼈다.  
    내일부터 대회 진행되는데 코드 이해와 베이스라인을 좀 더 보강해서 진행해야겠다.  
```
! 하루 마무리 : 리프레쉬가 필요한 걸까 그냥 나약한걸까
```

### Day68
> Data Annotation : convert ufo, baseline.  
1. Data Annotation.
    직접 라벨링한 데이터를 검수하고 학습에 이용할 ufo 포맷으로 변경했다.  
    변경 과정에서 polygon 형태의 annotation 을 모델(EAST)에 적용할 수 있을 지 고민했다.  
    우선은 이미지 중 하나라도 polygon 형태가 존재할 시 학습 이미지로 활용하지 않고 진행하고 있다.  
    polygon 형태의 단어를 masking 해서 학습에 활용하는 방법도 생각중이다.  
    데이터를 잘 가공해야하는 대회임으로 좀 더 고민하고 적용해보자.  
```
! 하루 마무리 : 데이터를 뜯어보자!
```

### Day69
> Data Annotation : polygon masking, pil issue.  
1. Data Annotation.
    `polygon` annotation 이 존재하는 이미지를 학습 이미지에서 제외했는데,  
    이번엔 영역을 검정색으로 마스킹해서 사용했다.  
    `train/valid` 에 경우도 현재 `random split(8:2)` 로 사용중인데 주말동안 EDA 하면서  
    잘 나눠보자.(새로 추가된 데이터도 같이!).  
    pil 에 경우 `exif` 에 `orientation` 정보를 통해서 자동으로 이미지를 열 때 방향을 바꾸게 된다.  
    이럴 경우 annotation 정보와 다르게 적용되기 때문에 `opencv` 를 활용해서 이미지를 읽어왔다.(해당 내용은 대회 repo에 issue 에 정리)  
```
! 하루 마무리 : 데이터 자체의 중요성을 더욱 느끼고 알아가는 중이다.  
```

### Week16
----------------
### Day70
> Data Annotation : Advanced text detection models, Bag of tricks.  
1. Data Annotation.
    `Text Detection model` 의 SOTA 모델들의 구조와 컨셉에 대해 공부했다.  
    이번 대회에서는 사용하지 못하지만, 이후 OCR task 를 할 때 해당 내용을 복습하고 진행해야겠다.  
    `Synthetic Data` 에 경우 이번 대회에 충분히 적용해볼만한 트릭이라서 진행해보려고 한다.  
    강의에서 배운 내용들을 가지고 직접 적용해보고 테스트하며 대회를 잘 마무리해봐야겠다.  

```
! 하루 마무리 : 어쩜 이렇게 세상엔 배울게 많을까?
```

### Day71
> Data Annotation : data preprocessing
1. Data Annotation.
    데이터 추가 이후 학습이 오히려 잘 되지않아서 재검수 후 진행했다.  
    평가 task 가 한글과 영어 검출로 되어있어서 해당 언어만 학습하면 더 좋을 것이라는 아이디어로  
    `language tag` 가 `ko`,`en` 인 경우를 제외하고는 `illegibility` 세팅을 해줬다.  
    학습 마무리된 결과 보고 분석해서 재진행해야겠다.  
```
! 하루 마무리 : 데이터 처리 파이프라인이 중요하는걸 느끼고있다.
```

### Day72
> Data Annotation : data preprocessing
1. Data Annotation.
    한글과 영어로만 학습한 결과가 리더보드 상에서 더 좋은 결과를 보이는 것을 확인했다.  
    이를 이용해서 마무리 학습을 진행하고 있다.  
    이번 대회보다는 최종 프로젝트 주제 선정에 좀 더 신경을 많이 쓴 하루였다.  
    재밌고, 의미있는 주제를 잘 골라서 좋은 마무리를 했으면 좋겠다.  
```
! 하루 마무리 : 어렵다 어려워
```

## Week 16 마무리.
정말 데이터에만 집중을 했던 일주일이었다.  
어떻게 하면 데이터를 더 잘 가공해서 학습이 잘 될지 고민했고, 적용해볼 수 있었다.  
이번주는 추가된 데이터를 정제하는 방법으로 성능을 올렸다면,  
다음주는 좀 더 면밀하게 train/valid split 을 진행해서 학습의 현황을 확인 할 수 있게해야겠다.  
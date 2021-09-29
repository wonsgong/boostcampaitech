# [[Week 9] Object Detection](./week9)

> 여기엔 매일매일의 간단한 내용과 느낌점을 두서없이 적어놓습니다.  
> 수업 필기는 `goodNotes` 앱을 활용해서 따로 폴더에서 확인.(수업 ppt는 가려둠.)  
> 피어세션 : https://www.notion.so/BoostCamp-CV-5-5ec79e6fc8854e5b905f94314823c1ed
> 과제    : 개인 코랩에 올려놓는 중.  

## Lecture
### Day37  
> Object Detection : Object Detection Overview, 2 Stage Detectors.  
1. Object Detection.  
    졸업 프로젝트 일정으로 인해서 강의를 우선 들었다.  
    기존에 배웠던 내용을 좀 더 자세하고 깊게 알려주는 느낌이었고, 복습이다 보니 좀 더 이해가 잘되었다.  
    이후에 베이스라인으로 제공된 코드, 데이터셋을 확인했다.  
    나머지 강의를 우선적으로 들으면서 EDA와 베이스라인 코드를 구축해봐야겠다.  

```
! 하루 마무리 : 졸업 가능할듯!
```

### Day38   
> Object Detection : Object Detection Library, Neck.  
> Special Mission : mAP metric, Faster RCNN, Baseline.  
1. Object Detection.  
    `MMDetection` 위주로 많이 실습을 해봤다.  
    마스터님 이야기처럼 명확하게 이해하고 쓰기 위해 이것저것 변경해보면서 테스트해봤다.  
    이것저것 테스트 해보면서 느낀 건 확실히 `mAP_s` 이 정말 안나온다는 것이었다.  
    `Neck` 에서 배운 여러가지 모델들을 고민해보고 적용해봐야겠다.  
2. Special Mission.  
    `mAP` 를 구현해보는 것에 그치지 않고 무엇을 의미하는 지 좀 더 공부해봤다.  
    `torchvision` , `MMDetection` 에서 제공하는 `Faster RCNN` 으로 학습과 추론을 진행했다.  
    강의를 우선적으로 듣기 위해서 `Challenge` 는 아직 도전하지 않았다.  
```
! 하루 마무리 : EDA 를 좀 더 해보고 모델를 구현하자.  
```


### Day39    
> Object Detection : 1 Stage Detection, EfficientDet.  
> Special Mission : YOLO v1, EfficientDet.  
1. Object Detection.  
    이론적인 내용은 스무스하게 이해하고 넘어갔다.  
    피어세션에서 공유했던 내용을 토대로 좀 더 잘 이해할 수 있었다.  
    큰 흐름을 가지고서 수업을 해주시다 보니까 발전 흐름을 이해할 수 있었다.  
2. Special Mission.  
    주어진 `EfficientDet` 코드를 활용해서 학습을 할 수 있도록 하고 있다.  
    직접 구현되어 있는 `mAP`와 `nms` 코드를 확인해보면서 완성하고 있다.   
    오늘 중으로 최대한 돌려볼 수 있도록 코드를 구현하고 있다.  
```
! 하루 마무리 : 다음주가 본격 시작이라 생각하고 기틀을 다지자.
```

## Week 9 마무리.
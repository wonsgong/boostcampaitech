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

### Day40    
> Object Detection : EDA, EfficientDet 
1. Object Detection.  
    계속해서 해왔던 EDA 를 좀 더 진행했다.  
    통계치나 분포에 대해서는 생각보다 잘 정리된 데이터였다.  
    `EfficientDet` 코드를 활용해서 학습을 진행했는 데 생각보다 결과가 나오지 않아서  
    어떻게 개선해야 할 지 고민이다.  

```
! 하루 마무리 : mmdetection 으로 갈아타야할까...
```

### Day41
> Object Detection : 데이터 라벨링 검수, wandb 연동, EfficientDet.  
1. Object Detection.  
    실제 데이터를 보니까 과도하게 작거나, 조금은 모호한 라벨링이 존재했다.  
    우선을 그대로 진행하되, 좀 더 고민해보고 해결방법을 찾아야겠다.  
    `wandb` 팀을 만들어서 팀원들과 활용하니까 훨씬 좋다.  
    더 열심히해야겠다는 느낌이 많이 든다.  
    EfficientDet 은 주말까지 해보고 안되면 갈아타야겠다.  

```
! 하루 마무리 : 삽질을 하면서 배우는 거 맞겠지...
```

### Day42
> Object Detection : Advanced Object Detection 1, Advanced Object Detection 2.  
1. Object Detection.  
    강의에서 설명해주신 기법들을 적용해보면서 하루를 보냈다.  
    그냥 좋아서 쓰기보다는 왜 좋을 지 고민하고 사용하자.  
    `1-stage detector` 와 `2-stage detector` 같이 학습을 했는데,  
    내일 배울 앙상블 할 때 좋을 것 같다.  
    `vfnet` 을 좀 더 공부하자.   
```
! 하루 마무리 : vfnet 더 파보자!
```

### Day43
> Object Detection : Ready for Competition, Review Top Solution in Kaggle.  
1. Object Detection.  
    강의에서 소개한 `MultilabelStratifiedKFold` 를 토대로 valid set을 확인해봤다.  
    간단하게 `클래스 별 bbox` 를 기준으로 나눴어서 `클래스 별 bbox size` 를 확인했다.  
    `Object Detection` 이나 `Segmentaion` 에선 항상 `bbox` 나 `mask` 정보가 중요하다는 것을 잊지말자.  
    `vfnet` 모델은 어느정도 성능이 나왔으니까 다른 모델을 가지고 테스트를 진행해야겠다.  
```
! 하루 마무리 : 슬슬 성능을 뽑아내야 할 시점이 온 것 같다.  
```

### Day44
> Object Detection : TTA, augment, yolov5
1. Object Detection.  
    3 scale 과 flip tta 를 적용하니까 0.1 정도 올랐다. tta 에 대해서 좀 더 고민해봐야겠다.  
    쓰레기별 색상이 다양하다는 점에서 그레이스케일로 변환해봤는 데 오히려 떨어지는 경향을 보였다.  
    쓰레기의 일부 카테고리(like 스티로폼)은 오히려 색이 고정되어 있어서 그런 것 같다.  
    Yolov5 에서 format 을 변경하는 방법을 오피스아워에서 듣고, 바로 적용해봤는데  
    학습속도도 빠르고 성능도 나름 잘 나와줘서 좀 더 공부해서 성능을 올려봐야겠다.   
```
! 하루 마무리 : 나름 어느정도의 결과를 낼 수 있었던 하루였다.  
```

### Day45
> Object Detection : 오프라인 모임, ensemble, yolov5, augment.  
1. Object Detection.  
    팀원들과 만나서 같이 하니까 확실히 다양한 접근법을 제시할 수 있었다.  
    모델이 `localization` 은 잘하지만, `classification` 을 못하는 걸 보고  
    backbone 자체를 학습 시켜보자는 접근이 좋았다.  
    `vfnet` 과 `yolo` 의 앙상블의 성능이 오르는 것을 보니  
    `2-stage detector` 도 잘 학습시켜서 같이 앙상블 해봐야 겠다.  
    연휴 간에 데이터를 좀 더 들여다보고 모델을 고도화 해야겠다.  
```
! 하루 마무리 : 우리 깐부하자.  
```

### Day46
> Object Detection : mosaic, general_trash eda.  
1. Object Detection.  
    일반쓰레기를 잘 못잡고 있어서 데이터를 다시 보면서 방법을 찾아봤다.  
    `IoU50` 이상을 지워보기도 하고, 일정 크기를 기준으로 분류도 해봤지만 크게 나아지지 못했다.  
    9가지 분류 이외에 쓰레기가 일반쓰레기라고 생각을 하고 있어서 이걸 어떻게 모델에 녹여낼지 고민이다. 어렵다.  
    `mosaic` 코드를 만들어서 학습을 진행하고 있다.  
    이제 이틀남았는 데 모델이 무겁다보니 두 개정도 완성시킬 수 있을 것 같다.  
    마지막까지 좀 더 성능을 올리기위해 할 수 있는 노력을 해보자.  
```
! 하루 마무리 : 일반쓰레기의 정의가 뭘까.
```

### Day47
> Object Detection : 멘토링, mosaic.  
1. Object Detection.  
    멘토링에서 나눈 철학적 질문들을 곰곰히 생각해본 하루였다.  
    사실 결론을 내진 못했지만, 부스트캠프를 하게 된 이유와 얻고자 하는 걸 한번 더 리마인드 할 수 있었다.  
    `mosaic` 방법에 경우 따로 구현해서 이미지를 저장해 진행했었는 데,  
    `MMdetection` 에서 `config` 수정으로 가능하도록 변경했다.   
    최종 모델을 위해 모든 학습 데이터를 활용해서 학습을 진행했는 데 역시나 오래걸린다.  
```
! 하루 마무리 : 사실상 대회 마지막 날인듯  
```

### Day48
> Object Detection : ensemble.  
1. Object Detection.  
    최종 모델들을 가지고 앙상블 해서 대회를 마무리했다.  
    더 큰 모델, 큰 해상도를 해주는 게 데이터 만지는 것보다 좋게 나와서 솔직히 조금 허무하다.  
    내가 데이터 전처리를 잘못한 것이겠지만.  
    어찌되었건 대회는 끝났고, 이제 다음주 `segmentation` 대회를 들어가기 전에  
    대회를 돌아보며 부족했던 것과 좋았던 것을 잘 정리해서 다음 대회에 적용하자.  
```
! 하루 마무리 : 3주간 삽질을 내껄로 만들기 위한 정리를 하자.  
```
## Week 9 마무리.
`Object Detection` task 를 처음해보다 보니까 초반 접근이 어려웠다.  
`MMDetection` 라이브러리를 활용하면 쉽게 할 수 있었겠지만,  
`EfficientDet` 으로 학습시켜보려고 하다 보니 삽질을 많이 했던 것 같다.  
주말까지 해보고 안되면 다른 모델로 갈아타야겠다.  
3일동안 쉬는 데 마냥 쉬지말고 대회생각을 해야겠다.  

## Week 10 마무리.
2주차로 들어서면서 점차 감을 잡아갔다.  
어떤걸 고쳐줘야 효과가 있을 지와 좋은 성적을 내기 위해서 해결해야 할  
task 를 명확하게 이해할 수 있었던 한 주였다.  
이번 연휴도 잘 쉬면서 공부하자...!  
그리고 파일과 결과 정리를 미리 해놓자...

# [[Week 3] Pytorch / Data Visualization ]
> 여기엔 매일매일의 간단한 내용과 느낌점을 두서없이 적어놓습니다.  
> 수업 필기는 `goodNotes` 앱을 활용해서 따로 폴더에서 확인.(수업 ppt는 가려둠.)  
> 피어세션 : https://drive.google.com/drive/folders/10awg6wJGwb6Xu-jHX5kLvl8_CmDx3b_0  
> 과제    : 개인 코랩에 올려놓는 중.  

## Lecture
### Day11.  
> Pytorch : Introduction to PyTorch , PyTorch Basics , PyTorch 프로젝트 구조 이해하기.  
> 과제 : Custom Model 개발하기.  
1. Pytorch   
	파이토치를 써봤기 때문에 1강,2강은 어렵지 않게 공부했다.  
	AutoGrad 지원을 그냥 알고만 있었는 데 튜토리얼보면서 더 공부할 수 있었다.  
	3강인 구조에 대해서는 그렇게 프로젝트를 해보진 못했어서 낯설었다. 작은 프로젝트에서도 저렇게 구조를 짜서 해봐야겠다.  
2. 과제  
	과제의 1부 격인 `Document` 까지 완료했다.  
	`torch.gather` 가 3차원이 되니까 상당히 헷갈렸다.  
```
! 하루 마무리 : pytorch 에 대한 첫날이었다 보니 크게 어렵지 않게 수업을 들었다.  남은 과제도 내일 다 끝내야겠다!
```

### Day12.  
> Pytorch : AutoGrad & Optimizer , Dataset & Dataloader.  
> Data Visualization : Text 사용하기.  
> 과제 : Custom Model 개발하기, Custom Dataset 과제.  
1. Pytorch  
	기본적인 구조에 대한 강의다 보니까 완벽하게 이해하기 보다는 구조와 흐름을 이해하려고 노력했다.  
	AutoGrad 의 경우 제공되는 기능으로서 알고만 넘어갔는데 어떻게 작동하는 지에 대한 내용을 공부할 수 있어서 좋았다.  
2. Data Visualization  
	시각화에서 text를 쓰는 경우는 제목과 x,y label을 표기할 때나 기본제공하는 annot=True 를 썼었는 데 생각보다 유용하게 쓸 수 있다는 걸 느꼈다.  
3. 과제  
	Custom Model 의 필수 부분은 완료했다.  
	🔥 푸느라 Custom Dataset 은 아직 시작 못했다.  
	Custom Dataset 과제 먼제 완료하고 🔥 풀어야겠다.  
```
! 하루 마무리 : 프레임워크 공식 API 를 보고 공부했었는 데 이번 기회에 공식문서를 잘 활용하는 게 중요한 걸 더욱 느꼈다.  
```

### Day13.  
> Pytorch : 모델 불러오기, Monitoring tools for PyTorch.  
> Data Visualization : Color/Facet 사용하기, More Tips.  
> 과제 : Custom Dataset 과제.  
1. Pytorch  
	인턴하면서 전이 학습을 많이 공부했었어서 크게 어려움 없이 학습했다.  
	`Tensorboard` 만 써봤는 데 `Weight and Biases`가 프로젝트 단위에 기록도 가능한게 좋아서 갈아탈 예정이다.  
2. Data Visualization  
	Color,Facet 에 대한 내용은 종종 쓰던 거에 좀 더 전문적인 내용이 추가된 거라 어렵지 않았는데.  
	More Tips 는 개념만 알고 넘어간듯하다.  
	키워드로 기억하고 시각화 시에 찾아가며 해야겠다.  
3. 과제  
	데이터셋 과제는 크게 어렵지 않게 할 수 있었다.  
	다만 `csv` 파일에서 쓸 수 있게 전처리하는 과정이 생각보다 까다로웠다.  
```
! 하루 마무리 : 볼 땐 이쁘게만 봤는데 코드로 그리는건 생각보다 어려웠다.  자주 그려보자.  
```

### Day14.  
> Pytorch : Multi-GPU 학습, Hyperparameter Tuning, PyTorch Troubleshooting.  
> 과제 : Transfer Learning + Parameter Tuning.  
1. Pytorch  
	`Multi-GPU` 환경을 느낌만 알고있었는 데 이론적인 부분을 학습할 수 있어서 좋았다.  
	강의에서 소개해준 에러를 전부 보고 삽질을 해봤던 것들이라 소름돋았다.  
	진작 알았으면 참 좋았을 것 같은데 이후 발생하면 꼭 기억해서 잘 고쳐나가야겠다.  
2. 과제  
	Transfer Learning 까지만 풀었다.  
	주말에 뒷 내용을 더 해보고 오피스 아워에서 들은 해설과 비교하며 공부해야겠다.  
```
! 하루 마무리 : 고기도 먹어본 놈이 잘먹는다고 삽질도 해본 사람이 잘한다...
```

## 한주 마무리.
과제의 양이 많아서 추가적인 부분은 하지 못했다. 주말에 추가적인 부분 풀어봐야겠다.  
드디어 첫번째 U-Stage 가 끝났다. 실제 데이터를 다루는 P-Stage 를 기대하고 열심히 준비해서 잘 따라가야겠다.  
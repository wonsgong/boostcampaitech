
# Naver BoostCamp AI Tech
> Naver BoostCamp AI tech 과정을 기록하는 공간.  
> 주차별 주제의 키워드와 수업 필기, 하루 회고를 기록하고 있습니다.:blush:  

## U stage
### [Week 1] Python_Basics_for_AI / AI_Math [[docs]](./week01)
- Python_Basics_for_AI : 기초 문법 / OOP / 데이터 다루기 / numpy / pandas.  
- AI Math : 벡터 / 행렬 / 경사 하강법 / 딥러닝 학습법 / 확률론 기초 / 통계학 기초 / CNN 기초 / RNN 기초.  
### [Week 2] DL Basic / Data Visualization [[docs]](./week02)
- DL Basic : MLP / Optimizer / CNN / CV Application / RNN / Transformer / Generative Model.  
- Data Visualization : 시각화 요소 / Matplotlib / barplot / lineplot / scatterplot.  
### [Week 3] Pytorch / Data Visualization [[docs]](./week03)
- Pytorch : Basic / AutoGrad / Optimizer / Dataset / Dataloader / Monitoring tools / Multi-GPU / Hyperparmeter tuning / Troubleshooting.  
- Data Visualization : Text / Color / Facet / Tips.  
### [Week 6-7] CV / Data Visualization [[docs]](./week06-7)
- CV : Image Classification / Self-Learning / Semantic Segmentation / Object Detection / CNN Visualization / AutoGrad / Instance,Panoptic Segmentation / Landmark Localization / Conditional Generative Model / Multi-model Learning / Image Captioning / 3D_Understaning.  
- Data Visualization : Polar Coordinate / Pie Charts / Library / Interactive Visualization / Custom Matplotlib Theme.  
### [Week 8] Special lecture [[docs]](./week08)
- 주제 : 서비스향 AI 모델 개발하기 / 캐글 그랜드마스터의 경진대회 노하우 대방출 / AI+ML 과 Quant trading / 내가 만든 AI모델은 합법일까, 불법일까 / Full-Stack ML Engineer / AI & Ethics / AI시대에 커리어 빌딩 / 자연어처리를 위한 언어 모델의 학습과 평가.  

## P stage
### [Week 4-5] Image Classification [[docs]](./week04-5) [[code]](https://github.com/wonsgong/image-classification-level1-21)
- 사람 얼굴 이미지의 마스크 착용 여부, 나이 및 성별를 분류하는 Task.
- 데이터 : 남여(20-70대) 4,500명. 1명 당 7장(마스크 착용 5장, 오착용 1장, 미착용1장) 의 이미지.
- 결과 : F1 Score, public LB(9등) :  0.770-> private LB(7등) : 0.763.

### [Week 9-11] Object Detection [[docs]](./week09-11) [[code]](https://github.com/wonsgong/object-detection-level2-cv-05)
- 일상에서 발생하는 10가지 종류의 쓰레기 객체를 검출하는 Task.  
- 데이터 : 일반쓰레기, 종이, 종이팩, 철, 유리, 플라스틱, 스티로폼, 비닐, 배터리, 의류 총 10종류 별로 bounding box 와 category 가 라벨링된 4883장 이미지.  
- 결과 : mAP, public LB(9등) :  0.674 -> private LB(8등) : 0.661.  

### [Week 12-14] Semantic Segmentation [[docs]](./week12-14) [[code]](https://github.com/wonsgong/semantic-segmentation-level2-cv-05)
- 일상에서 발생하는 10가지 종류의 쓰레기 객체를 검출하는 Task.  
- 데이터 : 일반쓰레기, 종이, 종이팩, 철, 유리, 플라스틱, 스티로폼, 비닐, 배터리, 의류 총 10종류 별로 masking 정보를 담고 있는 json 파일과 2647장 이미지.  
- 결과 : mIoU, public LB(5등) :  0.780 -> private LB(2등) : 0.766.  

### [Week 15-16] Data Annotation [[docs]](./week15-16) [[code]](https://github.com/wonsgong/data-annotation-cv-level3-cv-05)
- OCR 모델을 데이터 처리에만 집중해서 성능을 높이는 Task.  
- 데이터 : 직접 Annotation 한 scene text(한글, 영어) 의 정보를 담고 있는 json 파일과 1858 이미지.   
- 결과 : f1, public LB(3등) : 0.678 -> private LB(1등) : 0.691.
### [Week 17-18] Model Optimization [[docs]](./week17-18)

### [Week 19-21] Product Serving [[docs]](./week19-21)

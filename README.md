# toy_project-SGDClassifier

# 1. 개발목적
SGDClassifier을 공부한 후 이를 구현해보기 위한 학습목적으로 개발함.

# 2. 설명
데이터는 케글의 water_Potability.csv 파일을 가져와 사용하였음.
pH value, Hardness, Solids, Chloramines, Sulfate, Conductivity, Organic_carbon, Trihalomethanes, Turbidity이라는 물의 특성을 사용해 마실 수 있는 물인지 아닌지 분류해내는 모델을 확률적 경사하강법으로 개발함. 


# 3. 개발일지
2021/07/24 NaN값은 평균값으로 넣어주고 데이터는 표준점수로 전처리한 후 훈련을 했는데 이를 시각화 해본 결과 많이 낮은 정확도를 보임.

2021/07/25 정확도를 높이기 위해 PolynomialFeatures 메소드를 사용하여 degree를 조절하며 정확도를 높이고자했지만 max_test_score = 0.6을 보여줬고, 확률적 경사하강법 모델에 맞지 않는 데이터라고 생각하여 특성이 많을 수록 성능이 좋아지는 선형방정식을 따르는 로지스틱 회귀를 통해 구현해보았지만 train_score = 0.7, test_score = 0.67을 보여주었음. 결과적으로 Potability의 클래스를 분류하기 위한 나머지 특성이 서로 선형적인 관계가 아닐 수 있다는 판단을 함. 하지만 이 부분에 있어서는 데이터 분석에서 공부할 예정임. 

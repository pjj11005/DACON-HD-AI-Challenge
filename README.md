# DACON-HD-AI-Challenge


## 대회 요약
[https://dacon.io/competitions/official/236158/overview/description]

- 주최: HD한국조선해양 AI Center
- 운영: 데이콘
- 상금: 총 2000만원
- 주제: 항만 內 선박 대기 시간 예측을 위한 선박 항차 데이터 분석 AI 알고리즘 개발
- 평가 산식 : MAE (Mean Absolute Error, 평균 절대 오차) 
- 기간: 2023.09.25 ~ 2023.10.30
- 팀 구성: 진깃, 광운인(본인) -2인

코로나19로 인한 물류 지연 문제와 해운 물류 분야의 항만 정체 문제가 화두가 되고있다. 이를 해결하기 위해 조선해양 분야 데이터를 활용하여 선박 대기 시간을 예측하는 AI 알고리즘을 개발하는 대회이다. 

데이터는 2012년부터 2022년까지의 약 10년치 정보이다. 데이터에 민감한 정보들이 많이 포함되어있어 한번 데이터셋의 크기 및 피쳐가 삭제되는 고비가 있었다. 베이스라인을 따라 전처리 및 LGBM 모델을 기반으로 feature selection을 진행 하는 것이 기본적으로 높은 성능을 보였다. 

이후, 중요도 높은 feature들을 PCA변환, 종속변수 로그화, 스케일링하여 학습에 용이하게 했다. 모델은 LGBM의 성능이 가장 좋게 나와 이것을 모델로 채택했다. 최종적으로 하이퍼 파라미터 최적화와 교차검증으로 성능을 향상 시켰다.

결론적으로 feature engineering, feature selection등의 처리가 중요했고 교차검증 및 하이퍼 파라미터 최적화가 중요했다. 

## 대회 결과

| Submission | CV MAE | Public MAE | Rank | Private MAE | Rank |
| --- | --- | --- | --- | --- | --- |
| 진깃 solution | - | 44.11155 | 64 / 349| 44.018 | 57 /330|
| 광운인 solution | 37.8968 | 44.2716 | - | - | - |
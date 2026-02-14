# Deep-Learning

## Modeling for Flood Prediction: From Classical ML to Tabular Transformers
### 홍수 예측을 위한 다양한 머신러닝 및 딥러닝 접근법을 비교 분석한 연구 프로젝트
**AutoGluon** 프레임워크와 **SAINT(Tabular Transformer)** 모델을 활용하여 정형 데이터 환경에서의 최적의 예측 성능을 탐구했습니다.

## 연구 배경 (Research Background)
홍수 예측은 환경 데이터의 복잡성과 비선형성으로 인해 정확한 모델링이 까다로운 영역입니다. 본 연구는 단순 회귀부터 최신 딥러닝 모델인 SAINT까지 폭넓게 적용하여, **"어떤 모델이 실무 환경에서 가장 강건(Robust)한 성능을 보이는가?"**에 대한 답을 찾고자 수행

## 주요 수행 내용 (Key Contributions)
- 다각적 전처리: 데이터 정규화(Normalization) 및 PCA 기반 차원 축소가 모델 성능에 미치는 영향을 시나리오별로 대조 실험
- 불균형 데이터 대응: 실무 환경의 데이터 특성을 반영한 리샘플링 및 가중치 조정 실험

🧠 모델링 전략 (Modeling Strategy)
Classical ML: XGBoost, CatBoost, LightGBM 등 트리 기반 앙상블 모델 활용.

State-of-the-art DL: * SAINT: Row Attention과 Intersample Attention을 활용하여 피처 간 관계 모델링.

TabPFN: Prior-Data Fitted Network를 통한 신속한 정형 데이터 추론.

AutoML & Ensemble: AutoGluon을 활용하여 모델을 자동 탐색하고, 최종적으로 Voting Ensemble을 통해 개별 모델의 편향을 제거.

### 기술 스택 (Tech Stack)
Environment: Python 3.10, Jupyter Notebook

Deep Learning: PyTorch, AutoGluon.Tabular

ML Libraries: Scikit-learn, XGBoost, CatBoost

Analysis: Pandas, NumPy, Matplotlib, Seaborn

### 핵심 결과 및 인사이트 (Key Insights)
앙상블의 우위: 단일 모델보다 여러 알고리즘을 결합한 Voting Ensemble이 가장 안정적이고 높은 $R^2$ 스코어를 기록함.
딥러닝의 가능성과 한계: SAINT와 같은 Transformer 기반 모델이 정형 데이터의 복잡한 상관관계를 파악하는 데 유용함을 확인했으나, 데이터의 스케일과 특성에 따라 학습 안정성(Training Stability) 확보가 핵심 과제임을 도출함.

### 관련 논문 (Publication)
논문명: Modeling for Flood Prediction: Diverse Applications and Evaluation of Machine Learning and Deep Learning Approaches

학술지: 데이터과학연구(Journal of Data Science), 제13권, pp.15-39, 2024.


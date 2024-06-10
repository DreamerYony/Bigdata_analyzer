## 🍳 분류 과제 실기 자료
### 🍳 주의
- 분류 과제의 경우에는 prediction인지 prediction_proba인지, 평가 지표는 무엇인지를 잘 확인해야 합니다.
- 예측 확률값을 구하는 문제라면 prediction_proba를 사용하고 평가 지표로는 ROC-AUC가 사용됩니다.
- 예측값(0 또는 1)을 구하는 문제라면 평가 지표로는 accuracy, macro f1 score가 사용됩니다.
- 이러한 평가지표는 sklearn.metrics에서 accuracy_score, f1_score, roc_auc_score를 임포트하여 사용하면 됩니다.
### 🍳 포함된 파일
- Mobile_Price(Classification).ipynb : original version. 모바일 폰의 가격 범위를 예측합니다. 예측값을 확률로 계산하기 위해 proba를 사용하고, 평가 지표로는 rou_auc_score를 사용합니다.
- Mobile_Price(simple_version).ipynb : simple version. 일부 단계는 생략합니다.
- Star_size(simple_version).ipynb : 별의 크기를 예측합니다. simple version으로 일부 단계는 생략합니다. 예측값을 계산하기 위해 predict를 사용하고, 평가 지표로는 f1 score를 사용합니다.

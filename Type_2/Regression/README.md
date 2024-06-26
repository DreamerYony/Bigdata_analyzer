## 🍰 회귀 과제 실기 자료
### 🍰 주의
- 회귀 과제의 경우에는 predict_proba가 아닌 predict가 사용되고, 평가 지표로는 RMSE와 R2 score가 사용됩니다.
- 평가 지표는 sklearn.metrics에서 mean_squared_error와 r2_score를 임포트하여 사용합니다.
- mean_squared_error는 mse인데, 여기서 rmse를 구하기 위해서는 mean_squared_error(실제값, 예측값, squared = False)로 설정하면 mse에 제곱근을 씌운 값인 rmse가 계산됩니다.
### 🍰 포함된 파일
- Diamond_price(Regression).ipynb : 다이아몬드의 가격을 예측하는 과제입니다. 평가지표는 rmse를 사용합니다. 여기서는 문자열로 구성된 범주형 데이터(object)가 포함된 컬럼이 존재하고, 이를 원-핫 인코딩 하는 과정이 나타납니다.
- Diamond_price(simple_version).ipynb : 다이아몬드의 가격을 예측하는 과제입니다. 평가지표는 rmse를 사용합니다. 여기서는 문자열로 구성된 범주형 데이터(object)가 포함된 컬럼이 존재하고, 이를 원-핫 인코딩 하는 과정이 나타납니다. 위의 파일에서 인코딩 방법을 단순화한 파일입니다.
- Walmart_Unemployment(simple_version).ipynb : 월마트 실업률을 예측하는 과제입니다. 데이터셋의 스케일링은 생략한 simple version입니다. 평가지표는 rmse를 사용합니다.

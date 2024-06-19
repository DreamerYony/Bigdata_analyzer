## 🌻 카이제곱 검정
### 🌻 포함된 파일 :
#### Chi_square_test.ipynb
- 카이제곱 검정 중 독립성 검정을 수행하고, 로지스틱 회귀 모형을 사용하여 계수 및 오즈비를 계산합니다.
- 독립성 검정에서 필요한 패키지와 함수는 암기합니다 :   
  from scipy.stats import chi2_contingency
  result = pd.crosstab(df[], df[])  
  statistic, p_value, _, _ = chi2_contingency(result)
- 타이타닉 데이터셋을 대상으로 합니다.
- 로지스틱 회귀분석에서 필요한 패키지와 함수도 암기합니다 :
  from statsmodels.formula.api import logit  
  result2 = logit('종속변수 ~ 독립변수1, 독립변수2, 독립변수3', data=df).fit().summary()  
  result3 = logit('종속변수 ~ 독립변수1, 독립변수2, 독립변수3', data=df).fit().params
  np.exp(result3)

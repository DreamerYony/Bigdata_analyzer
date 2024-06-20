## 🚀 작업형 3유형 정리
### 🚀 정규성 검정
from statsmpdels.formula.api import shapiro  
statistic, p_value = shapiro(x)
### 🚀 한 개 그룹일 때 
- 단일표본 t-검정 : stats.ttest_1samp(x, 특정값, alternative)
- 윌콕슨 부호 검정 : stats.wilcoxon(x-특정값, alternative)
### 🚀 독립적인 두 개 그룹일 때
- 독립표본 t-검정 : stats.ttest_ind(x, y, alternative)
- Mann-Whitney U 검정 : stats.mannwhitneyu(x, y, alternative)
### 🚀 독립적이지 않은 두 개 그룹일 때 
- 쌍체표본 t-검정 : stats.ttest_rel(x, y, alternative)
- 윌콕슨 부호 검정 : stats.wilcoxon(x, y, alternative)
### 🚀 세 개 그룹일 때 
- ANOVA : stats.f_oneway(x, y, alternative)
- Kruskal-Wallis 검정 : stats.kruskal(x, y, alternative)
### 🚀 연관성 비교
- 카이제곱 검정(독립성 검정) : result = pd.crosstab(x, y) --> stats.chi2_contingency(result)
- 카이제곱 검정(적합성 검정) : stats.chisquare(x, y)
### 🚀 alternative의 사용
- two-sided : 양측 검정. 검정 통계량이 귀무 가설의 기대치와 양쪽 극단에서 벗어나는지를 확인.
- greater : 우측 검정. 검정 통계량이 귀무 가설의 기대치보다 큰지 확인.
- less : 좌측 검정. 검정 통계량이 귀무 가설의 기대치보다 작은지 확인.

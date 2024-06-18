## ⛳ 작업형 제2유형
- 실기 작업형 제2유형 자료입니다. 코드 파일 및 직접 가공한 데이터셋을 함께 제공합니다.
### ⛳ 포함된 코드 파일
#### Classification
- Mobile_Price(Classification).ipynb : 모바일폰의 가격대를 예측하는 과제.
- Mobile_Price(simple_version).ipynb : 모바일폰의 가격대를 예측하는 과제. 위 파일에서 일부 단계를 생략한 코드.
- Star_size(simple_version).ipynb : 별의 크기를 Giant 또는 Dwarf로 예측하는 과제.
#### Regression
- Diamond_price(Regression).ipynb : 다이아몬드의 가격을 예측하는 과제.
- Diamond_price(simple_version).ipynb : 다이아몬드의 가격을 예측하는 과제. 위 파일에서 인코딩 방법을 단순화한 코드.
- Walmart_Unemployment(simple_version).ipynb : 월마트의 실업률을 예측하는 과제.
### ⛳ 풀이 과정
- 분류 과제와 회귀 과제 모두 주요 풀이 과정은 다음의 순서를 따르고 있습니다.
- 실기 시험은 따로 코드에 대한 정답이 존재하지는 않습니다.
- 하지만 실전에 대비하기 위하여 정해진 순서를 외우고 간다면 도움이 될 것 같습니다.😁
1. 패키지 불러오기
2. 데이터 파일 읽기
3. info() 함수로 기본적인 정보 확인
4. 결측치 처리하기
5. describe() 함수로 요약 통계량 확인하기
6. 수치형 / 명목형 변수 리스트에 저장 --> 문제에 따라 생략 가능합니다.
7. 학습용 데이터와 검증용 데이터로 분리
8. 스케일링 수행 --> 문제에 따라 생략 가능합니다.
9. 모델 학습
10. 모델 평가
11. 파일 제출
### ⛳ 수치형 / 명목형 변수 변환에서의 주의사항
- info()함수를 사용해서 데이터셋의 행과 열, 결측치, 데이터 유형을 확인하면, 명목형 변수인 object가 있을 수 있습니다.
- 이때는 원핫 인코딩을 사용해서 명목형 변수를 수치형으로 바꿔야만 합니다.
- 포함된 파일 중 simple_version에서는 pandas의 get_dummies()함수를 사용해서 명목형 변수를 변환하였습니다.  
  ex) Diamond_price(simple_version).ipynb에서 'color'라는 컬럼의 데이터들이 새로운 컬럼으로 바뀌었습니다.
 11  color_D        43152 non-null  uint8   
 12  color_E        43152 non-null  uint8   
 13  color_F        43152 non-null  uint8  
 14  color_G        43152 non-null  uint8   
 15  color_H        43152 non-null  uint8  
 16  color_I        43152 non-null  uint8  
 17  color_J        43152 non-null  uint8
- 그러나 pandas의 get_dummies() 함수의 경우, 해당 데이터셋에 포함된 데이터만 컬럼으로 바뀌기 때문에 다른 데이터셋과 프레임이 일치하지 않게 되는 문제가 있습니다.
- 예를 들어, 훈련 데이터셋에 D~j라는 데이터가 있을 때 이것들은 get_dummies()를 통해 color_D ~ color_J라는 컬럼으로 만들어집니다.
  그리고 시험 데이터셋에 K라는 데이터가 있다면 이것은 get_dummies()를 통해 color_K라는 컬럼이 만들어집니다.
- 결국 훈련 데이터셋의 프레임의 형태와 시험 데이터셋의 프레임의 형태가 같지 않게 되어 이후 모델링 과정에서 오류가 나올 것입니다.
### ⛳ 수치형 / 명목형 변수 변환에서의 문제 해결
- 따라서 sklearn.preprocessing에서 OnehotEncoder 또는 LabelEncoder를 임포트하여 사용하는 것을 권장합니다.
- 이러한 인코더를 사용하면 데이터 형태를 일관되게 유지할 수 있습니다.
- Diamond_price(Regression).ipynb 파일에서 LabelEncoder를 임포트하여 사용한 것을 볼 수 있습니다.😁

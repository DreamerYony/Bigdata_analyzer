## ⛳ 작업형 제2유형
- 실기 작업형 제2유형 자료입니다. 코드 파일 및 직접 가공한 데이터셋을 함께 제공합니다.
### ⛳ 포함된 코드 파일
#### Classification
- Mobile_Price(Classification).ipynb : 모바일폰의 가격대를 예측하는 과제
- Mobile_Price(simple_version).ipynb : 모바일폰의 가격대를 예측하는 과제. 위 파일에서 일부 단계를 생략한 코드.
- Star_size(simple_version).ipynb : 별의 크기를 Giant 또는 Dwarf로 예측하는 과제.
#### Regression
- Diamond_price(simple_version).ipynb : 다이아몬드의 가격을 예측하는 과제.
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
6. 수치형 / 명목형 변수 리스트에 저장 --> 시험에서는 생략 가능합니다.
7. 학습용 데이터와 검증용 데이터로 분리
8. 스케일링 수행 --> 시험에서는 생략 가능합니다.
9. 모델 학습
10. 모델 평가
11. 파일 제출

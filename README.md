# 데이터 활용 부산관광 아이디어 공모전 (장려상)
- 목적 : 부산 해양/하천 관광지 맞춤형 코스 생성 서비스
- 일정 : 2023.01 - 2023.03
- 주최 : 부산관광공사 

## 주요 내용
부산 해양 및 하천 관광지에 대한 키워드를 추출하여 각 관광지를 대표할 수 있는 키워드를 바탕으로 군집화를 진행하여 코스를 추천해주고, 사용자가 위치와 키워드를 고려하여 부산 해양 및 하천 관광지를 찾고 원하는 관광지로 맞춤형 코스를 제공해주는 서비스기획 

### 1. 텍스트 데이터 전처리 
- 형태소 분석 및 명사 추출 : Mecab을 활용하여 형태소 분석을 진행
  
- 텍스트 정규화 : 예를 들어, ‘반려’, ‘댕댕이’, ‘애견’, ‘고양이’, ‘강아지’ 등의 단어들은 모두 ‘반려동물’로 통일해서 표시

- 불용어 삭제 : 600단어 이상의 불용어 지정

### 2. 텍스트 데이터 군집화
- 키워드 추출
한 관광지 내에서 추출한 명사들의 빈도수를 계산해 키워드 추출

- 피쳐 벡터화(TF-IDF)

  TF-IDF로 피쳐 벡터화를 진행하였고 문서 안에서 단어의 빈도가 10% 이하인 경우는 삭제하여 군집화에 활용될 키워드의 개수를 조절해 유의미한 정보만 남김

- 군집화(k-means)

  관광지에 대한 체계적인 분류를 위해서 군집화를 하였습니다. 군집화 방법으로 K-means를 사용했고 이때 K=10으로 설정하였습니다. 다음은 총 10개의 군집으로 나누어진 결과

  <img width="565" alt="image" src="https://github.com/kimjihooo/Traveling-Course-Creation/assets/97178674/66497db2-12c2-4175-9516-227f1c9aa6ce">


### 3. 서비스 기획
- Tableau를 활용해 코스 생성 서비스 구체화
  
  ![image](https://github.com/kimjihooo/Traveling-Course-Creation/assets/97178674/ac0384f0-5c7c-4549-9444-8dd1294ac5e6)
  
  https://public.tableau.com/app/profile/jihoo.kim3382/viz/_16758685634750/1

- 프로토타입 제작
  
  <img width="578" alt="image" src="https://github.com/kimjihooo/Traveling-Course-Creation/assets/97178674/9e556638-e017-42c8-b364-aeea914c4aed">

  <img width="580" alt="image" src="https://github.com/kimjihooo/Traveling-Course-Creation/assets/97178674/6d5d2530-3e1b-4160-a2c7-3cd3a258af28">
  
  <img width="579" alt="image" src="https://github.com/kimjihooo/Traveling-Course-Creation/assets/97178674/f11f6011-6ee9-472b-94eb-af3cd656fb43">

참고자료 : 머신러닝 완벽가이드. 권철민. 위키북스 



# 추천시스템 스터디  
- Coursera 강의를 중심으로 스터디 진행 후, 논문 실습 스터디 진행  
- 스터디 공부 내용을 주차별로 정리(Week1 ~ Week9)
- 머신러닝/딥러닝 기반의 모델 적용(Week10 ~ 진행 중)  

## 각 주차별 내용 정리
### 1. Week1
- 강의제목 : Introduction to Recommender Systems: Non-Personalized and Content-Based
- 강의주소 : https://www.coursera.org/learn/recommender-systems-introduction/home/welcome 
- 시청강의 : Preferences and Ratings, Predictions and Recommendations

- 과제 :
1. 모든 영화에 대한 평균 평점 계산, 평균 평점이 높은 영화 3개 구하기
2. 동일 평점의 영화 수를 세고, 가장 많은 평점이 기록된 영화 3개 구하기
3. 4점 이상이 가장 많이 기록된 영화 3개 구하기
* notebook : [homework_week1](https://github.com/gimys/recommeder_system/blob/master/week1/hw1_note.ipynb)  

### 2. Week2(생략)  
- 생략  

### 3. Week3
- 강의제목 : Introduction to Recommender Systems: Non-Personalized and Content-Based
- 강의주소 : https://www.coursera.org/learn/recommender-systems-introduction
- 시청강의 : Non-Personalized and Stereotype-Based Recommenders, Summary Statistics I & II, Demographics and Related Approaches

- 과제 :
1. 토이스토리를 본 사람들이 본 다른 영화와 상관 관계를 구하기 -> (토이스토리and다른영화)/토이스토리
2. 피어슨유사도로 토이스토리와 다른 영화들의 상관관계 도출하기
3. 성별간 평점을 아래의 조건으로 구하시오
> a) 모든 영화에 대한 평점을 성별별로 구하기  
> b) 각 성별의 상위 3개의 영화 구하기  
> c) 성별간 평점 차이가 큰 영화를 구하기  
> d) 성별의 모든 평점을 합한 값의 차이를 구하기 -> 여성평점-남성평점  
4. 각 성별에서 4점 이상의 점수를 갖는 영화들의 성별간 차이를 구하기
* notebook : [homework_week3](https://github.com/gimys/recommeder_system/blob/master/week3/week3_homework.ipynb)  
  
### 4. Week4
- 강의제목 : Nearest Neighbor Collaborative Filtering
- 강의주소 : https://www.coursera.org/learn/collaborative-filtering?specialization=recommender-systems
- 시청강의 : User-User Collaborative Filtering, Configureing User-User Collaborative Filtering

- 과제
1. 파일설명 :
> a) user.csv : 사용자가 column, 영화가 row인 행렬
> b) item.csv : 영화가 column, 가용자가 row인 행렬
2. 사용자-사용자 연관성 행렬을 완성하시오
> - 연산 결과는 1648과 사용자 5136의 연관성은 0.40298, 사용자 918과 사용자 2824의 연관성은 -0.31706
3. 사용자 3867과 사용자 89의 이웃을 각각 5명씩 구하기
> - 사용자 3712의 이웃은 2724 (연관성: 0.46291), 3867 (연관성: 0.400275), 5062 (연관성: 0.247693), 442 (연관성: 0.22713), 3853 (연관성: 0.19366)
4. 이웃 사용자 다섯명의 평점들을 통해 사용자 3867과 사용자 89의 모든 영화들에 대해 다섯명의 이웃들의 Correlation-weighted average를 사용하여 예상평점을 구하기(수식은 notebook 참고)  
5. 사용자 3867과 사용자 89에 대한 예상평점을 계산하고 상위 3개의 영화 구하기  
6. 4번 문제를 수식을 바꾸어 풀어보시오(notebook 참고)
* notebook : [homework_week4](https://github.com/gimys/recommeder_system/blob/master/week4/week4_homework.ipynb)  

### 5. Week5
- 강의제목 : Nearest Neighbor Collaborative Filtering
- 강의주소 : https://www.coursera.org/learn/recommender-metrics?specialization=recommender-systems
- 시청강의 : The Goals of Evaluation, Hidden Data Evaluation, Prediction Accuracy Metrics, Decision Support Metrics, Rank-Aware Top-N Metrics

- 과제
1. 파일설명 :
> a) ratings.csv : 사용자-아이템 별 평점  
> b) predictions.csv : 예측된 평점  
2. 다음 세가지 방법으로 전체 MAE를 구하기
> a) 기본 MAE: 모든 예측값들에 대한 MAE
> b) 사용자 MAE: 각 사용자들에 대한 평균 MAE (예를 들어 5261 사용자의 MAE는 0.82)
> c) 아이템 MAE: 각 아이템들에 대한 평균 MAE (예를 들어 Forest Gump의 MAE는 0.5)
> d) 가장 높은 MAE를 가진 사용자와 가장 낮은 MAE를 가진 사용자를 구하고 각각의 MAE를 구하기
3. 2번과 같은 과정을 MSE와 RMSE로 계산하기
* notebook : [homework_week5](https://github.com/gimys/recommeder_system/blob/master/week5/homwork_week5.ipynb)  

### 6. Week6
- 강의제목 : Nearest Neighbor Collaborative Filtering
- 강의주소 : https://www.coursera.org/learn/recommender-metrics?specialization=recommender-systems
- 시청강의 : Beyond Basic Evaluation, Additional Item and List-Based Metrics, Experimental Protocols, Unary Data Evaluation

- 과제
1. 파일설명 :
> a) ml-ratings.csv : 사용자-아이템 별 평점  
> b) ml-preds.csv : 예측된 평점  
2. Recall@10과 MRR@10을 구하기
> - pandas의 rank 함수는 method='first'를 적용하여 동점을 처리한다.
* notebook : [homework_week6](https://github.com/gimys/recommeder_system/blob/master/week6/homework_week6.ipynb)  

### 7. Week7
- 강의제목 : Nearest Neighbor Collaborative Filtering
- 강의주소 : https://www.coursera.org/learn/matrix-factorization?specialization=recommender-systems
- 시청강의 : Matrix Factorization and Advanced Techniques, Introduction to Matrix Factorization and Dimensionality Reduction, Singular Value Decomposition

- 과제
1. week6의 데이터를 사용하여 MAP@10, nDCG@10, binary nDCG@10을 구하기(binary는 평점이 4이상이면 1, 4미만이면 0으로 변환)
> - pandas의 rank 함수는 method='first'를 적용하여 동점을 처리한다.
* notebook : [homework_week7](https://github.com/gimys/recommeder_system/blob/master/week7/homework_week7.ipynb)  

### 8. Week8
- 스터디 내용 : 기본적인 추천 알고리즘 실습 및 논문 작성을 위한 선행 연구 조사 결과 공유

- 과제  
1. pytorch의 dataloader 사용을 위한 class 오버라이딩 실습  
* notebook : [homework_week8](https://github.com/gimys/recommeder_system/blob/master/week8/homework_week8.ipynb)  

### 9. Week9
- 스터디 내용 : surprise 모듈을 활용한 Matrix Factorization 실습  

- 과제  
1. Surprise를 사용해서 binary 데이터의 Matrix Factorization 실시  
* notebook : [homework_week9](https://github.com/gimys/recommeder_system/blob/master/week9/homework_week9.ipynb)  

### 10. Week10
- 논문명 :  Neural Collaborative Filtering  
- 논문출처 : https://arxiv.org/abs/1708.05031  
- 내용 : User와 Item을 임베딩하여 dot product로 유사도를 구하는 딥러닝 기반의 matrix factorization 기법  


### 11. Week11
- 논문명 :  Neural Collaborative Filtering  
- 논문출처 : https://arxiv.org/abs/1708.05031  
- 내용 : User와 Item을 임베딩하여 dot product로 유사도를 구하는 딥러닝 기반의 matrix factorization 기법  

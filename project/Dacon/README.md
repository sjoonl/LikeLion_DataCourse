# 팀프로젝트 - Dacon 가스공급량 수요 예측 모델개발(2021.10.11 ~ 2021.12.10)
+ 팀원: 이성준, 박승규, 노현곤

## 1.개요
+ 한국 가스 공사가 보유한 다년간 시간 단위 공급량 데이터를 기반으로 미래 공급량을 예측하는 모델을 만든다.

## 2.주제
+ 한국가스공사의 시간단위 가스 공급량 데이터와 기상 데이터 및 유가 데이터를 종합한 데이터셋을 구축하여 90일 한도 일간 공급량을 예측하는 인공지능 모델을 개발
+ 2013 ~ 2018년도 가스공급량 데이터로 모델을 학습 후 2019년 1,2,3월 가스공급량을 예측한다

## 3.주최 및 주관
+ 한국가스공사
+ 대회링크: https://dacon.io/competitions/official/235830/overview/description

## 4.데이터
+ 내부 데이터: 가스 공급량 데이터(2013~2018)
+ 외부 데이터: 기상청 데이터(2013~2018)

## 5.분석 과정 및 방법
+ 수집한 2013년 ~ 2018년 기온데이터를 새로운 feature로 생성한다.
+ 가스 공급량과 상관관계가 높은 feature를 추출하여 사용한다.
+ 수집한 2013년 ~ 2018년 기온데이터를 이용하여 2019년도 기온을 예측하여 2019년 가스 공급량 데이터 예측을 위한 입력으로 활용한다.

## 6.분석에 이용한 기술
+ 데이터 전처리 및 EDA: python, pandas, numpy, matplotlib, seaborn
+ 머신러닝 모델 : scikit learn- LinearRegression, RandomForest, Xgboost, LightGBM, Catboost, PyCaret
+ 평가지표: NMAE, MSE, RMSE, MAE

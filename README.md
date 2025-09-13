# 📱 Smart Motion Classification System
> 웨어러블 센서 데이터를 활용한 실시간 동작 인식 및 분류

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0+-orange.svg)](https://scikit-learn.org/)
[![IoT](https://img.shields.io/badge/IoT-Sensor%20Data-green.svg)]()
[![Signal Processing](https://img.shields.io/badge/Signal-Processing-red.svg)]()

## 📋 프로젝트 개요

**스마트 모션 분류 시스템**은 스마트폰의 가속도계, 자이로스코프, 지자기센서 데이터를 활용하여 사용자의 동작을 실시간으로 인식하고 분류하는 프로젝트입니다. 
계층적 분류 아키텍처를 통해 정적 동작과 동적 동작을 효과적으로 구분하며, 웨어러블 환경에서 실시간 동작 인식이 가능합니다.

### 🎯 주요 목표
- 스마트폰 센서 데이터 기반 실시간 동작 인식
- 계층적 분류를 통한 정확도 향상
- 웨어러블 환경에서의 실용적 활용
- 다양한 일상 동작의 정밀한 분류

## 🏆 주요 성과

<img width="1274" height="449" alt="image" src="https://github.com/user-attachments/assets/04134fdc-263d-4583-a812-0217b83bfc69" />

### 🧠 모델 아키텍처 혁신
- **계층적 분류 우수성**: 단일 모델 대비 분류 성능 향상
- **전체 특성 활용**: 상위 10개 특성보다 전체 특성이 더 효과적
- **정적/동적 분리**: LAYING, SITTING, STANDING과 WALKING 계열 동작의 명확한 구분

### 📊 데이터 분석 인사이트
- **특성 중요도 분석**: 주요 feature일수록 활동 간 분포가 명확히 구분
- **패턴 발견**: 영향력이 큰 feature는 특정 활동에 값이 집중되는 현상 발견
- **최종 정확도**: 98% 이상의 높은 분류 정확도 달성

### 🔍 실시간 처리
- **웨어러블 최적화**: 실시간 센서 데이터 처리 및 분류
- **6가지 기본 동작 인식**: 걷기, 뛰기, 앉기, 서기, 계단 오르기/내리기
- **확장 가능한 동작**: 운동 동작, 교통수단 이용, 휴대폰 사용 패턴

## 📊 센서 데이터 특성

### 센서 구성
| 센서 | 측정값 | 용도 |
|------|--------|------|
| **가속도계** | X, Y, Z 축 가속도 | 움직임 감지, 방향 변화 |
| **자이로스코프** | 각속도 측정 | 회전 감지, 자세 변화 |
| **지자기센서** | 방향 정보 | 자세 보정, 절대 방향 |

### 인식 가능한 동작
- **정적 동작**: 앉기(SITTING), 서기(STANDING), 누워있기(LAYING)
- **동적 동작**: 걷기(WALKING), 계단 오르기(WALKING_UPSTAIRS), 계단 내려가기(WALKING_DOWNSTAIRS)
- **확장 동작**: 뛰기, 운동, 교통수단 이용, 휴대폰 사용 패턴

## 🔍 데이터 분석
<img width="1443" height="420" alt="image" src="https://github.com/user-attachments/assets/c983bc8d-fb06-483f-9063-2a1d5ce7d2a4" />
- 데이터 학습 영향력 분석

<img width="1584" height="419" alt="image" src="https://github.com/user-attachments/assets/92175d3c-c7c3-4457-a2e0-c6881523cc07" />

- 학습 데이터에 따른 성능 분석


## 📈 모델 성능 분석

### 전체 특성 vs 상위 10개 특성 비교

| 접근법 | 정확도 | Precision | Recall | F1-Score |
|--------|--------|-----------|--------|----------|
| **전체 특성 학습** | **98%** | **0.98** | **0.98** | **0.98** |
| 상위 10개 특성 | 85% | 0.84 | 0.83 | 0.83 |

### 계층적 분류 성능
```
Classification Report:
                    precision    recall  f1-score   support

        LAYING         1.00      0.99      0.99       292
       SITTING         1.00      0.94      0.97       254
      STANDING         0.95      0.97      0.96       287
       WALKING         0.99      0.98      0.99       215
WALKING_DOWNSTAIRS     0.97      0.99      0.98       195
  WALKING_UPSTAIRS     0.99      0.98      0.98       215

     accuracy                           0.98      1471
    macro avg         0.98      0.98      0.98      1471
 weighted avg         0.98      0.98      0.98      1471
```

## 🔬 데이터 분석 결과

### 주요 발견사항
1. **특성 중요도**: 주요 feature일수록 활동 간 분포가 명확히 구분됨
2. **특성 개수**: 상위 10개 특성으로만 학습한 모델이 낮은 성능을 보임
3. **동작 구분**: 정적 동작(LAYING, SITTING, STANDING)과 동적 동작(WALKING 계열)의 명확한 분류 성능 향상

### 센서 데이터 시각화
- **KDE Plot**: 각 동작별 센서 값 분포 분석
- **Violin Plot**: 동작별 특성 값의 분산 및 분포 형태
- **Feature Importance**: 분류에 가장 중요한 센서 특성 순위


## 🙏 감사의 말

- Scikit-learn 커뮤니티의 머신러닝 라이브러리
- UCI Machine Learning Repository의 Human Activity Recognition 데이터셋
- 웨어러블 센서 연구 커뮤니티

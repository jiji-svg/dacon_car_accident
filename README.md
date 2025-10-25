# dacon_car_accident
For study purpose uploading dacon contest code

## 개요
교통사고는 차량/도로 환경 뿐만 아니라 운수종사자의 인지 특성에 크게 좌우됩니다.
이러한 특성을 활용해 사고 위험도를 예측하는 AI 모델을 개발하자.

## 주제
운수종사자 인지적 특성 데이터를 활용한 교통사고 위험 예측 AI 모델 개발

## 대회 방식
1차 평가, 2차 평가
1차 평가: 최종 Public 리더보드 기준 상위 15팀
2차 평가: '모델 개발 보고서'와 '데이터 분석 보고서'를 작성, 이를 종합하여 평가하여 상위 7팀을 수상.

## 조건
- 본 대회는 submit.zip 업로드 방식의 '코드 제출 대회'로 진행
- submit.zip에는 model/(model.pt) , script.py, requirements.txt로 구성되어야 함.
- 추론 코드 실행 시간 < 30분 + 패키지 설치 시간 < 10분 + 제출 파일 용량 제한 < 10GB + ONLY CPU

## 평가 기준
- 리더보드 산식: 0.5 * (1-AUC) + 0.25*Brier + 0.25*ECE

### AUC(Area Under the ROC Curve)
- ROC curve는 FPR(false positive rate)에 대한 TPR(true positive rate==recall)을 나타낸 그래프.
- AUC는 ROC 곡선 아래 면적.
- 무작위로 뽑은 양성 샘플과 음성 샘플중 모델이 양성에 더 높은 점수를 줄 확률.

### Brier Score
- 이진 분류에서 예측한 확률 p와 실제 라벨 y 사이의 평균 제곱 오차
- <img width="302" height="94" alt="image" src="https://github.com/user-attachments/assets/6c9a777c-f1dd-44b4-b30a-b9a014f4242c" />

### ECE (Expected Calibration Error)
- 예측 확률의 '보정 정도'를 요약한 지표
- <img width="415" height="96" alt="image" src="https://github.com/user-attachments/assets/83f76f2d-5a48-40f0-abc4-f5934708f71c" />


## 데이터
- open_v2.zip
  - baseline_submit.zip
  - data/
    - sample_submission.csv
    - train.csv
    - test.csv
    - test/
      - A.csv
      - B.csv
    - train/
      - A.csv
      - B.csv
- train.csv : 학습 샘플 목록이 포함된 CSV (944,767행)
- test.csv : 테스트 샘플 목록이 포함된 CSV
- train/A.csv: 학습 샘플 중 신규 자격 검사 샘플 (647,241행)
- train/B.csv : 학습 샘플 중 자격 유지 검사 샘플 (297,526행)
- test의 A와 B도 마찬가지

  

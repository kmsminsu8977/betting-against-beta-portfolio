# 발표 초안

## 1. 문제 정의

저베타 그룹을 시장 베타 1로 스케일하면 고베타 그룹 대비 기대 초과수익 스프레드가 남는가?

## 2. 데이터와 가정

- 합성 샘플 데이터: `data/sample/asset_beta_panel.csv`
- 재현 가능한 baseline 실행을 우선 구성

## 3. 방법

저베타 자산을 레버리지하고 고베타 자산을 축소하는 BAB 아이디어를 단순 수치로 검증한다.

## 4. 현재 산출물

- 실행 스크립트: `python -m src.run_baseline`
- 결과 표: `outputs/tables/baseline_results.csv`

## 5. 후속 작업

- 실제 데이터 연결
- 민감도 분석
- 차트/보고서 산출
- 프로젝트별 상세 검증

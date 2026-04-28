# Betting Against Beta Portfolio

Betting Against Beta 포트폴리오 프로젝트의 기본 연구 구조와 재현 가능한 baseline 산출물을 담은 저장소입니다.

**핵심 연구 질문**

> 저베타 그룹을 시장 베타 1로 스케일하면 고베타 그룹 대비 기대 초과수익 스프레드가 남는가?

## 저장소 구조

```text
betting-against-beta-portfolio/
├── src/                         # baseline 계산 로직과 실행 엔트리포인트
├── data/sample/                 # 합성 샘플 입력 데이터
├── docs/                        # 방법론과 해석 기준
├── notebooks/                   # 실행 흐름을 보여주는 최소 노트북
├── outputs/tables/              # 재현 가능한 결과 CSV
├── presentation/                # 발표/보고서 초안
└── references/                  # 재작성 개념 노트와 참고문헌 메모
```

## 빠른 시작

```bash
python -m src.run_baseline
```

실행 결과는 `outputs/tables/baseline_results.csv`에 저장됩니다.

## 구현 범위

- 베타 중앙값을 기준으로 저베타/고베타 leg를 나누고 각 leg를 베타 1로 스케일한다.
- 스케일된 기대 초과수익 차이를 BAB spread의 첫 진단 지표로 둔다.
- 수익률과 베타는 BAB leg 구성을 설명하는 교육용 합성 패널이다.

## 주요 파일

- `src/bab_baseline.py`: 저베타 자산을 레버리지하고 고베타 자산을 축소하는 BAB 아이디어를 단순 수치로 검증한다.
- `data/sample/asset_beta_panel.csv`: baseline 실행용 합성 입력값
- `docs/methodology.md`: 계산 절차, 입력/출력 정의, 해석상 주의점
- `outputs/tables/baseline_results.csv`: 현재 baseline 산출물

## 다음 확장 방향

- 실제 공개 데이터 또는 별도 수집 데이터 연결
- notebook 기반 탐색 분석 추가
- 차트와 표를 포함한 최종 보고서 작성
- 모델 검증, 민감도 분석, 비용/리스크 가정 보강

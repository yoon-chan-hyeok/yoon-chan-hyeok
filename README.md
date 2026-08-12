![Yoon Chanhyuk, AI/ML Engineer](assets/portfolio-hero.svg)

<div align="center">

## 윤찬혁 · AI/ML Engineer

서울과학기술대학교 교통공학 전공

[Portfolio](https://yoon-chan-hyeok.github.io/) · [RAG](https://github.com/yoon-chan-hyeok/temporal-rag-drift) · [Multi-Agent](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization) · [OCR](https://github.com/yoon-chan-hyeok/ocr-quality-monitoring)

</div>

AI 기능을 구현한 뒤 실제 조건이 바뀌었을 때 무엇이 깨지는지 확인하는 작업에 관심이 있습니다. 평균 점수 하나보다 어떤 입력에서 성능이 낮아졌는지, 실패가 어느 단계에서 시작됐는지, 운영자가 다음에 무엇을 확인해야 하는지를 측정 가능한 형태로 만드는 편입니다.

최근에는 RAG 지식베이스 업데이트 이후의 성능 저하, multi-agent execution trace의 exact-step failure localization, 라벨이 늦게 들어오는 OCR pipeline의 drift monitoring을 다뤘습니다. 연구용 코드는 평가 protocol, aggregate result와 test를 함께 공개하고 있습니다. 생체정보나 원천 데이터 제약이 있는 프로젝트는 공개 가능한 설계와 판단 근거를 case study로 정리했습니다.

## 관심 있는 문제

모델의 평균 성능보다 실제 환경에서 조건이 달라졌을 때 생기는 실패에 관심이 있습니다. 데이터나 지식베이스가 바뀐 뒤 어떤 입력부터 성능이 낮아지는지, 여러 단계로 이어진 시스템에서 오류가 어디서 시작됐는지, 정답 라벨이 늦게 들어올 때 무엇을 먼저 검토해야 하는지를 다룹니다.

탐지 결과는 사람이 다음 행동을 정할 수 있어야 한다고 생각합니다. 그래서 점수만 계산하기보다 검토 대상을 정렬하고, failure mechanism 후보를 좁히며, 결과를 어디까지 해석할 수 있는지 함께 기록합니다.

## 일하는 방식

프로젝트를 시작할 때 실제 배포 환경에서 입력이 어떻게 달라지고 누가 결과를 사용할지 먼저 생각합니다. 비슷한 문제를 다룬 선행 사례를 살펴본 다음, 핵심 가설만 확인할 수 있는 가벼운 목업이나 작은 실험을 만듭니다. 이 단계에서 가능성이 보이면 평가 기준과 실패 조건을 정리하고 상세 구현으로 확장합니다.

예상대로 작동하지 않을 때는 결과를 덮기보다 실패 사례, 데이터 조건과 실행 단계를 다시 나눠 봅니다. 진단 과정에서 새로 확인한 지식과 해결법은 실험 기록, 재현 절차, 테스트와 학습 로드맵으로 남깁니다. 완성된 기능만 보여주기보다 어떤 판단을 거쳐 현재 설계에 도달했는지 설명하려고 합니다.

## 프로젝트

### [Temporal RAG Drift](https://github.com/yoon-chan-hyeok/temporal-rag-drift)

DB 업데이트 이후 새로 발생한 RAG 성능 저하를 label-free하게 모니터링합니다. 탐지된 사례에는 evidence intervention을 적용해 retrieval coverage, ranking, context complexity와 evidence utilization 중 어느 구간을 먼저 조사해야 하는지 좁힙니다.

`Frozen temporal transfer` · `Distribution shift` · `P1-P5 diagnostic probe`

### [TSR-Loc: Multi-Agent Failure Localization](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization)

Task-only success requirements를 먼저 고정하고 execution trace를 시간순으로 검사합니다. 이후 step에서 복구되지 않은 가장 이른 오류를 responsible agent와 exact step으로 반환하는 training-free evaluation framework입니다.

`Requirement compiler` · `Trace localizer` · `Agent and exact-step evaluation`

### [Label-Free OCR Quality Monitor](https://github.com/yoon-chan-hyeok/ocr-quality-monitoring)

OCR embedding의 record-level anomaly와 batch-level distribution shift를 함께 계산합니다. Gold label이 도착하기 전에 사람이 먼저 검수할 결과를 review queue로 정렬하는 installable CLI입니다.

`Nearest-neighbor drift` · `Median/MAD` · `RBF-MMD` · `CLI and CI`

### [Face Attendance System](https://github.com/yoon-chan-hyeok/face-attendance-system)

RetinaFace와 ArcFace를 multi-frame enrollment, ambiguity rejection, FastAPI·MariaDB·React 출결 workflow로 연결했습니다. 생체정보와 원본 운영 환경은 공개하지 않고 architecture와 decision rule을 case study로 정리했습니다.

### [Event Traffic Delay Analysis](https://github.com/yoon-chan-hyeok/event-traffic-delay-analysis)

OD·생활인구·버스·GIS 데이터를 결합해 행사 종료 후 수요 집중을 분석했습니다. 분석 결과를 3개 환승거점과 capacity·cost constraint가 있는 shuttle operating scenario로 변환한 교통공학 졸업 연구입니다.

## 기술과 작업 범위

- Evaluation: temporal split, frozen transfer, baseline and ablation, paired significance test
- Reliability: distribution drift, semantic uncertainty, failure attribution, intervention probe
- AI systems: retrieval, embeddings, NLI, model backends, computer vision
- Engineering: Python, FastAPI, SQLAlchemy, MariaDB, React, TypeScript, CLI, CI
- Data analysis: EDA, GIS, multi-source join, demand and capacity scenario

각 저장소 README에는 프로젝트를 시작한 이유, 구현 범위, 평가 결과, 실행 방법과 해석 한계를 구분해 적었습니다.

## 문서로 보는 작업 과정

| 프로젝트 | 먼저 볼 문서 | 더 자세한 기록 |
|---|---|---|
| Temporal RAG Drift | [README](https://github.com/yoon-chan-hyeok/temporal-rag-drift#readme) | [Methods](https://github.com/yoon-chan-hyeok/temporal-rag-drift/blob/main/docs/METHODS.md) · [Results](https://github.com/yoon-chan-hyeok/temporal-rag-drift/blob/main/docs/RESULTS.md) · [Limitations](https://github.com/yoon-chan-hyeok/temporal-rag-drift/blob/main/docs/LIMITATIONS.md) · [Reproducibility](https://github.com/yoon-chan-hyeok/temporal-rag-drift/blob/main/docs/REPRODUCIBILITY.md) |
| Multi-Agent Failure Localization | [README](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization#readme) | [Method](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization/blob/main/docs/METHOD.md) · [Data and Evaluation](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization/blob/main/docs/DATA_AND_EVALUATION.md) · [Experiment History](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization/blob/main/docs/EXPERIMENT_HISTORY.md) |
| OCR Quality Monitoring | [README](https://github.com/yoon-chan-hyeok/ocr-quality-monitoring#readme) | [Learning and Engineering Roadmap](https://github.com/yoon-chan-hyeok/ocr-quality-monitoring/blob/main/docs/LEARNING_ROADMAP.md) |
| Face Attendance System | [README](https://github.com/yoon-chan-hyeok/face-attendance-system#readme) | [Learning and Engineering Roadmap](https://github.com/yoon-chan-hyeok/face-attendance-system/blob/main/docs/LEARNING_ROADMAP.md) |
| Event Traffic Delay Analysis | [README](https://github.com/yoon-chan-hyeok/event-traffic-delay-analysis#readme) | [Learning and Engineering Roadmap](https://github.com/yoon-chan-hyeok/event-traffic-delay-analysis/blob/main/docs/LEARNING_ROADMAP.md) |


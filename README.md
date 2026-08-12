![Yoon Chanhyuk, AI/ML Engineer](assets/portfolio-hero.svg)

<div align="center">

## 윤찬혁 · AI/ML Engineer

서울과학기술대학교 교통공학 전공

[Portfolio](https://yoon-chan-hyeok.github.io/) · [RAG](https://github.com/yoon-chan-hyeok/temporal-rag-drift) · [Multi-Agent](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization) · [OCR](https://github.com/yoon-chan-hyeok/ocr-quality-monitoring)

</div>

AI 기능을 구현한 뒤 실제 조건이 바뀌었을 때 무엇이 깨지는지 확인하는 작업에 관심이 있습니다. 평균 점수 하나보다 어떤 입력에서 성능이 낮아졌는지, 실패가 어느 단계에서 시작됐는지, 운영자가 다음에 무엇을 확인해야 하는지를 측정 가능한 형태로 만드는 편입니다.

최근에는 RAG 지식베이스 업데이트 이후의 성능 저하, multi-agent execution trace의 exact-step failure localization, 라벨이 늦게 들어오는 OCR pipeline의 drift monitoring을 다뤘습니다. 연구용 코드는 평가 protocol, aggregate result와 test를 함께 공개하고 있습니다. 생체정보나 원천 데이터 제약이 있는 프로젝트는 공개 가능한 설계와 판단 근거를 case study로 정리했습니다.

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


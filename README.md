![Yoon Chanhyuk, AI/ML Engineer](assets/portfolio-hero.svg)

<div align="center">

## 윤찬혁 · AI/ML Engineer

AI와 데이터 시스템에서 실패가 어디서 발생하는지 찾고, 이를 측정 가능한 신호로 바꿔 개선 방법을 검증합니다.

서울시립대학교 교통공학과·인공지능학과 복수전공 · 2026.08 졸업예정

ADsP · SQLD · 교내 데이터 분석 프로젝트 우수상

[Portfolio](https://yoon-chan-hyeok.github.io/) · [RAG Failure Detection](https://github.com/yoon-chan-hyeok/temporal-rag-drift) · [Agent Evaluation](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization) · [OCR Monitoring](https://github.com/yoon-chan-hyeok/ocr-quality-monitoring)

</div>

운영에서는 정답이 늦게 도착하거나, 긴 실행 기록에서 원인이 묻히거나, 여러 출처의 데이터를 같은 판단 기준으로 묶어야 하는 제약이 생깁니다. 저는 실제 실패와 데이터 현상을 먼저 확인하고, 이를 측정 가능한 질문으로 바꾼 뒤 구현과 평가를 진행했습니다.

RAG, multi-agent system과 OCR에서는 답변 분포, embedding과 execution trace를 비교 가능한 신호로 구성해 위험 사례와 조사 대상을 좁혔습니다. 교통 데이터 분석에서는 OD, 생활·체류인구, 버스와 GIS 데이터를 결합해 수요 증가와 공급 변화가 함께 나타나는 패턴을 운영 시나리오로 연결했습니다.

아이디어는 작은 목업으로 먼저 확인합니다. 가능성이 보이면 평가 기준을 고정하고 구현을 넓히며, 결과가 예상과 다르면 데이터와 실행 단계를 나눠 다시 진단합니다. 실행 코드에는 테스트, 재현 절차와 해석 한계를 함께 남깁니다.

RAG, multi-agent와 OCR 연구에서는 문제 정의, 가설, 실험 방향, 평가와 결과 해석을 주도했습니다. 구현과 반복 검증에는 Codex를 사용했습니다. Face Attendance는 기존 시스템 이후의 고도화 작업이며, 교통 분석은 개인 프로젝트입니다.

이 GitHub에는 기존 실험, 수업 프로젝트와 졸업 연구를 공개 가능한 형태로 다시 정리했습니다. 따라서 저장소 생성일이 실제 작업을 시작한 시점과 같지는 않습니다.

## 경험

- **지능형빅데이터 연구실 · 2026.03부터 약 6개월**: Temporal RAG, multi-agent failure attribution, OCR failure monitoring과 face-attendance 고도화
- **교통공학과 연구인턴 · 2025년 여름 6주**: 교차로 CCTV simulation 영상의 차량 탐지·tracking과 trajectory 추출 실험
- **교통공학과 학생회 사무국**: 예산 안에서 행사를 계획하고 현장 비용, 역할 조율과 인수인계 문서를 관리

## 대표 프로젝트

### [Temporal RAG Failure Detection](https://github.com/yoon-chan-hyeok/temporal-rag-drift)

DB 업데이트 직후에는 모든 질문의 최신 gold answer를 다시 만들기 어렵습니다. 업데이트 전후 RAG의 행동 변화만으로 새롭게 실패했을 가능성이 높은 질문을 탐지하고, evidence intervention으로 먼저 조사할 구간을 좁혔습니다.

Detector를 다시 맞추지 않은 미래 질문 186건 평가에서 AUROC `0.854`, Recall `0.714`, F1 `0.615`, Risk lift `3.59×`를 기록했습니다.

`Python` · `Retrieval` · `Embeddings` · `NLI` · `Temporal evaluation`

### [TSR-Loc: Multi-Agent Failure Localization](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization)

긴 execution trace에서는 마지막 오류만 보거나 이미 복구된 첫 실수를 원인으로 고르기 쉽습니다. Task의 성공 조건을 먼저 고정하고, 이후에도 복구되지 않은 가장 이른 오류를 agent와 exact step으로 찾았습니다.

Who&When 184 trajectories에서 task-only TSR-Loc의 exact-step accuracy는 `38.59%`였습니다. Direct 방식보다 `30.43%p` 높았고, A2P 대비 차이는 통계적으로 유의하지 않았습니다.

`Python` · `Execution trace` · `Failure attribution` · `Statistical evaluation`

### [Major Event Travel Time Delay Analysis](https://github.com/yoon-chan-hyeok/event-traffic-delay-analysis)

대형 행사 뒤 이동 불편을 계기로 시작한 개인 프로젝트입니다. 초기 정류장 매칭 품질을 다시 점검하고, OD·체류인구·버스·GIS 데이터를 결합해 혼잡을 수요 증가와 공급 proxy 감소가 함께 나타나는 문제로 확장했습니다. 선형 관계가 맞지 않는 구간에는 isotonic regression을 적용했습니다.

`Python` · `EDA` · `GIS` · `Isotonic regression` · `Data quality`

### [Label-Free OCR Failure Monitoring](https://github.com/yoon-chan-hyeok/ocr-quality-monitoring)

정답 transcription이 늦게 도착하는 OCR 환경에서 confidence와 embedding novelty를 failure signal로 비교했습니다. Confidence가 예상보다 강했고 embedding의 추가 이득은 오류 유형마다 달랐습니다. 공개 저장소에는 record·batch drift를 review queue로 연결하는 CLI와 테스트를 정리했습니다.

`Python` · `Confidence baseline` · `Embedding drift` · `Negative result` · `CI`

### [Face Attendance System Hardening](https://github.com/yoon-chan-hyeok/face-attendance-system)

기존 얼굴 출결 시스템에서 외형이 비슷한 사람이 승인되는 사례를 확인했습니다. Multi-frame enrollment, centroid 후보와 sample 재검증, top-1/top-2 margin을 적용하고 등록 단계에 계산량을 집중해 출결 시 추론 부담을 줄이는 방향으로 고도화했습니다.

`Existing system hardening` · `Computer vision` · `FastAPI` · `MariaDB` · `React`

## 기술

- AI/ML: PyTorch, scikit-learn, XGBoost, retrieval, embeddings, NLI, semantic uncertainty, computer vision
- Evaluation: temporal split, frozen transfer, baseline and ablation, paired significance test
- Engineering: Python, FastAPI, SQLAlchemy, MariaDB, React, TypeScript, CLI, CI
- Data: SQL, pandas, NumPy, EDA, GIS, multi-source join, distribution shift, isotonic regression

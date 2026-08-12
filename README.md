![Yoon Chanhyuk, AI/ML Engineer](assets/portfolio-hero.svg)

<div align="center">

## 윤찬혁 · AI/ML Engineer

AI 기능이 실제 환경에서 언제, 왜 실패하는지 찾고 다시 고칠 수 있는 형태로 만드는 엔지니어입니다.

서울과학기술대학교 교통공학 전공

[Portfolio](https://yoon-chan-hyeok.github.io/) · [RAG Monitoring](https://github.com/yoon-chan-hyeok/temporal-rag-drift) · [Agent Evaluation](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization) · [OCR Monitoring](https://github.com/yoon-chan-hyeok/ocr-quality-monitoring)

</div>

RAG, multi-agent system, OCR처럼 여러 단계가 연결된 AI 시스템을 다뤘습니다. 평균 성능을 보고 끝내기보다 어떤 입력이 새로 위험해졌는지, 실패가 어느 단계에서 시작됐는지, 운영자가 무엇을 먼저 확인해야 하는지까지 연결합니다.

아이디어는 작은 목업과 실험으로 먼저 확인합니다. 가능성이 보이면 평가 기준을 고정하고 구현 범위를 넓히며, 결과가 예상과 다르면 데이터와 실행 단계를 나눠 다시 진단합니다. 실험 결과뿐 아니라 재현 절차, 테스트와 해석 한계도 코드와 함께 남깁니다.

## 맡길 수 있는 일

- 데이터와 실행 조건이 바뀐 뒤 생기는 성능 저하를 탐지하는 평가·모니터링 설계
- 긴 실행 기록에서 실패에 책임 있는 단계와 조사할 원인 후보를 좁히는 도구 구현
- 연구 아이디어를 Python 패키지, CLI, API, 테스트와 재현 가능한 실험으로 연결
- 모델 출력이 실제 업무 흐름에 들어갈 때 필요한 거절 기준, 데이터 모델과 운영 경계 설계

## 대표 프로젝트

### [Temporal RAG Drift](https://github.com/yoon-chan-hyeok/temporal-rag-drift)

DB 업데이트 이후 새로 발생한 RAG 성능 저하를 정답 라벨 없이 먼저 찾고, evidence intervention으로 retrieval coverage, ranking, context complexity와 evidence utilization 중 조사할 구간을 좁혔습니다.

미래 질문 186건으로 구성한 question-disjoint 평가에서 detector를 다시 맞추지 않고 AUROC `0.854`, Recall `0.714`, F1 `0.615`, Risk lift `3.59×`를 기록했습니다. 탐지된 사례는 P1-P5 probe로 다시 실행해 최초 복구 지점을 진단 가설로 제공합니다.

[Methods](https://github.com/yoon-chan-hyeok/temporal-rag-drift/blob/main/docs/METHODS.md) · [Results](https://github.com/yoon-chan-hyeok/temporal-rag-drift/blob/main/docs/RESULTS.md) · [Reproduction](https://github.com/yoon-chan-hyeok/temporal-rag-drift/blob/main/docs/REPRODUCIBILITY.md)

`Python` · `Retrieval` · `Embeddings` · `NLI` · `Temporal evaluation`

### [TSR-Loc: Multi-Agent Failure Localization](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization)

Task의 성공 조건을 먼저 고정하고 execution trace를 시간순으로 검사해, 이후에도 복구되지 않은 가장 이른 오류를 responsible agent와 exact step으로 반환합니다. 별도 fine-tuning 없이 requirement compiler와 temporal localizer를 분리했습니다.

Who&When 184개 trajectory에서 task-only TSR-Loc의 exact-step accuracy는 `38.59%`였습니다. Direct 방식의 `8.15%`와 비교해 `30.43%p` 높았으며, paired McNemar 검정과 factorial experiment로 비교 범위를 따로 확인했습니다.

[Method](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization/blob/main/docs/METHOD.md) · [Evaluation](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization/blob/main/docs/DATA_AND_EVALUATION.md) · [Experiment history](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization/blob/main/docs/EXPERIMENT_HISTORY.md)

`Python` · `Execution trace` · `Failure attribution` · `Statistical evaluation`

### [Label-Free OCR Quality Monitor](https://github.com/yoon-chan-hyeok/ocr-quality-monitoring)

정답 transcription이 도착하기 전에 OCR embedding의 record-level anomaly와 batch-level distribution shift를 계산합니다. 결과를 자동 판정으로 포장하지 않고 사람이 먼저 확인할 review queue로 정렬했습니다.

설치 가능한 CLI, JSONL 입출력, Markdown report, 실행 hash, synthetic fixture와 CI 테스트를 포함해 작은 운영 도구로 구성했습니다.

`Python` · `Nearest-neighbor drift` · `RBF-MMD` · `CLI` · `CI`

### [Face Attendance System](https://github.com/yoon-chan-hyeok/face-attendance-system)

RetinaFace와 ArcFace를 multi-frame enrollment, ambiguity rejection, FastAPI·MariaDB·React 출결 흐름으로 연결했습니다. top-1 similarity만 사용하지 않고 threshold와 top-2 margin을 함께 적용했으며, 생체정보와 운영 설정은 공개 범위에서 제외했습니다.

`Computer vision` · `FastAPI` · `MariaDB` · `React` · `Decision rule`

### [Event Traffic Delay Analysis](https://github.com/yoon-chan-hyeok/event-traffic-delay-analysis)

OD, 생활인구, 버스와 GIS 데이터를 결합해 행사 종료 뒤의 수요 집중을 분석한 졸업 연구입니다. 분석 결과를 공덕·당산·노량진 환승거점과 좌석, 차량, 회전수, 비용을 포함한 셔틀 운영 시나리오로 변환했습니다.

`Python` · `GIS` · `Multi-source data` · `Demand and capacity scenario`

## 문제를 푸는 방식

실제 배포 환경에서 입력이 어떻게 달라지고 누가 결과를 사용할지 먼저 봅니다. 비슷한 사례와 기존 방법을 조사한 뒤 핵심 가설만 확인할 수 있는 목업을 만듭니다. 이 단계에서 가능성이 확인되면 baseline, 평가 기준과 실패 조건을 고정하고 상세 구현으로 넘어갑니다.

결과가 기대와 다르면 평균 점수에 머물지 않고 실패 사례를 데이터 조건과 실행 단계로 나눕니다. 새로 알게 된 내용은 다음 실험에 반영하고, 확인하지 못한 부분은 한계와 추가 검증 항목으로 남깁니다.

## 기술

- AI/ML: retrieval, embeddings, NLI, semantic uncertainty, computer vision
- Evaluation: temporal split, frozen transfer, baseline and ablation, paired significance test
- Engineering: Python, FastAPI, SQLAlchemy, MariaDB, React, TypeScript, CLI, CI
- Data: EDA, GIS, multi-source join, demand and capacity analysis

![Yoon Chanhyuk, AI/ML Engineer](assets/portfolio-hero.svg)

<div align="center">

## 윤찬혁 · AI/ML Engineer

AI 시스템에서 새로 발생한 실패를 찾고, 문제가 시작된 단계를 좁히는 평가·모니터링 도구를 만듭니다.

서울과학기술대학교 교통공학 전공

[Portfolio](https://yoon-chan-hyeok.github.io/) · [RAG Failure Detection](https://github.com/yoon-chan-hyeok/temporal-rag-drift) · [Agent Evaluation](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization) · [OCR Monitoring](https://github.com/yoon-chan-hyeok/ocr-quality-monitoring)

</div>

운영에서는 정답이 늦게 도착하거나, 긴 실행 기록에서 원인이 묻히거나, 서로 다른 데이터가 같은 의사결정으로 이어져야 하는 제약이 생깁니다. 저는 이 제약을 먼저 정의하고 측정 가능한 질문으로 바꾼 뒤 구현과 평가를 진행했습니다.

RAG, multi-agent system과 OCR에서는 답변 분포, embedding과 execution trace를 비교 가능한 신호로 구성해 위험 사례와 조사 대상을 좁혔습니다. 교통공학 졸업 연구에서는 OD, 생활·체류인구, 버스와 GIS 데이터를 결합해 분석 결과를 운영 시나리오로 연결했습니다.

아이디어는 작은 목업으로 먼저 확인합니다. 가능성이 보이면 평가 기준을 고정하고 구현을 넓히며, 결과가 예상과 다르면 데이터와 실행 단계를 나눠 다시 진단합니다. 실행 코드에는 테스트, 재현 절차와 해석 한계를 함께 남깁니다.

이 GitHub에는 기존 실험, 수업 프로젝트와 졸업 연구를 공개 가능한 형태로 다시 정리했습니다. 따라서 저장소 생성일이 실제 작업을 시작한 시점과 같지는 않습니다.

## 대표 프로젝트

### [Temporal RAG Failure Detection](https://github.com/yoon-chan-hyeok/temporal-rag-drift)

DB 업데이트 직후에는 모든 질문의 최신 gold answer를 다시 만들기 어렵습니다. 업데이트 전후 RAG의 행동 변화만으로 새롭게 실패했을 가능성이 높은 질문을 탐지하고, evidence intervention으로 먼저 조사할 구간을 좁혔습니다.

Detector를 다시 맞추지 않은 미래 질문 186건 평가에서 AUROC `0.854`, Recall `0.714`, F1 `0.615`, Risk lift `3.59×`를 기록했습니다.

`Python` · `Retrieval` · `Embeddings` · `NLI` · `Temporal evaluation`

### [TSR-Loc: Multi-Agent Failure Localization](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization)

긴 execution trace에서는 마지막 오류만 보거나 이미 복구된 첫 실수를 원인으로 고르기 쉽습니다. Task의 성공 조건을 먼저 고정하고, 이후에도 복구되지 않은 가장 이른 오류를 agent와 exact step으로 찾았습니다.

Who&When 184 trajectories에서 task-only TSR-Loc의 exact-step accuracy는 `38.59%`였습니다. Direct 방식보다 `30.43%p` 높았고, A2P 대비 차이는 통계적으로 유의하지 않았습니다.

`Python` · `Execution trace` · `Failure attribution` · `Statistical evaluation`

### [Label-Free OCR Quality Monitor](https://github.com/yoon-chan-hyeok/ocr-quality-monitoring)

정답 transcription이 늦게 도착하는 동안에는 OCR accuracy를 바로 계산할 수 없습니다. 승인 데이터와 비교한 record anomaly와 batch drift로 먼저 검수할 OCR 결과를 정렬했습니다. 설치 가능한 CLI, JSONL report, run hash와 CI tests를 포함합니다.

`Python` · `Nearest-neighbor drift` · `RBF-MMD` · `CLI` · `CI`

### [Face Attendance System Hardening](https://github.com/yoon-chan-hyeok/face-attendance-system)

기존 얼굴 출결 시스템에서 인식 결과를 바로 기록하면 흐린 등록 이미지와 비슷한 후보 때문에 잘못 승인할 수 있었습니다. 등록·식별·승인 흐름을 분석하고, RetinaFace와 ArcFace 기반 식별에 multi-frame enrollment, ambiguity rejection과 IN/OUT 상태 전환을 보강했습니다.

`Existing system hardening` · `Computer vision` · `FastAPI` · `MariaDB` · `React`

### [Event Traffic Delay Analysis](https://github.com/yoon-chan-hyeok/event-traffic-delay-analysis)

행사 혼잡 수치만으로는 언제, 어느 방향에, 어느 규모로 공급할지 결정하기 어렵습니다. OD, 생활·체류인구, 버스와 GIS 데이터를 결합하고 isotonic regression으로 지체의 단조 관계를 반영해, 공덕·당산·노량진 환승거점과 수송 용량·비용 시나리오를 만들었습니다.

`Python` · `GIS` · `Multi-source data` · `Demand and capacity analysis`

## 기술

- AI/ML: retrieval, embeddings, NLI, semantic uncertainty, computer vision
- Evaluation: temporal split, frozen transfer, baseline and ablation, paired significance test
- Engineering: Python, FastAPI, SQLAlchemy, MariaDB, React, TypeScript, CLI, CI
- Data: EDA, GIS, multi-source join, distribution shift, isotonic regression, demand and capacity analysis

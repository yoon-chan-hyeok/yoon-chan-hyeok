![Yoon Chanhyuk, AI/ML Engineer](assets/portfolio-hero.svg)

<div align="center">

## 윤찬혁 · AI/ML Engineer

AI 시스템의 성능 저하를 찾고, 실패가 시작된 단계를 좁히는 평가·모니터링 도구를 만듭니다.

서울과학기술대학교 교통공학 전공

[Portfolio](https://yoon-chan-hyeok.github.io/) · [RAG Monitoring](https://github.com/yoon-chan-hyeok/temporal-rag-drift) · [Agent Evaluation](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization) · [OCR Monitoring](https://github.com/yoon-chan-hyeok/ocr-quality-monitoring)

</div>

RAG, multi-agent system과 OCR처럼 여러 단계가 연결된 AI 시스템을 다뤘습니다. 평균 성능만 보고 끝내지 않고 어떤 입력이 새로 위험해졌는지, 오류가 어느 단계에서 시작됐는지, 사람이 무엇을 먼저 확인해야 하는지까지 연결합니다.

아이디어는 작은 목업으로 먼저 확인합니다. 가능성이 보이면 평가 기준을 고정하고 구현을 넓히며, 결과가 예상과 다르면 데이터와 실행 단계를 나눠 다시 진단합니다. 실행 코드에는 테스트, 재현 절차와 해석 한계를 함께 남깁니다.

## 대표 프로젝트

### [Temporal RAG Drift](https://github.com/yoon-chan-hyeok/temporal-rag-drift)

DB 업데이트 이후 새로 위험해진 RAG 질문을 정답 라벨 없이 우선순위화하고, evidence intervention으로 조사할 실패 구간을 좁혔습니다.

Detector를 다시 맞추지 않은 미래 질문 186건 평가에서 AUROC `0.854`, Recall `0.714`, F1 `0.615`, Risk lift `3.59×`를 기록했습니다.

`Python` · `Retrieval` · `Embeddings` · `NLI` · `Temporal evaluation`

### [TSR-Loc: Multi-Agent Failure Localization](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization)

Task의 성공 조건을 먼저 고정하고 execution trace에서 이후에도 복구되지 않은 가장 이른 오류를 agent와 exact step으로 찾습니다.

Who&When 184 trajectories에서 task-only TSR-Loc의 exact-step accuracy는 `38.59%`였습니다. Direct 방식보다 `30.43%p` 높았고, A2P 대비 차이는 통계적으로 유의하지 않았습니다.

`Python` · `Execution trace` · `Failure attribution` · `Statistical evaluation`

### [Label-Free OCR Quality Monitor](https://github.com/yoon-chan-hyeok/ocr-quality-monitoring)

정답 transcription이 도착하기 전에 record anomaly와 batch drift를 계산하고 먼저 검수할 OCR 결과를 정렬합니다. 설치 가능한 CLI, JSONL report, run hash와 CI tests를 포함합니다.

`Python` · `Nearest-neighbor drift` · `RBF-MMD` · `CLI` · `CI`

### [Face Attendance System](https://github.com/yoon-chan-hyeok/face-attendance-system)

RetinaFace와 ArcFace를 multi-frame enrollment, ambiguity rejection과 출결 기록으로 연결한 설계 case study입니다. 공개 저장소에는 실제 생체정보와 application source snapshot이 포함되지 않습니다.

`Computer vision` · `FastAPI` · `MariaDB` · `React` · `Decision rule`

### [Event Traffic Delay Analysis](https://github.com/yoon-chan-hyeok/event-traffic-delay-analysis)

OD, 생활인구, 버스와 GIS 데이터를 결합해 행사 종료 뒤 수요 집중을 분석한 졸업 연구입니다. 결과를 공덕·당산·노량진 환승거점과 수송 용량·비용을 포함한 운영 시나리오로 연결했습니다.

`Python` · `GIS` · `Multi-source data` · `Demand and capacity analysis`

## 기술

- AI/ML: retrieval, embeddings, NLI, semantic uncertainty, computer vision
- Evaluation: temporal split, frozen transfer, baseline and ablation, paired significance test
- Engineering: Python, FastAPI, SQLAlchemy, MariaDB, React, TypeScript, CLI, CI
- Data: EDA, GIS, multi-source join, demand and capacity analysis

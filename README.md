# 윤찬혁 | Applied AI & AI Reliability

AI 시스템을 만드는 것에서 멈추지 않고, **지식·데이터·실행 흐름이 바뀔 때 실패를 어떻게 발견하고 설명할지**를 탐구합니다.

서울시립대학교에서 교통공학과 인공지능을 함께 공부했으며, 문제 정의부터 데이터 분석, 실험 설계, 프로토타입 구현, 결과 검증까지 주도적으로 수행해 왔습니다.

## Focus

- RAG knowledge update 이후의 품질 변화와 위험 탐지
- Multi-agent trace의 책임 agent·결정적 실패 단계 추적
- 라벨이 부족한 환경의 AI 품질 모니터링
- 교통·공간 데이터를 이용한 운영 의사결정
- 모델과 웹·DB를 연결한 end-to-end AI application

## Selected Projects

| Project | What it demonstrates | Status |
|---|---|---|
| [Temporal RAG Drift Evaluation](https://github.com/yoon-chan-hyeok/temporal-rag-drift) | 지식 스냅샷 간 변화와 유해한 품질 저하 위험을 구분하는 평가 설계 | Research prototype |
| [Multi-Agent Failure Localization](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization) | 긴 agent trace에서 책임 agent와 결정적 step을 찾는 실험 | Experimental research |
| [Face Attendance System](https://github.com/yoon-chan-hyeok/face-attendance-system) | ArcFace·RetinaFace·FastAPI·DB·React를 연결한 실제 동작 프로토타입 | Working prototype |
| [Major-Event Traffic Delay Analysis](https://github.com/yoon-chan-hyeok/event-traffic-delay-analysis) | 다중 교통·공간 데이터 EDA와 행사 운영 시나리오 | Graduation research |
| [Label-Free OCR Quality Monitoring](https://github.com/yoon-chan-hyeok/ocr-quality-monitoring) | 정답 라벨 없이 OCR 품질 위험을 선별하는 모니터링 설계 | Implementation in progress |

## How I Work

1. 평가할 수 있는 질문으로 문제를 다시 정의합니다.
2. 데이터 누수와 비교 기준을 먼저 점검합니다.
3. 평균 점수뿐 아니라 실패 사례와 불확실성을 함께 봅니다.
4. 현재 확인된 사실, 한계, 다음 검증 항목을 분리해 기록합니다.

## Technical Toolbox

`Python` · `FastAPI` · `SQLAlchemy` · `MariaDB` · `React` · `Vite` · `Git`  
`RAG Evaluation` · `Embeddings` · `LLM-as-a-Judge` · `Experimental Design` · `EDA`

## Currently Strengthening

- SQL과 PostgreSQL 기반 데이터 모델링
- 재현 가능한 데이터·평가 파이프라인
- Docker, CI, 자동화 테스트
- tracing, metrics, structured logging을 이용한 observability

## AI-Assisted Development

AI 코딩 도구를 구현과 디버깅에 적극 활용합니다. 문제 정의, 실험 설계, 평가 기준, 결과 해석과 최종 의사결정은 직접 주도하며, 결과물은 테스트와 재현 절차로 검증하는 방향으로 발전시키고 있습니다.


![Yoon Chanhyeok, AI/ML Engineer](assets/portfolio-hero.svg)

<div align="center">

# 윤찬혁 · AI/ML Engineer

실패 사례와 데이터를 따라가며 문제를 다시 정의하고, 필요한 신호와 평가 방법을 설계합니다.

서울시립대학교 교통공학과·인공지능학과 복수전공 · 2026.08 졸업예정

[포트폴리오](https://yoon-chan-hyeok.github.io/) · [이메일](mailto:ych1390@gmail.com)

</div>

## 소개

교통공학과 인공지능을 함께 공부하며, 실제 현상과 AI 시스템의 실패를 데이터로 확인해 왔습니다.

모호한 문제를 확인 가능한 질문으로 바꾸는 데 강점이 있습니다. 처음 세운 가설과 결과가 다르면 원인을 나눠 살피고, 문제를 다시 정의한 뒤 대안을 시험합니다. 멀티에이전트 로그 분할을 성공 명세 기반 추적으로 바꾼 과정과 OCR에서 confidence와 embedding의 역할을 다시 정리한 과정이 이런 방식에서 나왔습니다.

실험이 끝난 뒤에는 코드와 테스트, 실행 방법, 결과를 해석할 수 있는 범위를 함께 정리합니다.

## 대표 프로젝트

| 프로젝트 | 시작한 질문 | 확인할 수 있는 내용 |
|---|---|---|
| [Temporal RAG Failure Detection](https://github.com/yoon-chan-hyeok/temporal-rag-drift) | 지식 DB가 바뀐 직후, 최신 정답지가 없어도 새롭게 위험해진 질문을 먼저 찾을 수 있을까? | 시간 순서를 지킨 탐지기 학습·평가, 미래 업데이트 전이, 근거 개입 실험 |
| [TSR-Loc: Multi-Agent Failure Localization](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization) | 과업의 성공 명세를 trace보다 먼저 만들고 대조하면 실패 위치를 더 정확히 찾을 수 있을까? | 성공 요건 사전 고정, 복구 여부 추적, 책임 agent·earliest step 평가 |
| [Yeouido Festival Mobility Analysis](https://github.com/yoon-chan-hyeok/yeouido-festival-mobility-analysis) | 불꽃축제 뒤 길어진 귀가를 수요 증가만으로 설명할 수 있을까? | SKT OD·체류인구, 버스·지하철, TPSS·GIS를 결합한 이동시간·수요·정차횟수 비교 |
| [OCR Failure Risk Monitoring](https://github.com/yoon-chan-hyeok/ocr-quality-monitoring) | Text log를 embedding space에서 비교하면 gold transcription 없이 failure risk를 찾을 수 있을까? | Nearest-neighbor distance, centroid·MMD batch drift, confidence 비교와 한계 |
| [Face Attendance System](https://github.com/yoon-chan-hyeok/face-attendance-system) | 기존 얼굴 출결 시스템의 오승인과 느린 다중 프레임 처리를 어떻게 줄일 수 있을까? | 다중 프레임 등록, 후보 재정렬, 판정 여유값, 다중 얼굴 중복 처리 |

각 저장소에는 결과만 적지 않았습니다. 왜 그 문제를 골랐는지, 무엇이 예상과 달랐는지, 어떤 판단으로 방법을 바꿨는지까지 정리했습니다.

## 일하는 방식

1. 실제 현상이나 실패 사례에서 질문을 찾습니다.
2. 선행 사례를 살펴보고 작은 실험으로 가설이 움직이는지 먼저 확인합니다.
3. 비교 기준을 정한 뒤 구현과 실험 범위를 넓힙니다.
4. 결과가 예상과 다르면 데이터, 지표, 실행 과정을 나눠 다시 봅니다.

## 경험

- **지능형빅데이터 연구실 · 2026.03부터 약 6개월**: Temporal RAG, 멀티에이전트 실패 추적, OCR 품질 모니터링과 얼굴 출결 시스템 고도화를 진행했습니다.
- **교통공학과 연구인턴 · 2025년 여름 6주**: 교차로 CCTV 시뮬레이션 영상에서 차량을 탐지하고 추적해 이동 궤적을 추출하는 실험을 했습니다.
- **교통공학과 학생회 사무국**: 예산 안에서 행사를 계획하고 현장 비용, 역할 조율과 인수인계 문서를 관리했습니다.
- **자격·수상**: ADsP, SQLD, 교내 데이터 분석 프로젝트 우수상, 교통영향평가협회장상

## 기술

- **AI·ML**: PyTorch, scikit-learn, RAG, 임베딩, NLI, 분포 변화 탐지, 통계 검정
- **데이터**: Python, pandas, NumPy, SQL, GIS, 시계열·공간 데이터 결합
- **구현**: FastAPI, SQLAlchemy, MariaDB, React, TypeScript, CLI, 자동화 테스트, GitHub Actions

프로젝트나 채용 관련 연락은 [ych1390@gmail.com](mailto:ych1390@gmail.com)으로 부탁드립니다.

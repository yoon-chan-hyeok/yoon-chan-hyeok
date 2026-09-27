# 윤찬혁 · AI/ML Engineer

교통공학과 인공지능을 함께 공부하며, 데이터를 분석하고 AI 시스템을 구현해 왔습니다. 최근에는 RAG와 멀티에이전트 시스템이 실패한 상황을 찾아내고, 다음에 무엇을 점검할지 좁히는 평가 방법을 연구했습니다.

서울시립대학교 교통공학과·인공지능학과 복수전공 · **2026.08 졸업**

[포트폴리오](https://yoon-chan-hyeok.github.io/) · [ych1390@gmail.com](mailto:ych1390@gmail.com)

## 대표 프로젝트

| 프로젝트 | 무엇을 했는가 |
|---|---|
| [Temporal RAG Failure Detection](https://github.com/yoon-chan-hyeok/temporal-rag-drift) | DB 업데이트 전후 답변 변화를 비교해 검수가 필요한 질문을 찾고, 근거 개입 실험으로 점검할 RAG 단계를 좁혔습니다. |
| [Multi-Agent Failure Localization · TSR-Loc](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization) | 과업 성공 조건을 먼저 만든 뒤 실행 로그와 대조해, 복구되지 않은 오류의 에이전트와 단계를 찾았습니다. |
| [Yeouido Festival Mobility Analysis](https://github.com/yoon-chan-hyeok/yeouido-festival-mobility-analysis) | 불꽃축제 귀가 교통을 수요·운행·이동시간으로 분석하고, 외곽 환승거점 셔틀을 제안했습니다. |
| [OCR Failure Risk Monitoring](https://github.com/yoon-chan-hyeok/ocr-quality-monitoring) | 규제 문서를 RAG에 넣기 전 검수할 상황을 가정해 confidence와 텍스트 임베딩을 비교하고, 임베딩이 보완하는 오류와 놓치는 오류를 구분했습니다. |
| [Face Attendance System Upgrade](https://github.com/yoon-chan-hyeok/face-attendance-system) | 기존 시스템의 오승인 사례를 바탕으로 다중 샘플 등록과 후보 간 margin 판정, 재촬영 흐름을 보완했습니다. |

## 일하는 방식

실제로 사용할 상황을 먼저 생각합니다. 선행 사례를 살펴보고 작은 목업이나 실험으로 가설을 확인한 뒤 구현 범위를 넓히는 편입니다. 결과가 예상과 다르면 데이터와 평가 기준, 실행 과정을 나눠 다시 봅니다.

교통 분석에서는 단위가 다른 자료를 시간·공간 기준에 맞추고 평상시와 비교했습니다. OCR 실험에서는 confidence가 예상보다 강해, 임베딩의 역할을 대체재에서 보조 신호로 좁혔습니다. 방법을 고를 때는 결과가 좋은 조건뿐 아니라 놓치는 경우도 함께 봅니다.

## 경험

- **지능형빅데이터 연구실 · 2026년 연구 경험:** Temporal RAG, 멀티에이전트 실패 추적, OCR 품질 모니터링과 얼굴 출결 시스템 고도화
- **교통공학과 연구인턴 · 2025년 여름 6주:** 교차로 CCTV 시뮬레이션 영상의 차량 탐지·추적과 이동 궤적 추출 실험
- **교통공학과 학생회 사무국:** 행사 예산·현장 비용 관리, 역할 조율과 인수인계
- **자격·수상:** ADsP, SQLD, 교내 데이터 분석 프로젝트 우수상, 교통영향평가협회장상

## 사용 기술

- **분석·실험:** Python, SQL, pandas, NumPy, scikit-learn, PyTorch, GIS
- **AI 평가:** RAG, 텍스트 임베딩, NLI, 분포 변화 탐지, 통계 검정
- **시스템 구현:** FastAPI, SQLAlchemy, MariaDB, React, TypeScript, CLI, 자동화 테스트

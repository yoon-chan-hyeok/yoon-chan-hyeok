<div align="center">

# 윤찬혁 · Applied AI Engineer

### AI를 만드는 것에서 끝내지 않고, 실패를 측정하고 원인을 추적합니다.

서울시립대학교 교통공학 × 인공지능  
**RAG Evaluation · Multi-Agent Reliability · AI Monitoring · Data Products**

[![GitHub](https://img.shields.io/badge/GitHub-yoon--chan--hyeok-181717?style=flat-square&logo=github)](https://github.com/yoon-chan-hyeok)

</div>

---

## Featured Work

### 01 · [Temporal RAG Drift Evaluation](https://github.com/yoon-chan-hyeok/temporal-rag-drift)

> 지식 업데이트가 RAG 답변을 어떻게 바꾸는지 측정하고, 그 변화가 실제 품질 저하로 이어질 위험을 탐지합니다.

- CLARK 누적 뉴스 스냅샷을 고정한 **temporal transfer evaluation**
- 186개 confirmatory cohort에서 **AUROC 0.854 · F1 0.615 · Risk Lift 3.59×**
- 평가 코드, 6개 테스트 모듈, 집계 결과와 재현 문서를 공개

**Keywords** · Temporal RAG · Drift Detection · Risk Scoring · Evaluation Design

---

### 02 · [Multi-Agent Failure Localization](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization)

> 긴 multi-agent 실행 기록에서 누가, 언제, 어떤 결정으로 최종 실패를 만들었는지 추적합니다.

- Who & When 벤치마크 **184 trajectories** 평가
- task-only 설정 exact-step **38.59%**, direct baseline **8.15%**
- 평가 harness, model backend, 테스트와 GitHub Actions 공개

**Keywords** · Multi-Agent Systems · Trace Analysis · Failure Attribution · LLM Evaluation

---

### 03 · [Face Attendance System](https://github.com/yoon-chan-hyeok/face-attendance-system)

> 얼굴 등록부터 인증·출결 기록·관리 화면까지 연결한 end-to-end AI 애플리케이션입니다.

- RetinaFace + ArcFace 기반 다중 프레임 등록과 품질 필터
- **유사도 임계값 0.68 + 후보 간 margin 0.03**으로 오인식 방어
- FastAPI · SQLAlchemy · MariaDB · React · Vite 통합

**Keywords** · Computer Vision · Face Recognition · API · Database · Frontend

---

### 04 · [Label-Free OCR Quality Monitoring](https://github.com/yoon-chan-hyeok/ocr-quality-monitoring)

> 정답 라벨이 즉시 없는 운영 환경에서 OCR 임베딩 분포의 이상 신호를 조기에 선별합니다.

- nearest-neighbor · robust z-score · centroid distance · RBF-MMD 모니터링
- CLI, 합성 예제, 단위 테스트와 GitHub Actions를 갖춘 실행 가능한 패키지
- 경보를 정답 판정이 아닌 **검토 우선순위 신호**로 설계

**Keywords** · OCR · Data Drift · Unsupervised Monitoring · MMD · CI

---

### 05 · [Major-Event Traffic Delay Analysis](https://github.com/yoon-chan-hyeok/event-traffic-delay-analysis)

> 행사 수요와 교통·공간 데이터를 결합해 혼잡 위험과 운영 대안을 수치화한 졸업 연구입니다.

- 혼잡 관련 상관계수 **0.5864 · 0.5969 · 0.7034**
- 1.3만 명 수요 시나리오의 평균 지연 **0.80 · 1.26 · 1.93분**
- 공덕·당산·노량진 허브와 **45인승 × 100대 × 3회 = 13,500명** 수송안 제시

**Keywords** · Mobility Data · EDA · Scenario Analysis · Decision Support

---

## What I Bring

| 역량 | 작업 방식 | 프로젝트 근거 |
|---|---|---|
| 문제 정의 | 모호한 현상을 측정 가능한 질문과 지표로 바꿉니다. | RAG drift risk, failure localization |
| 평가 설계 | 비교 기준·누수·불확실성을 먼저 확인합니다. | temporal split, baseline/ablation |
| AI 구현 | 모델을 API·DB·UI·CLI와 연결합니다. | face attendance, OCR monitor |
| 데이터 활용 | 여러 데이터의 관계를 운영 시나리오로 번역합니다. | traffic delay analysis |
| 결과 전달 | 성과와 한계, 재현 절차를 함께 공개합니다. | code, tests, CI, result tables |

## Toolbox

**Build**  
`Python` · `FastAPI` · `SQLAlchemy` · `MariaDB` · `React` · `TypeScript`

**AI & Evaluation**  
`RAG Evaluation` · `Embeddings` · `LLM-as-a-Judge` · `Computer Vision` · `Experimental Design` · `Statistical Testing`

**Data & Delivery**  
`EDA` · `Git` · `GitHub Actions` · `Reproducible Experiments`

## How I Work

<div align="center">

### Define → Build → Measure → Diagnose → Improve

문제를 평가 가능한 형태로 정의하고, 빠르게 구현한 뒤, 실패 사례와 불확실성을 근거로 다음 개선을 결정합니다.

</div>

---

<sub>AI 코딩 도구를 구현과 디버깅에 적극 활용합니다. 문제 정의, 실험 설계, 평가 기준, 결과 해석과 최종 의사결정은 직접 주도하며 테스트와 재현 절차로 결과를 검증합니다.</sub>

![Yoon Chanhyeok, AI/ML Engineer](assets/portfolio-hero.svg)

<div align="center">

# 윤찬혁 · AI/ML Engineer

운영 제약이 있는 AI 시스템을 측정 가능한 문제로 바꾸고, 데이터와 실험으로 개선 방향을 검증합니다.

서울시립대학교 교통공학과·인공지능학과 복수전공 · 2026.08 졸업예정

[Portfolio](https://yoon-chan-hyeok.github.io/) · [Email](mailto:ych1390@gmail.com) · [GitHub](https://github.com/yoon-chan-hyeok)

</div>

## 관심 분야

배포된 시스템에서는 정답 label이 늦게 도착하고, 긴 실행 기록에 실패 원인이 묻히며, 서로 다른 출처의 데이터를 하나의 판단 기준으로 묶어야 합니다. 저는 이런 제약을 관찰 가능한 신호와 평가 문제로 바꾸는 작업에 관심이 있습니다.

현재는 RAG, multi-agent system과 OCR의 실패 탐지·진단을 연구하고 있습니다. 교통공학 프로젝트에서는 여러 이동 데이터를 결합해 현상을 설명하고 운영 시나리오로 연결했습니다.

## 핵심 프로젝트

| 프로젝트 | 해결하려 한 문제 | 공개 증거 |
|---|---|---|
| [Temporal RAG Failure Detection](https://github.com/yoon-chan-hyeok/temporal-rag-drift) | DB 업데이트 직후 새 gold label 없이 위험 질문을 우선 탐지하고, intervention으로 먼저 점검할 구간을 좁힙니다. | 코드, 테스트, 파생 결과표, 재현 절차 |
| [TSR-Loc: Multi-Agent Failure Localization](https://github.com/yoon-chan-hyeok/multi-agent-failure-localization) | 긴 execution trace에서 최종 실패로 이어진 최초 미복구 step과 책임 agent를 찾습니다. | 코드, 테스트, 집계 결과, 평가 문서 |
| [OCR Failure Risk Monitoring](https://github.com/yoon-chan-hyeok/ocr-quality-monitoring) | 정답 transcription이 없는 시점에 confidence와 embedding signal로 검수 우선순위를 만듭니다. | 실행 가능한 CLI, 예제, 테스트, 원 실험 범위 문서 |

### 대표 결과

- Temporal RAG: 첫 업데이트에서 모델과 threshold를 고정한 뒤 네 개의 미래 업데이트 341건으로 옮겨 평가했습니다. L2 logistic은 future AUROC `0.883`을 기록했고, 상위 모델 간 차이는 bootstrap 구간이 겹쳐 하나의 모델이 항상 우수하다고 해석하지 않았습니다.
- TSR-Loc: Who&When 184 trajectories에서 exact-step accuracy `38.59%`를 기록했습니다. Direct 방식보다 `30.43%p` 높았지만 A2P와의 차이는 통계적으로 유의하지 않았습니다.
- OCR monitoring: confidence가 강한 baseline임을 확인했고, embedding novelty의 추가 이득은 failure type에 따라 달라졌습니다. 공개 CLI는 원 benchmark 재현 도구가 아니라 baseline과 candidate 사이의 record·batch drift를 점검하는 도구입니다.

## 추가 사례

- [Yeouido Festival Mobility Analysis](https://github.com/yoon-chan-hyeok/yeouido-festival-mobility-analysis): 행사 뒤 귀가 지연을 계기로 SKT OD·체류인구, 버스·지하철 이용 자료, TPSS 정차횟수와 GIS를 결합했습니다. 잘못된 요일 비교와 30분 구간 누락을 바로잡고, 동일 토요일 비교·join audit·공개 집계 재현 절차를 남겼습니다.
- [Face Attendance System Hardening](https://github.com/yoon-chan-hyeok/face-attendance-system): 기존 얼굴 출결 시스템의 오승인 사례를 바탕으로 다중 프레임 등록, 후보 간 margin 판정과 다중 얼굴 중복 처리를 구현했습니다. 전체 애플리케이션 소스는 공개하고 얼굴 이미지·임베딩·접속 정보는 제외했으며, FAR·FRR calibration이 남아 있습니다.

## 일하는 방식

1. 실제 현상과 운영 제약에서 질문을 정의합니다.
2. 선행 사례를 확인하고 작은 목업으로 가설이 움직이는지 봅니다.
3. 평가 기준을 고정한 뒤 구현을 넓힙니다.
4. 결과가 예상과 다르면 데이터, 지표와 실행 단계를 나눠 다시 진단합니다.
5. 코드와 함께 테스트, 재현 절차와 해석 한계를 남깁니다.

## 경험과 기반

- **지능형빅데이터 연구실 · 2026.03부터 약 6개월**: Temporal RAG, multi-agent failure attribution, OCR failure monitoring과 얼굴 출결 시스템 고도화
- **교통공학과 연구인턴 · 2025년 여름 6주**: 교차로 CCTV simulation 영상의 차량 탐지·tracking과 trajectory 추출 실험
- **교통공학과 학생회 사무국**: 행사 예산, 현장 운영, 역할 조율과 인수인계 문서 관리
- **자격·수상**: ADsP, SQLD, 교내 데이터 분석 프로젝트 우수상

## 공개 작업에서 확인할 수 있는 기술

- **AI evaluation**: temporal split, frozen transfer, baseline·ablation, paired significance test
- **ML and data**: PyTorch, scikit-learn, retrieval, embeddings, NLI, pandas, NumPy, SQL, GIS
- **Engineering**: Python package, CLI, automated test, CI, reproducible experiment workflow

연락: [ych1390@gmail.com](mailto:ych1390@gmail.com)

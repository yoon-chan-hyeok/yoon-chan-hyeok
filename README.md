![Yoon Chanhyuk — Applied AI Engineer](assets/portfolio-hero.svg)

<div align="center">

### AI를 “동작하게” 만드는 데서 끝내지 않고, 실패를 측정하고 설명합니다.

서울시립대학교 교통공학 × 인공지능  
**RAG Reliability · Multi-Agent Evaluation · AI Monitoring · Data Products**

[프로젝트 보기](#featured-projects) · [검증된 성과](#proof-over-promises) · [기술 역량](#engineering-toolbox)

</div>

---

## 30-second snapshot

| | |
|---|---|
| **지향점** | AI/ML Engineer · AI Reliability · Applied AI |
| **강점** | 문제 정의 → 프로토타입 → 평가 설계 → 실패 분석 → 문서화 |
| **대표 증거** | RAG drift AUROC **0.854**, multi-agent exact-step **+30.43%p**, 실행 가능한 OCR monitor |
| **작업 방식** | 바이브코딩으로 속도를 확보하고, 지표·테스트·재현 절차로 결과를 검증 |
| **도메인 연결** | AI 연구 문제를 웹·DB·CLI·교통 운영 의사결정까지 확장 |

## Proof over promises

<table>
<tr>
<td width="25%" align="center"><h3>0.854</h3><sub>Temporal RAG<br/>Confirmatory AUROC</sub></td>
<td width="25%" align="center"><h3>+30.43%p</h3><sub>Multi-Agent<br/>Exact-step vs Direct</sub></td>
<td width="25%" align="center"><h3>3.59×</h3><sub>RAG Degradation<br/>Risk Lift</sub></td>
<td width="25%" align="center"><h3>5 Projects</h3><sub>Research · Product<br/>Data · Monitoring</sub></td>
</tr>
</table>

> 수치는 README 장식이 아니라 공개된 결과표·평가 코드·테스트에서 확인할 수 있습니다.

## Featured Projects

<table>
<tr>
<td width="50%" valign="top">
<h3><a href="https://github.com/yoon-chan-hyeok/temporal-rag-drift">01 · Temporal RAG Drift</a></h3>
<p><strong>지식 업데이트 뒤 새로 망가진 질문을 어떻게 찾을까?</strong></p>
<p>누적 뉴스 스냅샷 간 답변 분포 이동과 불확실성을 이용해 품질 저하 위험을 탐지했습니다.</p>
<p><code>AUROC 0.854</code> · <code>F1 0.615</code> · <code>Risk Lift 3.59×</code></p>
<p><sub>Python · RAG Evaluation · Embeddings · NLI · Statistical Testing</sub></p>
</td>
<td width="50%" valign="top">
<h3><a href="https://github.com/yoon-chan-hyeok/multi-agent-failure-localization">02 · Multi-Agent Failure Localization</a></h3>
<p><strong>여러 에이전트 중 누가, 정확히 언제 실패했을까?</strong></p>
<p>작업 요구조건을 먼저 고정하고 긴 trace에서 가장 이른 미복구 오류를 찾는 TSR-Loc을 평가했습니다.</p>
<p><code>184 traces</code> · <code>38.59% exact-step</code> · <code>+30.43%p</code></p>
<p><sub>LLM Evaluation · Trace Analysis · Experiment Harness · CI</sub></p>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<h3><a href="https://github.com/yoon-chan-hyeok/ocr-quality-monitoring">03 · Label-Free OCR Monitor</a></h3>
<p><strong>정답 라벨이 늦게 오는 운영 환경에서 무엇을 먼저 검수할까?</strong></p>
<p>최근접 거리·robust z-score·centroid shift·RBF-MMD를 검토 우선순위로 변환했습니다.</p>
<p><code>CLI</code> · <code>Synthetic demo</code> · <code>Tests</code> · <code>GitHub Actions</code></p>
<p><sub>AI Monitoring · Data Drift · MMD · Python Packaging</sub></p>
</td>
<td width="50%" valign="top">
<h3><a href="https://github.com/yoon-chan-hyeok/face-attendance-system">04 · Face Attendance System</a></h3>
<p><strong>얼굴 인식 결과를 실제 출결 흐름까지 어떻게 연결할까?</strong></p>
<p>RetinaFace·ArcFace, 다중 프레임 등록, threshold+margin 판정, API·DB·UI를 통합했습니다.</p>
<p><code>0.68 threshold</code> · <code>0.03 margin</code> · <code>Full-stack AI</code></p>
<p><sub>Computer Vision · FastAPI · MariaDB · React</sub></p>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<h3><a href="https://github.com/yoon-chan-hyeok/event-traffic-delay-analysis">05 · Event Traffic Delay</a></h3>
<p><strong>대형 행사 혼잡 분석을 실행 가능한 운영안으로 바꿀 수 있을까?</strong></p>
<p>OD·생활인구·버스·GIS 데이터를 결합해 3개 환승거점과 13,500명 셔틀 수송안을 설계했습니다.</p>
<p><code>3 hubs</code> · <code>13,500 capacity</code> · <code>~₩50M</code></p>
<p><sub>Mobility Data · EDA · GIS · Scenario Planning</sub></p>
</td>
<td width="50%" valign="top">
<h3>What connects them?</h3>
<p><strong>모델 점수보다 의사결정 가능한 증거를 만듭니다.</strong></p>
<p>변화를 감지하고, 실패 위치를 설명하고, 사람이 검토할 순서를 만들며, 결과를 제품과 운영 흐름에 연결합니다.</p>
<p><code>Measure</code> → <code>Diagnose</code> → <code>Decide</code></p>
</td>
</tr>
</table>

## Engineering through-line

```mermaid
flowchart LR
    A["Ambiguous problem"] --> B["Measurable question"]
    B --> C["Working prototype"]
    C --> D["Evaluation protocol"]
    D --> E["Failure analysis"]
    E --> F["Product / decision"]
    F -. feedback .-> B
```

## Capability map

| 역량 | 실제로 한 일 | 확인할 프로젝트 |
|---|---|---|
| **AI 평가 설계** | temporal split, frozen transfer, baseline·ablation, paired significance | RAG · Multi-Agent |
| **AI 시스템 구현** | embeddings, retrieval, model backends, CLI, API·DB·UI 연결 | RAG · OCR · Face |
| **실패 분석** | drift risk, exact-step attribution, intervention probe | RAG · Multi-Agent |
| **데이터 의사결정** | 다중 데이터 결합, 시나리오·용량·비용 산정 | Traffic |
| **재현성** | 합성 fixture, 자동 테스트, CI, 결과표, claim boundary | RAG · Multi-Agent · OCR |

## Engineering toolbox

<p>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"/>
<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"/>
<img src="https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white" alt="SQLAlchemy"/>
<img src="https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=mariadb&logoColor=white" alt="MariaDB"/>
<img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React"/>
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript"/>
<img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions"/>
</p>

**AI & Research**  
RAG Evaluation · Embeddings · LLM-as-a-Judge · Computer Vision · Experimental Design · Statistical Testing

**Data & Delivery**  
EDA · GIS · Reproducible Experiments · API Design · Relational Data Modeling · CI

## How I build

<div align="center">

### Define → Build → Measure → Diagnose → Improve

</div>

1. 모호한 요구를 평가 가능한 질문으로 바꿉니다.
2. 빠르게 동작하는 end-to-end 경로를 만듭니다.
3. baseline과 실패 기준을 정하고 수치로 비교합니다.
4. 평균 성능 뒤의 실패 사례와 불확실성을 찾습니다.
5. 코드·테스트·문서·한계를 함께 남깁니다.

## AI-assisted, human-owned

AI 코딩 도구를 구현·탐색·디버깅에 적극 활용합니다.  
**문제 정의, 실험 설계, 비교 기준, 결과 해석, 공개 범위와 최종 의사결정은 직접 책임집니다.**

---

<div align="center">

### 좋은 AI는 높은 점수만 내는 시스템이 아니라, 실패를 발견하고 설명할 수 있는 시스템이라고 생각합니다.

[GitHub에서 작업 보기](https://github.com/yoon-chan-hyeok)

</div>

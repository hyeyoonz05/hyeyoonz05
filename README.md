# Hye Yoon Jeong

**Wireless Communication · Network/System · AI Engineering**

무선통신 시스템의 성능 분석부터 5G 네트워크 환경 구축 및 장애 분석까지 경험했습니다.
MATLAB·Python 기반 알고리즘 연구와 Kubernetes 기반 5G Core 구축을 수행하며,
**성능 수치뿐 아니라 실제 시스템이 안정적으로 동작하는지 검증하는 과정**에 집중해 왔습니다.

## Portfolio

📄 [Portfolio](https://github.com/hyeyoonz05/portfolio)

---

## Featured Projects

### 01. Kubernetes-based 5G Core Fault Analysis

**Kubernetes 환경에서 5G Core 장애를 재현하고 서비스 지표 기반으로 장애 유형과 위치를 분석**

- Open5GS Network Function을 Kubernetes 환경에 배포
- AMF / SMF / UPF / NRF / PCF 장애 재현
- Latency / Packet Loss / Link Down 장애 주입
- NAS, NGAP, SBI, PFCP, GTP-U 및 Link Quality 지표 수집
- XGBoost 기반 장애 유형 및 NF 위치 분류
- Pod 상태뿐 아니라 UE 등록·터널·외부 통신을 기준으로 서비스 복구 검증

**Tech**  
`Kubernetes` `Docker` `Linux` `Open5GS` `UERANSIM` `Python` `XGBoost`

➡️ [View Repository](https://github.com/hyeyoonz05/open5gs-k8s-fault-detection)
---

### 02. GNN-based RIS Control Optimization

**GNN 기반 후보 선별을 통해 RIS의 통신 성능·에너지 효율·연산 효율을 함께 개선한 연구**

- MATLAB 기반 채널, 사용자 간 간섭 및 소비전력 모델링
- RIS 소자 그룹화 및 동적 제어 알고리즘 설계
- Python 기반 GNN으로 15개 제어 후보 중 Top-3 후보 선별
- 선별된 후보에 대해 물리 모델 기반 정밀 평가

**Results**
- Candidate: **15 → 3**
- Runtime: **약 4.2× 향상**
- Energy Efficiency: **19.4% 향상**
- BER: **53.6% 개선**
- Published in **IEEE Access**

**Tech**  
`MATLAB` `Python` `GNN` `RIS` `Wireless Communication`

📄 [View Paper - IEEE Access](https://ieeexplore.ieee.org/document/11611896)

---

### 03. AI-based 3GPP Standard Document Analysis

**대규모 3GPP 표준 문서 검토 시간을 줄이기 위한 검색·분석 파이프라인**

**Problem**
RAN1 관련 문서를 사람이 직접 검토하면 많은 시간이 필요하며, Embedding 검색만 사용할 경우 3GPP 고유 용어나 문서 제목을 놓치는 문제가 있었습니다.

**What I Did**

* 3GPP 표준 및 TDoc 기반 검색·분석 파이프라인 구축
* Embedding 검색과 BM25를 결합한 Hybrid Retrieval 설계
* 검색 결과를 대상으로 관련 문서 Recall 및 검토 대상 감소율 평가
* 검색된 문서를 LLM이 근거 중심으로 분석하도록 구성

**Result**

* 1,504개 TDoc 중 상위 200개 검토 시 관련 문서 **153/156개 검색**
* Recall **98.1%**
* 전체 문서 대비 검토 대상 약 **86.7% 감소**
* AI를 단순 답변 생성이 아닌 **기술 문서 탐색 및 검토 효율화 도구**로 활용

🔗 [3GPP RAG Chatbot](https://github.com/hyeyoonz05/3gpp-rag-chatbot)

**Tech Stack**
`Python` `RAG` `BM25` `Embedding` `LLM` `3GPP`

---

## Engineering Skills

### Network / System

`Linux` `Kubernetes` `Docker` `Open5GS` `UERANSIM`
5G Core 구축 · 장애 재현 · 로그 및 네트워크 지표 분석 · 서비스 정상 여부 검증

### Wireless Communication

`5G NR` `OFDM` `RIS` `MATLAB`
무선 채널 모델링 · BER 분석 · 간섭 분석 · 알고리즘 성능 및 연산량 검증

### AI / Data

`Python` `XGBoost` `GNN` `RAG` `BM25`
분류 모델 구축 · Feature 분석 · 검색 시스템 설계 · 모델 성능 평가

---

## Research Experience

**M.S. in Wireless Communication**

* RIS 기반 무선통신 시스템의 Energy Efficiency 개선
* GNN 기반 RIS 제어 후보 선별 알고리즘 개발
* 5G / 6G 및 3GPP 표준 기술 분석
* Kubernetes 기반 5G Core 장애 분석 프로젝트

**Publication**

* IEEE Access — RIS Energy Efficiency Research
* IEEE Access — RAN Slicing / Cell-Free Massive MIMO Research

---

## What I Focus On

**Performance → Implementation → Validation**

알고리즘의 성능 수치만 확인하는 데 그치지 않고,
실제 환경에서 **어떻게 구현되고, 어떤 조건에서 문제가 발생하며, 정상 동작을 어떻게 검증할 것인지**까지 고민하는 엔지니어를 지향합니다.

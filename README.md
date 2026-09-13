# Hye Yoon Jeong

**Wireless Communication · Network/System · AI Engineering**

무선통신 시스템의 성능 분석부터 5G 네트워크 환경 구축 및 장애 분석까지 경험했습니다.
MATLAB·Python 기반 알고리즘 연구와 Kubernetes 기반 5G Core 구축을 수행하며,
**성능 수치뿐 아니라 실제 시스템이 안정적으로 동작하는지 검증하는 과정**에 집중해 왔습니다.

---

## Featured Projects

### 01. Kubernetes-based 5G Core Fault Analysis

**5G Core 장애를 재현하고 서비스 지표 기반으로 장애 유형과 위치를 분석한 프로젝트**

**Problem**
Kubernetes에서 Pod가 `Running` 상태이더라도 UE 등록과 데이터 통신 등 실제 5G 서비스가 정상적으로 동작한다고 볼 수 없는 문제가 있었습니다.

**What I Did**

* Open5GS Network Function을 컨테이너화하여 Kubernetes 환경에 배포
* AMF / SMF / UPF / NRF / PCF 장애 환경 구성
* Network Latency / Packet Loss / Link Down 장애 주입
* UERANSIM 기반 UE Registration 및 데이터 통신 검증
* NAS, NGAP/SCTP, SBI, PFCP, GTP-U, RTT, Loss, Jitter 등 서비스 지표 수집
* XGBoost 기반 정상/장애, 장애 유형 및 NF 위치 분류

**Result**

* NORMAL / FAULT 분류 정확도 약 **100%**
* Fault Family 분류 정확도 약 **99.7%**
* NF Location 분류 정확도 약 **99%**
* 장애 복구 시 Pod 상태가 아닌 **UE 등록·터널 생성·외부 통신까지 확인하는 검증 절차 구축**

**Tech Stack**
`Kubernetes` `Docker` `Linux` `Open5GS` `UERANSIM` `Python` `XGBoost`

---

### 02. GNN-based RIS Control Optimization

**통신 성능을 유지하면서 RIS 제어 연산량과 에너지 효율을 개선한 연구**

**Problem**
RIS 제어 후보를 매 시간 구간마다 모두 평가하면 높은 통신 성능을 얻을 수 있지만, 후보 수 증가에 따라 연산 부담과 소비전력이 증가하는 문제가 있었습니다.

**What I Did**

* MATLAB 기반 무선 채널, 사용자 간 간섭 및 소비전력 모델링
* RIS 소자 그룹화를 통한 제어 후보 구성
* Python 기반 GNN을 활용하여 유망한 후보를 Top-k로 사전 선별
* 선별된 후보에 대해서만 물리 모델 기반 정밀 평가 수행
* SNR과 채널 환경 변화에 따른 BER, Energy Efficiency 및 실행시간 분석

**Result**

* 제어 후보 **15개 → 3개**로 축소
* Exhaustive Search 대비 실행시간 약 **4.2배 개선**
* Always-On RIS 대비 Energy Efficiency **19.4% 개선**
* BER **53.6% 개선**
* 연구 결과 SCI급 저널 게재 및 국제학술대회 발표

**Tech Stack**
`MATLAB` `Python` `GNN` `Wireless Communication` `RIS`

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

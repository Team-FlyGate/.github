<p align="center">
  <img src="https://raw.githubusercontent.com/Team-FlyGate/.github/main/profile/assets/flygate-hero_v2.0.0.png" alt="FlyGate — Evidence before inference. FlyDiscovery와 FlyVigilance를 잇는 근거 검증" width="100%">
</p>

<p align="center"><strong>신약 후보 탐색부터 시판 후 약물감시까지, 판단이 근거를 넘지 않도록.</strong></p>
<p align="center">NVIDIA Korea Agentic AI Hackathon 2026 · Team FlyGate</p>

<p align="center">
  <a href="https://github.com/Team-FlyGate/Project-FlyGate"><strong>메인 제출 저장소 ↗</strong></a>
  &nbsp; · &nbsp;
  <a href="https://github.com/Team-FlyGate/Project-FlyGate/tree/main/fly_discovery">FlyDiscovery</a>
  &nbsp; · &nbsp;
  <a href="https://github.com/Team-FlyGate/Project-FlyGate#flyvigilance">FlyVigilance</a>
  &nbsp; · &nbsp;
  <a href="https://github.com/Team-FlyGate/Project-FlyGate/blob/main/docs/EVALUATION.md">평가 보고서</a>
</p>

---

## 01 / Two perspectives. One evidence trail.

**FlyGate**는 **FlyDiscovery**와 **FlyVigilance**로 구성됩니다. 후보물질의 구조·결합 근거와 시판 후 안전성 근거를 살피고, AI가 내놓은 주장이 원자료로 뒷받침되는지 검토합니다.

<p align="center"><img src="https://raw.githubusercontent.com/Team-FlyGate/.github/main/profile/assets/flygate-modules_v2.0.0.png" width="100%" alt="FlyDiscovery: 구조와 결합 근거. FlyVigilance: 보고와 안전성 검토."></p>
<p align="center"><sub>두 모듈의 역할을 표현한 AI 생성 개념 이미지</sub></p>

<table>
<tr>
<td width="50%" valign="top">

### 01 / FlyDiscovery
**시판 전 · 후보 탐색과 검증**

후보물질을 구조 예측 → 분자 도킹 → 친화도 평가로 따라갑니다. 계산 결과를 실험 구조와 참조 데이터에 대조하고, 근거를 넘는 해석을 검토합니다.

- **구조와 결합:** MSA-Search · OpenFold3 · DiffDock
- **친화도 평가:** Boltz-2 · ChEMBL 참조 데이터
- **주장 검증:** 근거 ID · 원본 수치 · 과잉해석 판정

[탐색 워크벤치와 실행 결과 →](https://github.com/Team-FlyGate/Project-FlyGate/tree/main/fly_discovery)

</td>
<td width="50%" valign="top">

### 02 / FlyVigilance
**시판 후 · 약물감시와 검토 배분**

이상사례 보고, 허가 라벨, 문헌을 연결합니다. 규칙과 통계로 선별한 뒤 필요한 사례를 모델의 심층 검토와 사람의 검토로 보냅니다.

- **근거 조회:** FDA FAERS · openFDA · PubMed
- **판단과 검토:** Jev · NVIDIA Nemotron · Safety Guard
- **국내 보고:** 사례 구조화 · 인과성 평가 보조

[약물감시 구조와 평가 결과 →](https://github.com/Team-FlyGate/Project-FlyGate/blob/main/README.md)

</td>
</tr>
</table>

## 02 / Inside the workbench

<a href="https://flyvigilance.vercel.app"><img src="https://raw.githubusercontent.com/Team-FlyGate/.github/main/profile/assets/flyvigilance-screen_v2.0.0.png" width="100%" alt="FlyVigilance 관제 화면: 신경 연결 지도와 이상사례 검토 흐름"></a>

**[FlyVigilance 데모 열기 ↗](https://flyvigilance.vercel.app)** · [FlyDiscovery 코드와 실행 기록 ↗](https://github.com/Team-FlyGate/Project-FlyGate/tree/main/fly_discovery)

<sub>실제 프로젝트의 관제 화면입니다. 표시된 수치는 해당 화면을 기록한 시점의 결과이며, 평가 범위와 한계는 평가 문서를 참고하세요.</sub>

## 03 / Evidence before inference.

> **출처와 숫자가 맞아도, 결론이 근거의 범위를 넘으면 다시 검토합니다.**

| 검증 단계 | 확인하는 질문 |
| :--- | :--- |
| **01 · 근거** | 주장을 뒷받침하는 근거 ID와 원자료가 존재하는가? |
| **02 · 수치** | 인용한 숫자가 원본 로그와 계산 결과에 일치하는가? |
| **03 · 해석** | 도구와 데이터가 허용하는 범위 안에서 결론을 내렸는가? |

FlyVigilance는 초파리 신경 연결 지도(connectome)에서 착안한 감각·반사·기억·숙고·행동의 층으로 검토 흐름을 표현합니다. 빠른 판단에는 TypeSafe AI의 **Jev**, 심층 검토에는 **NVIDIA Nemotron**, 안전성 점검에는 **Nemotron Safety Guard**를 활용합니다.

## 04 / Meet the team

면역학, 바이오 데이터, 의료영상 AI, 약학, 에이전트 개발의 관점을 하나의 검토 흐름으로 연결합니다.

<table>
<tr>
<td align="center" width="20%"><a href="https://github.com/kakyungkim"><img src="https://avatars.githubusercontent.com/u/84395053?v=4" width="88" alt="Ka-Kyung Kim"><br><strong>김가경</strong><br>Ka-Kyung Kim</a><br><sub>TEAM COORDINATION<br>PV EVIDENCE</sub></td>
<td align="center" width="20%"><a href="https://github.com/AwesomeZun"><img src="https://avatars.githubusercontent.com/u/55944204?v=4" width="88" alt="Seong-Jun Kang"><br><strong>강성준</strong><br>Seong-Jun Kang</a><br><sub>INTEGRATION<br>FLYVIGILANCE</sub></td>
<td align="center" width="20%"><a href="https://github.com/Geongyu"><img src="https://avatars.githubusercontent.com/u/37532168?v=4" width="88" alt="Geon-Gyu LEE"><br><strong>이건규</strong><br>Geon-Gyu LEE</a><br><sub>FLYDISCOVERY<br>AI & INTERFACE</sub></td>
<td align="center" width="20%"><a href="https://github.com/ybaeus"><img src="https://avatars.githubusercontent.com/u/47170687?v=4" width="88" alt="Yeji Bae"><br><strong>배예지</strong><br>Yeji Bae</a><br><sub>AGENT WORKFLOWS<br>PV EXTENSION</sub></td>
<td align="center" width="20%"><a href="https://github.com/YMYDGenie"><img src="https://avatars.githubusercontent.com/u/133306595?v=4" width="88" alt="Eunjin Jeon"><br><strong>전은진</strong><br>Eunjin Jeon</a><br><sub>PHARMACY<br>DOMAIN REVIEW</sub></td>
</tr>
</table>

| Member | Background | Contribution to FlyGate |
| :--- | :--- | :--- |
| **김가경** · [@kakyungkim](https://github.com/kakyungkim) | 바이오 데이터 분석 · 혈중 암세포 및 신약개발 바이오마커 분석 경험 | 팀 조율과 제출 기획 · 약물감시 근거 설계 · 보고서 양식 매핑과 근거 등급 규칙 |
| **강성준, Ph.D.** · [@AwesomeZun](https://github.com/AwesomeZun) · [Website ↗](https://kangseongjun.com) | 면역학 박사 · 단일세포·공간오믹스 · 신약 후보 평가 | FlyVigilance 개발 · 데이터·평가 파이프라인 · 두 모듈 통합과 시각화 · [FDDD](https://github.com/AwesomeZun/FDDD) 개발 — FlyDiscovery의 모티브 |
| **이건규** · [@Geongyu](https://github.com/Geongyu) | AI researcher · 병리·영상의학 및 오믹스를 결합한 예후·약물 반응 예측 | FlyDiscovery 개발 · 탐색 워크벤치와 사용자 인터페이스 개선 |
| **배예지** · [@ybaeus](https://github.com/ybaeus) | 병원 데이터 사이언티스트 · 멀티오믹스·공간·이미지 데이터 | Jev 기반 약물감시 확장 · 문헌 검토 흐름 설계 · 약사 피드백 반영 |
| **전은진** · [@YMYDGenie](https://github.com/YMYDGenie) | 약사 · 약사를 위한 AI 제품 개발 | 약학 관점의 요구사항 검토 · 이상사례·국내 보고 사례 조사 · 워크플로 자문 |

## 05 / Explore the evidence

| 살펴볼 내용 | 바로가기 |
| :--- | :--- |
| **통합 프로젝트** | [Project-FlyGate](https://github.com/Team-FlyGate/Project-FlyGate) |
| **FlyDiscovery 실행 원자료** | [구조·도킹·친화도 측정 기록](https://github.com/Team-FlyGate/Project-FlyGate/tree/main/fly_discovery/measurements) |
| **FlyVigilance 평가** | [평가 방법, 결과와 한계](https://github.com/Team-FlyGate/Project-FlyGate/blob/main/docs/EVALUATION.md) |
| **시스템 구조** | [Architecture](https://github.com/Team-FlyGate/Project-FlyGate/blob/main/docs/ARCHITECTURE.md) |
| **에이전트 스킬** | [Skills](https://github.com/Team-FlyGate/Project-FlyGate/tree/main/skills) |

<details>
<summary><strong>데모와 결과를 읽는 방법</strong></summary>

- FlyDiscovery 웹 화면은 저장된 실행 결과를 보여 주는 데모입니다. 화면을 열 때 새 모델 추론을 실행하지 않습니다.
- 도킹 점수는 약효의 입증이 아니며, 자발적 이상사례 보고의 통계 신호는 인과관계를 확정하지 않습니다.
- 신경 연결 지도 시각화는 에이전트의 처리 흐름을 표현하며 임상적 검증을 뜻하지 않습니다.
- 평가 범위와 실패 사례는 각 모듈의 문서에서 확인할 수 있습니다. 이 프로젝트는 해커톤 연구 데모이며 실제 의료 판단을 대체하지 않습니다.

</details>

---

<p align="center"><strong>FlyDiscovery + FlyVigilance = FlyGate</strong><br><sub>Evidence before inference.</sub></p>
<p align="center"><sub>히어로와 모듈 아트는 AI 생성 개념 이미지입니다. 실제 분자 구조나 임상 데이터를 나타내지 않습니다.</sub></p>

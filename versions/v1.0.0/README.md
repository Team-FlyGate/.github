<p align="center">
  <img src="https://raw.githubusercontent.com/Team-FlyGate/.github/main/profile/assets/flygate-banner_v1.0.0.png" alt="FlyGate — Evidence before inference. FlyDiscovery와 FlyVigilance를 잇는 근거 검증" width="100%">
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

## 하나의 FlyGate, 두 개의 관점

**FlyGate**는 **FlyDiscovery**와 **FlyVigilance**로 구성됩니다. 후보물질의 구조·결합 근거와 시판 후 안전성 근거를 살피고, AI가 내놓은 주장이 원자료로 뒷받침되는지 검토합니다.

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

## 공통 원칙: 근거에서 판단까지

> **출처와 숫자가 맞아도, 결론이 근거의 범위를 넘으면 다시 검토합니다.**

| 검증 단계 | 확인하는 질문 |
| :--- | :--- |
| **01 · 근거** | 주장을 뒷받침하는 근거 ID와 원자료가 존재하는가? |
| **02 · 수치** | 인용한 숫자가 원본 로그와 계산 결과에 일치하는가? |
| **03 · 해석** | 도구와 데이터가 허용하는 범위 안에서 결론을 내렸는가? |

FlyVigilance는 초파리 신경 연결 지도(connectome)에서 착안한 감각·반사·기억·숙고·행동의 층으로 검토 흐름을 표현합니다. 빠른 판단에는 TypeSafe AI의 **Jev**, 심층 검토에는 **NVIDIA Nemotron**, 안전성 점검에는 **Nemotron Safety Guard**를 활용합니다.

## 코드와 근거를 함께 공개합니다

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
<p align="center"><sub>배너는 AI로 생성한 개념 이미지이며 실제 분자 구조나 임상 데이터를 나타내지 않습니다.</sub></p>

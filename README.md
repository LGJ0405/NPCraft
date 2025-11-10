# NPCraft
**게임 도메인 특화 한국어 sLLM 구축 및 개발**  
*– NPC 대사, 퀘스트 시나리오, 이벤트 및 트리거 생성 중심 –*
---

## 개요
본 프로젝트는 게임 도메인(대사·시나리오·이벤트) 특화 sLLM 구축 및 개발을 목표로 진행합니다.

최근 글로벌 게임 시장은 지속적으로 성장하고 있으며, 2024년 기준 한국은 전 세계 4위(약 95억 달러 규모)의 시장을 형성하고 있습니다.

출처: [Newzoo 2024 Global Games Market Report](https://newzoo.com/resources/rankings/top-10-countries-by-game-revenues?utm_source=chatgpt.com), [Grand View Research](https://www.grandviewresearch.com/horizon/outlook/video-game-market/south-korea?utm_source=chatgpt.com)

그러나 대규모 언어모델(LLM)의 발전에도 불구하고,
게임 도메인, 특히 한국어 기반 LLM/sLLM의 실질적 활용은 아직 초기 단계에 머물러 있습니다. <br>
현재까지 NCSOFT의 VARCO 모델이 유일한 사례로 알려져 있으나,
연구용 목적에 한정되어 상용화나 외부 활용에는 제약이 존재합니다.

출처: [KED Global](https://www.kedglobal.com/korean-games/newsView/ked202507110006), [arXiv](https://arxiv.org/html/2507.08924v1)

또한 대부분의 상용 LLM이 영어 중심으로 학습되어 있어
게임 특유의 대화체 문체, 은어, 감정 표현, 캐릭터별 말투를 자연스럽게 반영하기 어렵습니다. <br>
이에 따라 국내 게임 개발 과정에서는 여전히 기획자나 작가의 수작업 의존도가 높고, NPC 대사, 퀘스트 시나리오, 이벤트 텍스트 작성 등의 반복적 작업에서 많은 리소스가 소모되고 있습니다.


NPCraft는 이러한 문제를 해결하기 위해,
- 한국어 게임 도메인 데이터에 특화된 sLLM 구축,
- RAG 기반 캐릭터 일관성 유지,
- 시나리오 자동 생성 및 변형 기능

을 통합적으로 지원하는 콘텐츠 생성 자동화 플랫폼을 목표로 합니다.

---

## 프로젝트 목표

**NPCraft**는 다음 세 가지 핵심 목표를 중심으로 개발됩니다.

1. **한국어 게임 도메인에 특화된 sLLM 구축**  
   - NPC 대사, 퀘스트 시나리오, 이벤트 텍스트 등 게임 내 반복 텍스트 자동 생성  

2. **RAG 기반 캐릭터 일관성 유지**  
   - NPC 설정 문서, 시나리오 데이터를 활용해 캐릭터 말투·성격 일관성 확보  

3. **시나리오 확장 및 변형 자동화**  
   - 기존 스토리라인을 바탕으로 서브 시나리오 및 이벤트 분기 자동 생성  

---

### 환경 구축
```bash
conda create -n npcraft_env python=3.12
conda activate npcraft_env
```
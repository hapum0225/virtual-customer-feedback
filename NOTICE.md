# NOTICE — 이 저장소는 **이중 라이선스**입니다

한 저장소 안에 라이선스가 다른 두 종류의 파일이 들어 있습니다. **쓰기 전에 어느 쪽인지 확인하세요.**

| 구분 | 대상 | 라이선스 | 의무 |
|---|---|---|---|
| **스킬 (규칙·문서·패키징)** | 아래 표 밖의 모든 파일 | **MIT** | 저작권 고지 유지 |
| **페르소나 팩 (데이터)** | `persona-index.md`<br>`persona-cards.md`<br>`sampling-record.md` | **CC BY 4.0** | **출처 표기 필수** (§2) |

세 파일의 정확한 위치는 `plugins/virtual-customer-feedback/skills/virtual-customer-feedback/references/` 입니다.

> **이 문서의 경로 표기 규칙**: 아래에서 `SKILL.md`·`references/…`처럼 짧게 적은 것은 모두
> `plugins/virtual-customer-feedback/skills/virtual-customer-feedback/` 아래를 가리킵니다.

---

## 1. 스킬 부분 — MIT

`Copyright (c) 2026 Ant (hapum0225)` · 전문은 [`LICENSE`](./LICENSE).

이 스킬의 규칙·절차·출력 형식(`SKILL.md`, `references/output-contract.md`, `references/modes.md`, `references/pilot-tests.md`, 인젝션 시험 fixture, 저장소 패키징·문서)은 **새로 작성한 저작물**입니다.

> **아이디어 출처에 대한 자기 선언**: "가상 고객 패널"이라는 **발상**은 제3자 스킬에서 얻었습니다. 그 문서·코드·문장은 사용하지 않았고 규칙은 전부 새로 썼습니다. 다만 이 문장은 **작성자의 진술이며 제3자 대조로 검증되지 않았습니다** — `references/ATTRIBUTION.md` §5·§7과 같은 등급으로 취급하세요.

## 2. 페르소나 팩 — CC BY 4.0 (표기 의무 있음)

페르소나 팩은 NVIDIA가 CC BY 4.0으로 공개한 데이터셋에서 **선별·가공한 파생물**입니다. 이 팩이나 그 개작물을 재배포·공개 사용할 때는 아래 표기를 그대로 붙여야 합니다.

> **Nemotron-Personas-Korea** — Creator: **NVIDIA Corporation** · **© NVIDIA Corporation**
> 원자료: https://huggingface.co/datasets/nvidia/Nemotron-Personas-Korea
> 라이선스: **CC BY 4.0** — https://creativecommons.org/licenses/by/4.0/
> **개작(Changes): Ant가 원자료 100만 레코드에서 40건을 선별하고, 26필드 중 16필드만 남기고, 카드에는 `uuid`를 앞 8자리만 표기하고(전체 UUID는 `sampling-record.md`의 추적 기록에만 남김), 서술문에서 **페르소나 본인의 성명**을 제거해 별칭(P01…)으로 대체하고, 말투·성 역할을 단정하는 특정 표현(`사투리`·`남자다운` 등)이나 민감 건강 낱말이 든 문장을 삭제하고, 목록형 필드를 한 줄로 합쳤습니다. 관심사 등에 등장하는 **제3자 공인의 이름은 원자료 그대로 남아 있습니다.**
> 원자료는 **무보증(as-is)** 제공입니다. NVIDIA의 보증·후원·제휴가 아닙니다.

**스킬이 이 표기를 자동으로 처리합니다** — 매 실행 출력 마지막 줄에 축약 표기 한 줄이 자동으로 붙습니다. 출력을 그대로 공개물에 옮길 때는 위 전문을 크레딧에 넣으세요.

원본 데이터셋의 라이선스가 이 저장소의 MIT보다 **우선합니다.** 위 세 파일을 MIT로 재배포할 수 없습니다.

### CC BY 4.0이 허용하는 것 / 요구하는 것

- **허용**: 복제·배포·개작, **상업적 이용 포함** (데이터셋 카드 원문: 상업·비상업 모두 자유롭게 사용 가능)
- **요구**: 저작자 표시, 라이선스 링크, **변경 사실 명시**
- **금지되지 않음**: 2차적 저작물에 다른 라이선스 적용(ShareAlike 조항 없음). 단 원저작물 부분의 표기 의무는 남습니다.

## 3. 데이터에 대해 확인되지 않은 것 (쓰기 전에 반드시 읽으세요)

`references/ATTRIBUTION.md` §5의 미검증 항목을 여기에 옮깁니다. **이 저장소를 쓰는 사람도 같은 불확실성을 안게 됩니다.**

- **"개인정보(PII)가 없다"는 문장은 데이터셋 카드에 없습니다.** 카드는 "완전히 인공적으로 합성" + "실존 인물과의 유사성은 우연"이라고만 말합니다. 이름은 대법원 실제 이름 통계에 기반해 생성되므로 **실존하는 이름 조합이 반복 등장합니다.**
- 팩 제작 시 **페르소나 본인의 성명**을 별칭(P01…)으로 치환했지만, **치환 기준은 `[가-힣]{2,4} 씨` 정규식**입니다. 그 형태가 아닌 인명은 **미검사**입니다.
- 카드 본문에는 **시군구 이하 지명**(동·마을·신도시 이름)이 남아 있습니다. 스킬의 출력 규칙이 시도 단위까지만 쓰도록 막지만, **파일 자체에는 남아 있습니다.**
- 2026-08-06 이후 **원본 데이터셋이 갱신됐는지 확인하는 수단을 두지 않았습니다.**

### 확인된 사실이지만 알고 써야 하는 것 (위와 등급이 다릅니다 — 이건 확인됐습니다)

- **관심사·취미 서술에 나오는 제3자 공인의 이름은 원자료 그대로 남아 있습니다** — 페르소나 본인의 신원이 아니라서 치환 대상이 아니었습니다. 공개물에 팩 내용을 옮기면 함께 노출됩니다.
- **별칭화는 익명화가 아닙니다** — `sampling-record.md`에 **32자리 UUID 40개가 그대로** 있어 원본 레코드를 조회할 수 있습니다(카드에만 앞 8자리로 줄여 표기). 그래서 스킬은 로그 기록 줄에 UUID를 적지 않습니다.
- 성명 치환 정규식이 **1건을 오검출**해 일반 명사구를 별칭으로 바꿨던 것을 공개 전 감사에서 발견해 고쳤습니다(`sampling-record.md` §6-1). 실제 성명 치환은 40건입니다.

## 4. 데이터셋 자체의 한계 (NVIDIA 카드가 스스로 밝힌 것)

- **만 19세 이상 성인만** 포함 — 미성년 고객은 이 팩으로 다룰 수 없습니다.
- 세부 직업 배정 시 성별·소득·학력·전공이 **독립적으로** 영향을 준다고 가정했고, **요인 간 교호작용(예: 성별×전공)은 반영되지 않았습니다.**
- 생물학적 성과 구분되는 젠더는 국내 공공 통계 부재로 반영 불가.
- 한국 인구 분포 기준입니다 — 해외 고객에는 쓸 수 없습니다.

## 5. 인용 (학술·문서용)

```bibtex
@software{nvidia_nemotron_personas_korea,
  author = {Kim, Hyunwoo and Ryu, Jihyeon and Lee, Jinho and Ryu, Hyungon and Praveen, Kiran
            and Prayaga, Shyamala and Thadaka, Kirit and Jennings, Will and Sadeghi, Bardiya
            and Sharabiani, Ashton and Choi, Yejin and Meyer, Yev},
  title  = {Nemotron-Personas-Korea: Synthetic Personas Aligned to Real-World Distributions for Korea},
  month  = {April}, year = {2026},
  url    = {https://huggingface.co/datasets/nvidia/Nemotron-Personas-Korea}
}
```

## 6. 무보증

이 저장소는 무보증(as-is)으로 제공됩니다. **이 스킬의 출력은 가상 결과이며 실제 고객 근거가 아닙니다.** 출력을 근거로 한 사업 결정의 책임은 사용자에게 있습니다 — 그래서 스킬 자체가 그런 결정을 거부하도록 설계돼 있습니다(`SKILL.md` §3).

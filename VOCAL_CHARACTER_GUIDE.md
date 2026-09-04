# VOCAL CHARACTER GUIDE — 2026 AUTUMN

## 1. 목적

이 문서는 2026 가을 프로젝트의 보컬 다양성을 관리하기 위한 프로젝트 전용 지침입니다.

기존 `Vocal` 필드의 `Female / Male / Duet` 구분은 유지합니다.

이 프로젝트에서는 보컬을 `Warm Airy Female`, `Smoky Male` 같은 고정 완제품 프로필로만 분류하지 않습니다. 실제 보컬은 여러 특성이 동시에 존재할 수 있으므로, 보컬 캐릭터를 여러 축의 조합으로 설계합니다.

예:

- `husky + soulful`
- `soft + smoky`
- `warm + husky + soulful`
- `airy + fragile + intimate`
- `clear + rhythmic + bright`

따라서 `husky`와 `soulful`, `soft`와 `smoky`는 서로 배타적인 유형이 아닙니다.

## 2. 기본 구조

보컬 설계는 다음 순서로 봅니다.

`Vocal Type + Timbre + Weight + Register + Delivery + Expression + Technique + Role`

모든 축을 반드시 채울 필요는 없습니다. 곡에 필요한 정보만 선택합니다.

공통 `CORE_RULES.md`의 "권장 보컬 특성 중 곡마다 1~2개만 선택" 원칙은 이 프로젝트에서도 유지합니다. 다만 여기서 1~2개는 핵심 음색/표현 특성을 뜻하며, `mid-register`, `close-mic`, `female lead` 같은 기능적 설명까지 모두 같은 수식어 개수로 계산하지 않습니다.

Style Prompt가 수식어 나열문이 되지 않도록 핵심 캐릭터는 명확하게 유지합니다.

## 3. Vocal Type

기존 MASTER BOARD의 보컬 비율 관리용 필드입니다.

- `Female`
- `Male`
- `Duet`

`Vocal Type`과 실제 보컬 캐릭터는 별개로 관리합니다.

예:

- `Female` + `husky / soulful / low-mid / intimate`
- `Female` + `clear / light / high / rhythmic`

둘은 같은 Female이지만 다른 보컬 캐릭터입니다.

## 4. Vocal Character Matrix

### A. Timbre — 음색 / 질감

곡당 보통 1개를 중심으로 사용하고, 필요한 경우 보조 특성 1개를 추가합니다.

- `warm` — 따뜻하고 둥근 질감
- `clear` — 맑고 선명함
- `husky` — 숨과 거친 결이 섞인 질감
- `smoky` — 어둡고 흐릿한 질감
- `velvety` — 부드럽고 매끄러운 질감
- `airy` — 공기감이 있는 가벼운 질감
- `raspy` — 거칠고 긁히는 결
- `crisp` — 발음과 어택이 또렷한 질감
- `earthy` — 꾸밈이 적고 자연스러운 질감
- `silky` — 밝고 매끈하게 흐르는 질감

### B. Weight — 보컬 무게 / 밀도

- `soft`
- `light`
- `gentle`
- `grounded`
- `full`
- `rich`
- `powerful`

`soft`는 음색 자체라기보다 가창 강도와 밀도에 가깝습니다. 따라서 `soft smoky`, `soft husky`, `soft clear`처럼 결합할 수 있습니다.

### C. Register — 중심 음역

- `low`
- `low-mid`
- `mid`
- `mid-high`
- `high`

음역은 성별과 자동으로 연결하지 않습니다.

Female 저음, Male 고음 등도 곡에 맞으면 사용할 수 있습니다.

### D. Delivery — 전달 방식

- `intimate`
- `close-mic`
- `conversational`
- `restrained`
- `relaxed`
- `rhythmic`
- `punchy`
- `floating`
- `soaring`
- `raw`
- `understated`
- `storytelling`

### E. Expression — 감정 표현 방식

- `soulful`
- `fragile`
- `wistful`
- `tender`
- `detached`
- `playful`
- `hopeful`
- `melancholic`
- `confident`
- `vulnerable`
- `calm`

`soulful`은 장르명이 아니라 프레이징과 감정 전달 방식으로 사용할 수 있습니다.

따라서 다음 조합이 모두 가능합니다.

- `husky soulful`
- `velvety soulful`
- `clear soulful`
- `smoky soulful`

### F. Technique — 필요한 경우에만 지정

- `natural breath spacing`
- `restrained vibrato`
- `subtle rasp`
- `smooth phrasing`
- `light falsetto`
- `controlled belting`
- `minimal melisma`
- `crisp articulation`

기법은 곡마다 많이 넣지 않습니다. SUNO가 과장해서 해석할 위험이 있는 요소는 특히 제한합니다.

공통 규칙에 따라 다음은 억제합니다.

- heavy autotune
- exaggerated melisma
- excessive breathiness
- constant high belting
- theatrical whispering
- glossy choir stacks

## 5. 조합 예시

### Female

`Female — warm / husky / low-mid / soulful / intimate`

Style Prompt 확장 예:

`warm husky female vocal, soft low-mid register, soulful phrasing, intimate close-mic delivery`

### Female — 같은 Husky이지만 다른 성격

`Female — husky / full / mid-high / emotional / soaring`

Style Prompt 확장 예:

`husky female vocal, full mid-high register, emotionally expressive phrasing, controlled soaring chorus`

같은 `husky`라도 앞의 보컬과 다른 캐릭터입니다.

### Male

`Male — smoky / soft / low / melancholic / conversational`

Style Prompt 확장 예:

`soft smoky male vocal, low register, melancholic conversational delivery, restrained vibrato`

### Bright Pop

`Female — clear / light / mid-high / rhythmic / confident`

Style Prompt 확장 예:

`clear light female vocal, bright mid-high register, crisp rhythmic phrasing, confident modern pop delivery`

## 6. Duet 설계

Duet은 단순히 `Duet` 하나의 보컬 유형으로 보지 않습니다.

다음 두 요소를 함께 관리합니다.

### A. Voice Contrast

- warm female + clear male
- husky female + soft male
- airy female + smoky male
- clear female + warm baritone male
- similar warm voices
- contrasting low / high registers

### B. Role Configuration

- `Female Lead + Male Harmony`
- `Male Lead + Female Harmony`
- `Alternating Verses`
- `Call and Response`
- `Equal Duet`
- `Unison Chorus`
- `Lead + Atmospheric Backing`
- `Separate Verses + Shared Final Chorus`

Duet의 중복은 성별만이 아니라 `Voice Contrast + Role Configuration`까지 비교합니다.

## 7. 중복 판단

보컬 중복은 `Female / Male / Duet`만으로 판단하지 않습니다.

다음 조합을 누적 기준으로 확인합니다.

`Vocal Type + Core Timbre + Register + Delivery + Expression + Genre`

예:

`Female + husky + low-mid + intimate + soulful + Alternative R&B`

이 조합이 가까운 Track에서 반복되면 중복 위험이 높습니다.

반면:

`Female + husky + low-mid + intimate + soulful`

과

`Female + husky + mid-high + rhythmic + confident`

은 공통 음색이 있어도 다른 보컬 캐릭터로 취급할 수 있습니다.

## 8. 다양성 운영 원칙

1. 같은 핵심 `Timbre + Delivery` 조합을 인접 Track에서 반복하지 않습니다.
2. 같은 `Genre + Timbre + Expression` 조합의 반복을 특히 주의합니다.
3. `airy`, `breathy`, `intimate`만 가을 감성의 기본값처럼 반복하지 않습니다.
4. Female 보컬을 모두 가볍고 높은 음역으로 만들지 않습니다.
5. Male 보컬을 모두 낮고 허스키하게 만들지 않습니다.
6. R&B라고 항상 `soulful / velvety`를 자동 배정하지 않습니다.
7. Indie라고 항상 `husky / raw`를 자동 배정하지 않습니다.
8. 밝은 곡에도 낮은 음역 또는 따뜻한 보컬을 사용할 수 있고, 느린 곡에도 clear vocal을 사용할 수 있습니다.
9. 한 프로젝트 안에서 다양한 조합을 만들되, 한 곡의 Style Prompt에는 핵심 캐릭터만 간결하게 남깁니다.
10. 실존 가수의 목소리를 목표로 삼지 않고 음향적 특성으로 설명합니다.

## 9. MASTER BOARD 및 확정 배치 운영

현재 작성된 MASTER BOARD의 `Vocal: Female / Male / Duet` 값은 그대로 유효합니다.

Track 001~100의 Vocal Character 최종 재검토와 배치는 완료되었으며, 확정 단일 기준은 `VOCAL_CHARACTER_ASSIGNMENTS.md`입니다.

최종 배치표는 다음 정보를 관리합니다.

- Core Timbre
- Weight
- Register
- Delivery
- Expression
- Technique
- Duet Role

Vocal Character 배정 완료는 MASTER BOARD의 Planning 승인과 별개입니다. 사용자 별도 승인 전 Track 상태는 `PLANNED`를 유지합니다.

기존 `Vocal` 자체를 Female → Male, Male → Duet처럼 바꿀 필요가 있는 경우에는 일반 Character 조정과 구분하여 별도 변경 제안으로 처리합니다.

## 10. 실제 작사 / Style Prompt 단계

한 곡의 실제 작사를 시작할 때는 대상 Track의 `VOCAL_CHARACTER_ASSIGNMENTS.md` 행을 읽고 Style Prompt에 필요한 요소만 자연어로 확장합니다.

권장 순서:

`[core timbre] + [vocal type] + [register/weight] + [expression or phrasing] + [delivery]`

예:

`warm husky female vocal, soft low-mid register, soulful phrasing, intimate close-mic delivery`

다음처럼 지나치게 많은 특성을 나열하지 않습니다.

`warm airy smoky husky velvety emotional soulful fragile soft female vocal...`

목표는 많은 수식어가 아니라 서로 구별되는 보컬 캐릭터입니다.

실제 제작 시에는 대상 Track뿐 아니라 앞뒤 Track의 Character도 확인해 연속 피로와 유사 Character 반복을 다시 검토합니다.

## 11. 현재 적용 상태

- MASTER BOARD 001~100: 기획 완료
- 기존 Vocal Type: Female 40 / Male 40 / Duet 20 유지
- Vocal Character 001~100: 최종 배정 완료
- 확정 배치 파일: `VOCAL_CHARACTER_ASSIGNMENTS.md`
- Track Status: 전곡 `PLANNED` 유지
- 실제 가사 / 완성 Style Prompt: 미작성
- 다음 단계: 사용자 별도 Planning 승인 후 `1곡 = 1개 독립 대화 세션` 방식으로 실제 제작

이 문서는 2026 AUTUMN 프로젝트의 프로젝트별 보컬 지침이며, `suno-music-master`의 공통 규칙보다 우선하지 않습니다.

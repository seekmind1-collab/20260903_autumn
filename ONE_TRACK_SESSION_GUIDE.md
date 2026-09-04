# ONE TRACK SESSION GUIDE — 2026 AUTUMN

## 목적

실제 작사 단계에서 컨텍스트 누적 때문에 후반 곡의 규칙 누락, 표현 반복, 구조 획일화가 발생하는 문제를 방지합니다.

이번 프로젝트의 실제 가사 작성은 반드시 `1곡 = 1개 독립 대화 세션`을 기본으로 합니다.

## 1. 새 작사 세션에서 읽을 문서

1. `seekmind1-collab/suno-music-master/START_HERE.md`
2. `seekmind1-collab/suno-music-master/CORE_RULES.md`
3. 이 저장소의 `PROJECT_PLAN.md`
4. 대상 Track이 포함된 MASTER BOARD 파일의 해당 행
5. 이 저장소의 `DUPLICATION_INDEX.md`
6. 이 저장소의 `VOCAL_CHARACTER_GUIDE.md`
7. 이 저장소의 `VOCAL_CHARACTER_ASSIGNMENTS.md`에서 대상 Track 행과 앞뒤 Track 행
8. `seekmind1-collab/suno-music-master/TRACK_TEMPLATE.md`
9. `seekmind1-collab/suno-music-master/QA_CHECKLIST.md`

전체 100곡의 기존 가사를 읽는 방식은 기본 절차로 사용하지 않습니다.

## 2. 세션 입력 범위

작사 세션에는 다음 정보만 집중적으로 가져옵니다.

- 대상 Track의 승인된 MASTER_BOARD 행
- 앞 Track과 뒤 Track의 Title / Hook / Primary Genre / BPM / Vocal / Structure
- 대상 Track과 인접 Track의 Vocal Character
- DUPLICATION_INDEX의 제목·Hook·상황 중복 주의
- 공통 금지 표현
- 해당 곡의 언어 모드와 보컬 방향

## 3. Vocal Character 적용 규칙

- MASTER BOARD의 `Female / Male / Duet` 값은 그대로 유지합니다.
- `VOCAL_CHARACTER_ASSIGNMENTS.md`의 대상 Track Character를 실제 제작의 기준으로 사용합니다.
- Character 전체를 Style Prompt에 그대로 나열하지 않습니다.
- `VOCAL_CHARACTER_GUIDE.md` 기준으로 핵심 Timbre / Expression 특성 1~2개를 우선 선택합니다.
- Register / Weight / Delivery / Technique는 필요한 기능적 정보만 추가합니다.
- 앞뒤 Track의 `Timbre + Register + Delivery + Expression`을 비교해 연속 피로와 캐릭터 중복을 다시 확인합니다.
- Duet은 지정된 Voice Contrast와 Role Configuration을 반영합니다.
- Vocal Character 조정이 필요하면 가사 작성 전에 변경 제안만 하고, 임의로 배치표를 바꾸지 않습니다.

## 4. 절대 규칙

- `PLANNING_APPROVED`가 아닌 Track은 작사하지 않습니다.
- 한 세션에서 두 번째 곡의 실제 가사를 이어서 쓰지 않습니다.
- 승인된 Title, 핵심 상황, Hook 방향, Primary Genre, BPM, Vocal Type, Language, Structure를 임의로 변경하지 않습니다.
- 변경이 필요하면 실제 가사를 쓰기 전에 변경 제안만 합니다.
- 실존 가수, 실존 곡, 상표명을 Style Prompt에 넣지 않습니다.
- 완성 결과는 `Title + Style Prompt + Structured Lyrics` 형태로 제공합니다.
- SUNO 브라우저 자동화는 수행하지 않습니다.

## 5. 실제 Track 파일

작사 승인 후 다음과 같이 10곡 단위 폴더를 사용합니다.

- `tracks/001-010/`
- `tracks/011-020/`
- `tracks/021-030/`
- `tracks/031-040/`
- `tracks/041-050/`
- `tracks/051-060/`
- `tracks/061-070/`
- `tracks/071-080/`
- `tracks/081-090/`
- `tracks/091-100/`

파일명 예시:

```text
tracks/001-010/TRACK_001_긴소매를_꺼낸_날.md
```

각 파일은 공통 `TRACK_TEMPLATE.md` 구조를 유지합니다.

## 6. 권장 새 세션 시작 프롬프트

```text
@GitHub

GitHub 저장소 `seekmind1-collab/20260903_autumn`의 Track XXX 한 곡만 작업합니다.

먼저 공통 기준 저장소 `seekmind1-collab/suno-music-master`의 START_HERE.md, CORE_RULES.md, TRACK_TEMPLATE.md, QA_CHECKLIST.md를 확인하세요.

그 다음 `seekmind1-collab/20260903_autumn`의 PROJECT_PLAN.md, 대상 Track이 포함된 MASTER BOARD, DUPLICATION_INDEX.md, VOCAL_CHARACTER_GUIDE.md, VOCAL_CHARACTER_ASSIGNMENTS.md를 확인하세요.

이번 세션에서는 Track XXX만 실제 작사합니다. 다른 곡의 실제 가사를 작성하지 마세요.

MASTER BOARD에서 Track XXX가 PLANNING_APPROVED인지 먼저 확인하고, 승인된 Title / 상황 / Hook 방향 / Primary Genre / BPM / Vocal / Language / Structure를 유지하세요.

VOCAL_CHARACTER_ASSIGNMENTS.md에서 Track XXX와 앞뒤 Track의 Character를 확인하고, 확정 Character에서 핵심 특성만 선별해 Style Prompt에 반영하세요. Character 전체를 수식어처럼 나열하지 마세요.

앞뒤 인접 Track과 DUPLICATION_INDEX를 비교해 중복 위험을 먼저 짧게 점검한 뒤, 해당 곡의 Title + Style Prompt + Structured Lyrics를 작성하세요.
```

## 7. 완료 후 갱신

한 곡의 Text QA가 끝난 후 해당 Track 파일에 결과를 기록합니다.

총괄 세션에서만 필요에 따라 다음 공통 파일을 갱신합니다.

- 해당 MASTER BOARD 파일
- `DUPLICATION_INDEX.md`
- Vocal Character가 승인 절차를 거쳐 변경된 경우 `VOCAL_CHARACTER_ASSIGNMENTS.md`

곡 제목이나 Hook이 변경되었다면 해당 MASTER BOARD와 `DUPLICATION_INDEX.md`를 반드시 함께 갱신합니다.

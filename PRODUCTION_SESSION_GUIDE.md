# PRODUCTION SESSION GUIDE — 2026 AUTUMN

## 목적

Track 001~100 실제 제작을 `1개 대화 세션 = 최대 3곡` 단위로 진행하면서, 동일 프롬프트를 여러 세션에 동시에 실행해도 서로 다른 Batch를 자동 선점하도록 운영합니다.

기존 `1곡 = 1개 독립 대화 세션` 원칙은 이 프로젝트의 현재 제작 단계에서는 사용하지 않습니다.

공통 저장소의 세션 권장 한도인 일반곡 최대 5곡, 아이돌/듀엣 최대 3곡 범위 안에서 모든 Production Batch를 최대 3곡으로 통일합니다.

## 1. Production Batch

`PRODUCTION_QUEUE.md`가 유일한 순서 기준입니다.

- 001~003
- 004~006
- 007~009
- ...
- 097~099
- 100

사용자는 매 세션마다 Track 번호를 지정하지 않습니다.

각 세션이 GitHub에서 아직 선점되지 않은 가장 앞의 Batch를 자동으로 찾습니다.

## 2. 새 제작 세션에서 먼저 읽을 문서

### 공통 저장소 `seekmind1-collab/suno-music-master`

1. `START_HERE.md`
2. `CORE_RULES.md`
3. `TRACK_TEMPLATE.md`
4. `QA_CHECKLIST.md`

### 프로젝트 저장소 `seekmind1-collab/20260903_autumn`

1. `README.md`
2. `PRODUCTION_SESSION_GUIDE.md`
3. `PRODUCTION_QUEUE.md`
4. `production_claims/README.md`
5. 대상 Batch가 포함된 MASTER BOARD 파일
6. `DUPLICATION_INDEX.md`
7. `VOCAL_CHARACTER_GUIDE.md`
8. `VOCAL_CHARACTER_ASSIGNMENTS.md`

필요한 경우 대상 Batch 바로 앞뒤 Track의 MASTER BOARD 정보와 이미 완성된 Track 파일도 확인합니다.

## 3. 자동 선점 절차

### 기본

1. `PRODUCTION_QUEUE.md`를 Track 번호 오름차순으로 읽습니다.
2. 첫 Batch부터 해당 CLAIM 파일의 존재 여부를 확인합니다.
3. `IN_PROGRESS` 또는 `COMPLETE` CLAIM이 있으면 건너뜁니다.
4. CLAIM 파일이 없으면 해당 경로에 새 파일 생성을 실제로 시도합니다.
5. 파일 생성에 성공한 경우에만 그 Batch를 이 세션의 작업 범위로 확정합니다.
6. 생성 실패 또는 충돌은 다른 세션이 먼저 선점한 것으로 보고 즉시 다음 Batch로 이동합니다.
7. 사용자에게 Track 범위를 다시 묻지 않습니다.
8. CLAIM 성공 전에는 가사나 완성 Style Prompt를 작성하지 않습니다.

### CLAIM 경로

예:

- `production_claims/CLAIM_001_003.md`
- `production_claims/CLAIM_028_030.md`
- `production_claims/CLAIM_100.md`

### CLAIM 시작 내용

```text
# PRODUCTION CLAIM

- Tracks: 001~003
- Status: IN_PROGRESS
- Lyrics: IN_PROGRESS
- Text QA: NOT_STARTED
```

### RELEASED 처리

`RELEASED` 상태의 기존 CLAIM은 최신 SHA를 다시 읽은 후 `IN_PROGRESS`로 갱신을 시도합니다.

동시 갱신 충돌이 발생하면 해당 Batch를 포기하고 다음 Batch로 이동합니다.

다른 세션의 `IN_PROGRESS` CLAIM은 절대 빼앗지 않습니다.

## 4. 작업 범위 확정

CLAIM에 성공한 뒤에만 사용자에게 짧게 다음 내용을 알립니다.

`이번 세션 작업 범위: Track XXX~XXX`

그 후 해당 Batch의 Track만 실제 제작합니다.

Batch 밖의 실제 가사는 작성하지 않습니다.

## 5. 각 Track에서 유지할 MASTER BOARD 기준

특별한 명백한 오류가 없는 한 다음 요소를 임의로 변경하지 않습니다.

- Title
- Core Situation
- Relationship / Speaker
- Emotional Direction
- Hook 방향
- Primary Genre
- BPM
- Vocal Type
- Language Mode
- Idol Style
- Structure

수정이 꼭 필요하면 실제 가사를 쓰기 전에 최소 변경으로 처리하고 그 이유를 기록합니다.

## 6. Vocal Character

각 Track마다 반드시 `VOCAL_CHARACTER_ASSIGNMENTS.md`의 확정 Character를 사용합니다.

- Female / Male / Duet 자체는 변경하지 않습니다.
- Character 전체를 Style Prompt에 그대로 나열하지 않습니다.
- `VOCAL_CHARACTER_GUIDE.md` 기준으로 핵심 Timbre / Expression 1~2개를 우선 사용합니다.
- Register / Weight / Delivery / Technique는 필요한 기능적 설명만 추가합니다.
- 동일 Batch 안 3곡의 보컬 캐릭터 체감이 겹치지 않는지 다시 확인합니다.

## 7. 실제 결과물

각 Track은 다음을 완성합니다.

1. Title
2. Style Prompt
3. Structured Lyrics

실존 가수명, 실존 곡명, 상표명을 Style Prompt에 사용하지 않습니다.

실제 Track 파일은 다음 10곡 단위 폴더를 사용합니다.

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

`tracks/001-010/TRACK_001_긴소매를_꺼낸_날.md`

각 파일은 공통 `TRACK_TEMPLATE.md` 구조를 기준으로 저장합니다.

## 8. 3곡 내부 QA

3곡을 모두 작성한 후 서로 비교합니다.

- Verse 시작 문법 반복
- Chorus 첫 문장 반복
- Hook 리듬 / 반복 방식
- 영어 캐치프레이즈 반복
- 같은 감정 결론
- 보컬 Delivery / Register 체감 반복
- 같은 악기 중심 전개
- Bridge 기능 반복
- Outro 방식 반복
- 비슷한 문장 길이와 어순
- AI 상투어

필요한 수정은 담당 Batch 안에서 이 세션이 직접 완료합니다.

## 9. 병렬 실행 때문에 가능한 것과 불가능한 것

10개 세션을 동시에 실행하면 앞 Batch가 아직 완성되지 않은 상태에서 뒤 Batch가 제작될 수 있습니다.

따라서 제작 세션에서는:

- 자신의 3곡 내부 실제 가사 중복 QA는 수행합니다.
- 앞뒤 Track은 MASTER BOARD / DUPLICATION_INDEX / Vocal Character 기준으로 비교합니다.
- 이미 완성된 인접 Track 파일이 있으면 추가로 참고합니다.
- 아직 완성되지 않은 다른 Batch의 실제 가사를 기다리거나 추측하지 않습니다.

**Batch 사이 실제 완성 가사 중복 검수는 병렬 제작 후 별도의 통합 QA 세션에서 수행합니다.**

## 10. 병렬 세션에서 수정 금지할 공유 파일

충돌 방지를 위해 일반 Production Session은 아래 파일을 읽기 전용으로 취급합니다.

- `README.md`
- `MASTER_BOARD_INDEX.md`
- `MASTER_BOARD*.md`
- `DUPLICATION_INDEX.md`
- `VOCAL_CHARACTER_GUIDE.md`
- `VOCAL_CHARACTER_ASSIGNMENTS.md`
- `PRODUCTION_QUEUE.md`
- 다른 Batch의 CLAIM 파일

자신의 세션에서 수정할 수 있는 것은 원칙적으로:

1. 자신의 CLAIM 파일
2. 자신의 Track 파일 1~3개

뿐입니다.

## 11. 완료 처리

담당 Track 파일 저장과 3곡 내부 Text QA가 끝나면 자신의 CLAIM 파일만 다음 상태로 갱신합니다.

```text
# PRODUCTION CLAIM

- Tracks: 001~003
- Status: COMPLETE
- Lyrics: COMPLETE
- Text QA: COMPLETE
```

병렬 제작 세션에서는 전체 MASTER BOARD 상태나 공통 인덱스를 갱신하지 않습니다.

여러 Production Session 완료 후 별도 통합 세션에서 다음을 수행합니다.

- CLAIM 완료 상태 집계
- Track 파일 누락 확인
- Batch 간 실제 가사 중복 QA
- 필요 시 `DUPLICATION_INDEX.md` 보강
- 프로젝트 전체 상태 갱신

## 12. 핵심 안전장치 요약

- 번호를 사용자가 지정하지 않음
- GitHub CLAIM 성공으로만 Batch 확정
- 동일 CLAIM 파일 생성 경쟁으로 중복 선점 방지
- 실패하면 자동으로 다음 Batch 탐색
- 최대 3곡만 작업
- 공유 인덱스는 병렬 세션에서 수정하지 않음
- Batch 간 실제 가사 QA는 이후 통합 세션으로 분리

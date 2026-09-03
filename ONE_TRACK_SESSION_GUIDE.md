# ONE TRACK SESSION GUIDE — 2026 AUTUMN

## 목적

실제 작사 단계에서 컨텍스트 누적 때문에 후반 곡의 규칙 누락, 표현 반복, 구조 획일화가 발생하는 문제를 방지합니다.

이번 프로젝트의 실제 가사 작성은 반드시 `1곡 = 1개 독립 대화 세션`을 기본으로 합니다.

## 1. 새 작사 세션에서 읽을 문서

1. `seekmind1-collab/suno-music-master/START_HERE.md`
2. `seekmind1-collab/suno-music-master/CORE_RULES.md`
3. 이 저장소의 `PROJECT_PLAN.md`
4. 이 저장소의 `MASTER_BOARD.md`에서 대상 Track 행
5. 이 저장소의 `DUPLICATION_INDEX.md`
6. `seekmind1-collab/suno-music-master/TRACK_TEMPLATE.md`
7. `seekmind1-collab/suno-music-master/QA_CHECKLIST.md`

전체 30곡의 기존 가사를 읽는 방식은 기본 절차로 사용하지 않습니다.

## 2. 세션 입력 범위

작사 세션에는 다음 정보만 집중적으로 가져옵니다.

- 대상 Track의 승인된 MASTER_BOARD 행
- 앞 Track과 뒤 Track의 Title / Hook / Primary Genre / BPM / Vocal / Structure
- DUPLICATION_INDEX의 제목·Hook·상황 중복 주의
- 공통 금지 표현
- 해당 곡의 언어 모드와 보컬 방향

## 3. 절대 규칙

- `PLANNING_APPROVED`가 아닌 Track은 작사하지 않습니다.
- 한 세션에서 두 번째 곡의 실제 가사를 이어서 쓰지 않습니다.
- 승인된 Title, 핵심 상황, Hook 방향, Primary Genre, BPM을 임의로 변경하지 않습니다.
- 변경이 필요하면 실제 가사를 쓰기 전에 변경 제안만 합니다.
- 실존 가수, 실존 곡, 상표명을 Style Prompt에 넣지 않습니다.
- 완성 결과는 `Title + Style Prompt + Structured Lyrics` 형태로 제공합니다.
- SUNO 브라우저 자동화는 수행하지 않습니다.

## 4. 실제 Track 파일

작사 승인 후 다음 경로를 사용합니다.

- `tracks/001-010/`
- `tracks/011-020/`
- `tracks/021-030/`

파일명 예시:

```text
tracks/001-010/TRACK_001_긴소매를_꺼낸_날.md
```

각 파일은 공통 `TRACK_TEMPLATE.md` 구조를 유지합니다.

## 5. 권장 새 세션 시작 프롬프트

```text
GitHub 저장소 `seekmind1-collab/20260903_autumn`의 Track XXX 한 곡만 작업합니다.

먼저 공통 기준 저장소 `seekmind1-collab/suno-music-master`의 START_HERE.md, CORE_RULES.md, TRACK_TEMPLATE.md, QA_CHECKLIST.md를 확인하세요.

그 다음 `seekmind1-collab/20260903_autumn`의 PROJECT_PLAN.md, MASTER_BOARD.md, DUPLICATION_INDEX.md를 확인하세요.

이번 세션에서는 Track XXX만 실제 작사합니다. 다른 곡의 실제 가사를 작성하지 마세요.

MASTER_BOARD에서 Track XXX가 PLANNING_APPROVED인지 먼저 확인하고, 승인된 Title / 상황 / Hook 방향 / Primary Genre / BPM / Vocal / Language / Structure를 유지하세요.

앞뒤 인접 Track과 DUPLICATION_INDEX를 비교해 중복 위험을 먼저 짧게 점검한 뒤, 해당 곡의 Title + Style Prompt + Structured Lyrics를 작성하세요.
```

## 6. 완료 후 갱신

한 곡의 Text QA가 끝난 후 해당 Track 파일에 결과를 기록합니다.

총괄 세션에서만 필요에 따라 다음 공통 파일을 갱신합니다.

- `MASTER_BOARD.md`
- `DUPLICATION_INDEX.md`

곡 제목이나 Hook이 변경되었다면 두 파일을 반드시 함께 갱신합니다.

# 2026 AUTUMN — SUNO PROJECT

2026년 가을 시즌용 SUNO 음악 프로젝트입니다.

## 목표

- 최종 목표: 100곡
- 한 번에 100곡을 기획하지 않음
- 새로운 기획 대화 세션마다 최대 30곡의 MASTER BOARD를 추가
- 실제 가사는 반드시 `1곡 = 1개 독립 대화 세션`

## 기준 저장소

공통 제작 규칙과 템플릿은 아래 저장소를 기준으로 합니다.

- `seekmind1-collab/suno-music-master`
  - `START_HERE.md`
  - `CORE_RULES.md`
  - `PROJECT_TEMPLATE.md`
  - `TRACK_TEMPLATE.md`
  - `QA_CHECKLIST.md`

이 프로젝트 저장소에는 공통 규칙의 복사본을 두지 않고 프로젝트별 기획과 결과물만 관리합니다.

## 100곡 확장 방식

| Planning session | Tracks | Master Board |
|---|---:|---|
| Batch 01 | 001~030 | `MASTER_BOARD.md` |
| Batch 02 | 031~060 | `MASTER_BOARD_031_060.md` |
| Batch 03 | 061~090 | `MASTER_BOARD_061_090.md` |
| Batch 04 | 091~100 | `MASTER_BOARD_091_100.md` |

`MASTER_BOARD.md`는 이미 설계한 첫 30곡의 기준 문서로 유지합니다. 이후 보드는 각각 새로운 대화 세션에서 생성했습니다.

## 프로젝트 문서

- `PROJECT_PLAN.md` — 첫 30곡의 음악 방향과 분포 및 프로젝트 기본 방향
- `MASTER_BOARD.md` — Track 001~030 Decision Gate
- `MASTER_BOARD_031_060.md` — Track 031~060 Decision Gate
- `MASTER_BOARD_061_090.md` — Track 061~090 Decision Gate
- `MASTER_BOARD_091_100.md` — Track 091~100 Decision Gate
- `MASTER_BOARD_INDEX.md` — 전체 보드와 Track 범위 관리
- `MASTER_BOARD_SESSION_GUIDE.md` — MASTER BOARD 기획 세션 운영 규칙
- `DUPLICATION_INDEX.md` — Track 001~100의 제목·상황·Hook·장르·BPM·보컬·언어 중복 누적 관리
- `VOCAL_CHARACTER_GUIDE.md` — 고정형 보컬 프로필 대신 음색·무게·음역·전달·감정·기법을 조합하여 보컬 캐릭터를 설계하는 프로젝트 전용 기준
- `VOCAL_CHARACTER_ASSIGNMENTS.md` — Track 001~100의 최종 Vocal Character 단일 배치표
- `ONE_TRACK_SESSION_GUIDE.md` — 실제 작사 시 `1곡 = 1개 독립 대화 세션` 운영 규칙

## 핵심 운영 원칙

- MASTER BOARD 기획은 Track 001~100까지 완료했습니다.
- 실제 가사는 아직 작성하지 않았습니다.
- 실제 가사는 반드시 `1곡 = 1개 독립 대화 세션`입니다.
- 각 작사 세션은 대상 Track, 인접 Track, `DUPLICATION_INDEX.md`, `VOCAL_CHARACTER_ASSIGNMENTS.md`, 공통 규칙을 중심적으로 참조합니다.
- 보컬 다양성은 `Female / Male / Duet`만으로 판단하지 않고 `VOCAL_CHARACTER_GUIDE.md`의 조합형 Character 기준을 사용합니다.
- Track 001~100의 Vocal Character 최종 배정은 `VOCAL_CHARACTER_ASSIGNMENTS.md`에 완료되어 있습니다.
- 기존 MASTER BOARD의 Female / Male / Duet 비율은 Female 40 / Male 40 / Duet 20으로 유지합니다.
- Vocal Character 배정은 기존 Title / 상황 / 관계 / 감정 / Primary Genre / BPM / Language / Idol Style / Structure를 변경하지 않습니다.
- Character 전체를 완성 Style Prompt에 그대로 나열하지 않고, 실제 제작 시 핵심 특성 1~2개와 필요한 기능적 설명만 선별합니다.
- 최종 제작물은 `Title + Style Prompt + Structured Lyrics` 형식입니다.
- SUNO 생성은 사용자가 직접 복사·붙여넣기로 진행합니다.
- 브라우저 자동화는 현재 범위에서 제외합니다.
- 사용자 별도 승인 전 모든 Track 상태는 `PLANNED`로 유지합니다.

현재 단계: `MASTER_BOARD_001_100_PLANNED_COMPLETE / VOCAL_CHARACTER_001_100_ASSIGNED`

# 2026 AUTUMN — SUNO PROJECT

2026년 가을 시즌용 SUNO 음악 프로젝트입니다.

## 목표

- 최종 목표: 100곡
- MASTER BOARD 001~100 기획 완료
- Vocal Character 001~100 배정 완료
- 실제 제작은 `1개 대화 세션 = 최대 3곡`
- 동일한 제작 프롬프트를 여러 세션에 동시에 실행 가능
- GitHub CLAIM 파일로 Batch 중복 선점을 방지

## 기준 저장소

공통 제작 규칙과 템플릿은 아래 저장소를 기준으로 합니다.

- `seekmind1-collab/suno-music-master`
  - `START_HERE.md`
  - `CORE_RULES.md`
  - `PROJECT_TEMPLATE.md`
  - `TRACK_TEMPLATE.md`
  - `QA_CHECKLIST.md`

이 프로젝트 저장소에는 공통 규칙의 복사본을 두지 않고 프로젝트별 기획과 결과물만 관리합니다.

## MASTER BOARD 구성

| Planning session | Tracks | Master Board |
|---|---:|---|
| Batch 01 | 001~030 | `MASTER_BOARD.md` |
| Batch 02 | 031~060 | `MASTER_BOARD_031_060.md` |
| Batch 03 | 061~090 | `MASTER_BOARD_061_090.md` |
| Batch 04 | 091~100 | `MASTER_BOARD_091_100.md` |

## 프로젝트 문서

- `PROJECT_PLAN.md` — 프로젝트 기본 방향
- `MASTER_BOARD.md` — Track 001~030 Decision Gate
- `MASTER_BOARD_031_060.md` — Track 031~060 Decision Gate
- `MASTER_BOARD_061_090.md` — Track 061~090 Decision Gate
- `MASTER_BOARD_091_100.md` — Track 091~100 Decision Gate
- `MASTER_BOARD_INDEX.md` — 전체 보드와 상태 관리
- `DUPLICATION_INDEX.md` — Track 001~100 중복 누적 관리
- `VOCAL_CHARACTER_GUIDE.md` — Vocal Character 조합형 설계 기준
- `VOCAL_CHARACTER_ASSIGNMENTS.md` — Track 001~100 최종 Vocal Character 단일 배치표
- `PRODUCTION_QUEUE.md` — 실제 제작용 3곡 단위 고정 Batch 순서 및 제작 승인 기준
- `PRODUCTION_SESSION_GUIDE.md` — 병렬 3곡 제작 세션 운영 규칙
- `production_claims/README.md` — GitHub CLAIM 잠금 규칙
- `ONE_TRACK_SESSION_GUIDE.md` — 과거 1곡 단위 운영 방식의 기록용 문서. 현재 제작에는 사용하지 않음

## 현재 제작 운영 원칙

### 1. 세션 단위

실제 제작은 `1개 대화 세션 = 최대 3곡`입니다.

Production Batch는 `PRODUCTION_QUEUE.md`에 고정되어 있습니다.

- 001~003
- 004~006
- 007~009
- ...
- 097~099
- 100

### 2. 사용자 Track 번호 지정 불필요

사용자는 각 제작 세션마다 Track 번호를 지정하지 않습니다.

각 세션은 GitHub의 최신 CLAIM 상태를 확인하고 아직 다른 세션이 선점하지 않은 가장 앞 Batch를 자동으로 가져갑니다.

### 3. 병렬 실행

동일한 프롬프트를 여러 대화 세션에 동시에 실행할 수 있습니다.

Batch 소유권은 채팅 선언이 아니라 `production_claims/CLAIM_XXX_XXX.md` 파일 생성 성공으로만 확정합니다.

CLAIM 생성에 실패하면 다른 세션이 먼저 선점한 것으로 보고 다음 Batch로 자동 이동합니다.

### 4. 제작 승인

2026-09-04 사용자 결정으로 Track 001~100의 MASTER BOARD와 Vocal Character 배정은 실제 제작 기준으로 승인되었습니다.

`PRODUCTION_QUEUE.md`의 모든 Batch는 `APPROVED_FOR_PRODUCTION` 상태입니다.

기존 MASTER BOARD 파일의 `PLANNED` 표기는 기획 당시의 스냅샷으로 유지하며, 현재 실제 제작 가능 여부는 `PRODUCTION_QUEUE.md`를 기준으로 판단합니다.

이는 기획 내용 자체를 변경하지 않고 병렬 제작 단계의 승인 상태를 별도 운영 레이어로 분리하기 위함입니다.

### 5. Vocal Character

- 기존 Vocal Type은 Female 40 / Male 40 / Duet 20을 유지합니다.
- `VOCAL_CHARACTER_ASSIGNMENTS.md`를 실제 제작의 단일 기준으로 사용합니다.
- Character 전체를 Style Prompt에 그대로 나열하지 않습니다.
- `VOCAL_CHARACTER_GUIDE.md` 기준으로 핵심 특성만 선별합니다.

### 6. 병렬 세션의 쓰기 범위

병렬 제작 세션은 원칙적으로 다음만 수정합니다.

1. 자신이 선점한 CLAIM 파일
2. 자신이 담당한 Track 파일 1~3개

MASTER BOARD, DUPLICATION_INDEX, PRODUCTION_QUEUE 같은 공유 파일은 병렬 제작 세션에서 수정하지 않습니다.

공유 문서와 Batch 간 실제 가사 중복 QA는 별도의 통합 세션에서 처리합니다.

## 최종 제작물

각 Track은 다음 형식으로 완성합니다.

- Title
- Style Prompt
- Structured Lyrics

SUNO 생성은 사용자가 직접 복사·붙여넣기로 진행합니다.

브라우저 자동화는 현재 범위에서 제외합니다.

## 현재 단계

`MASTER_BOARD_001_100_COMPLETE / VOCAL_CHARACTER_001_100_ASSIGNED / PRODUCTION_READY_PARALLEL_3_TRACK`

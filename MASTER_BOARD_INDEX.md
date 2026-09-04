# MASTER BOARD INDEX — 2026 AUTUMN

## 목적

이 문서는 100곡 규모 가을 프로젝트의 MASTER BOARD 범위와 현재 제작 단계의 상태를 관리합니다.

## 보드 구성

| Batch | Tracks | File | Planning Snapshot | Production Gate |
|---|---:|---|---|---|
| 01 | 001~030 | `MASTER_BOARD.md` | PLANNED snapshot | APPROVED_FOR_PRODUCTION |
| 02 | 031~060 | `MASTER_BOARD_031_060.md` | PLANNED snapshot | APPROVED_FOR_PRODUCTION |
| 03 | 061~090 | `MASTER_BOARD_061_090.md` | PLANNED snapshot | APPROVED_FOR_PRODUCTION |
| 04 | 091~100 | `MASTER_BOARD_091_100.md` | PLANNED snapshot | APPROVED_FOR_PRODUCTION |

기존 MASTER BOARD의 `PLANNED` 값은 각 기획 세션 종료 당시의 스냅샷으로 유지합니다.

2026-09-04 사용자 결정으로 Track 001~100은 실제 제작 단계로 진입했으며, 현재 제작 가능 여부는 `PRODUCTION_QUEUE.md`의 `APPROVED_FOR_PRODUCTION` 값을 기준으로 판단합니다.

## Vocal Character 상태

- Track 001~100 Vocal Type: Female 40 / Male 40 / Duet 20
- Track 001~100 Vocal Character 최종 배정: 완료
- 단일 기준 파일: `VOCAL_CHARACTER_ASSIGNMENTS.md`
- 설계 기준: `VOCAL_CHARACTER_GUIDE.md`

## 실제 제작 방식

- 실제 제작 단위: `1개 대화 세션 = 최대 3곡`
- 고정 Batch 순서: `PRODUCTION_QUEUE.md`
- 병렬 세션 운영: `PRODUCTION_SESSION_GUIDE.md`
- 동시 작업 선점: `production_claims/CLAIM_XXX_XXX.md`
- 사용자가 매 세션마다 Track 번호를 직접 지정하지 않음

## Production Batch 구성

- 001~003
- 004~006
- 007~009
- 010~012
- ...
- 097~099
- 100

총 34개 Production Batch입니다.

## 병렬 실행 원칙

1. 각 세션은 `PRODUCTION_QUEUE.md`를 앞에서부터 확인합니다.
2. 다른 세션의 `IN_PROGRESS` 또는 `COMPLETE` CLAIM이 있는 Batch는 건너뜁니다.
3. CLAIM 파일이 없는 가장 앞 Batch에 대해 새 CLAIM 파일 생성을 실제로 시도합니다.
4. 생성 성공한 세션만 해당 Batch를 작업합니다.
5. 생성 충돌 시 사용자에게 묻지 않고 다음 Batch로 이동합니다.
6. CLAIM 성공 전에는 실제 가사와 완성 Style Prompt를 작성하지 않습니다.
7. 일반 Production Session은 공유 MASTER BOARD와 DUPLICATION_INDEX를 수정하지 않습니다.
8. Batch 간 실제 완성 가사 중복 QA와 공통 인덱스 갱신은 별도 통합 세션에서 수행합니다.

## 현재 상태

- MASTER BOARD 기획 완료 범위: Track 001~100
- Vocal Character 배정 완료 범위: Track 001~100
- Production Gate: Track 001~100 승인 완료
- 실제 가사 작성: 시작 전
- Production Queue: 준비 완료
- Parallel Claim System: 준비 완료

## 다음 작업

동일한 Production Session 프롬프트를 여러 대화 세션에 동시에 실행할 수 있습니다.

각 세션은 `PRODUCTION_SESSION_GUIDE.md`와 `production_claims/README.md`에 따라 서로 다른 Production Batch를 자동 선점하고 최대 3곡을 제작합니다.

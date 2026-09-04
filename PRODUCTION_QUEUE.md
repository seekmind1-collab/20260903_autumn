# PRODUCTION QUEUE — 2026 AUTUMN

## 목적

Track 001~100 실제 제작을 `1개 대화 세션 = 최대 3곡` 단위로 병렬 실행하기 위한 고정 작업 순서입니다.

2026-09-04 사용자 결정에 따라 MASTER BOARD 001~100과 Vocal Character 001~100을 실제 제작 단계의 기준으로 사용합니다.

이 파일은 **순서와 제작 가능 범위만 정의하는 읽기 전용 기준표**입니다. 병렬 제작 세션은 이 파일을 수정하지 않습니다.

실제 선점 여부는 `production_claims/CLAIM_XXX_XXX.md` 파일로만 판단합니다.

## 운영 원칙

- Production Batch는 Track 번호 오름차순으로 3곡씩 고정합니다.
- 마지막 Track 100은 단독 Batch입니다.
- 모든 Batch의 Planning Gate는 `APPROVED_FOR_PRODUCTION`입니다.
- 동일 프롬프트를 여러 세션에서 동시에 실행할 수 있습니다.
- 세션은 가장 앞의 미선점 Batch부터 CLAIM 생성을 시도합니다.
- CLAIM 파일 생성 성공 전에는 실제 가사와 Style Prompt를 작성하지 않습니다.
- 이 파일의 상태를 세션별로 수정하지 않습니다.

## Production Batches

| Batch | Tracks | Planning Gate |
|---:|---|---|
| 001 | 001~003 | APPROVED_FOR_PRODUCTION |
| 002 | 004~006 | APPROVED_FOR_PRODUCTION |
| 003 | 007~009 | APPROVED_FOR_PRODUCTION |
| 004 | 010~012 | APPROVED_FOR_PRODUCTION |
| 005 | 013~015 | APPROVED_FOR_PRODUCTION |
| 006 | 016~018 | APPROVED_FOR_PRODUCTION |
| 007 | 019~021 | APPROVED_FOR_PRODUCTION |
| 008 | 022~024 | APPROVED_FOR_PRODUCTION |
| 009 | 025~027 | APPROVED_FOR_PRODUCTION |
| 010 | 028~030 | APPROVED_FOR_PRODUCTION |
| 011 | 031~033 | APPROVED_FOR_PRODUCTION |
| 012 | 034~036 | APPROVED_FOR_PRODUCTION |
| 013 | 037~039 | APPROVED_FOR_PRODUCTION |
| 014 | 040~042 | APPROVED_FOR_PRODUCTION |
| 015 | 043~045 | APPROVED_FOR_PRODUCTION |
| 016 | 046~048 | APPROVED_FOR_PRODUCTION |
| 017 | 049~051 | APPROVED_FOR_PRODUCTION |
| 018 | 052~054 | APPROVED_FOR_PRODUCTION |
| 019 | 055~057 | APPROVED_FOR_PRODUCTION |
| 020 | 058~060 | APPROVED_FOR_PRODUCTION |
| 021 | 061~063 | APPROVED_FOR_PRODUCTION |
| 022 | 064~066 | APPROVED_FOR_PRODUCTION |
| 023 | 067~069 | APPROVED_FOR_PRODUCTION |
| 024 | 070~072 | APPROVED_FOR_PRODUCTION |
| 025 | 073~075 | APPROVED_FOR_PRODUCTION |
| 026 | 076~078 | APPROVED_FOR_PRODUCTION |
| 027 | 079~081 | APPROVED_FOR_PRODUCTION |
| 028 | 082~084 | APPROVED_FOR_PRODUCTION |
| 029 | 085~087 | APPROVED_FOR_PRODUCTION |
| 030 | 088~090 | APPROVED_FOR_PRODUCTION |
| 031 | 091~093 | APPROVED_FOR_PRODUCTION |
| 032 | 094~096 | APPROVED_FOR_PRODUCTION |
| 033 | 097~099 | APPROVED_FOR_PRODUCTION |
| 034 | 100 | APPROVED_FOR_PRODUCTION |

## 병렬 작업에서 읽기 전용으로 유지할 공통 파일

병렬 제작 세션에서는 다음 공통 파일을 수정하지 않습니다.

- `PRODUCTION_QUEUE.md`
- `MASTER_BOARD_INDEX.md`
- `MASTER_BOARD*.md`
- `DUPLICATION_INDEX.md`
- `VOCAL_CHARACTER_GUIDE.md`
- `VOCAL_CHARACTER_ASSIGNMENTS.md`

각 제작 세션이 쓸 수 있는 파일은 원칙적으로 다음뿐입니다.

1. 자신이 선점한 `production_claims/CLAIM_XXX_XXX.md`
2. 자신이 담당한 개별 `tracks/.../TRACK_XXX_*.md`

공통 인덱스와 전체 상태 갱신은 병렬 제작 세션이 끝난 뒤 별도의 통합 QA/정리 세션에서 수행합니다.

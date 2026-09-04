# PRODUCTION CLAIMS

## 목적

동일한 제작 프롬프트를 여러 대화 세션에서 동시에 실행할 때 같은 Track을 중복 제작하지 않도록 GitHub 파일 생성 자체를 작업 잠금으로 사용합니다.

## 파일명

Production Batch마다 아래 형식을 사용합니다.

`CLAIM_XXX_XXX.md`

예:

- `CLAIM_001_003.md`
- `CLAIM_028_030.md`
- `CLAIM_100.md`

## 가장 중요한 규칙

CLAIM은 채팅에서 선언하는 것이 아니라 **GitHub 파일 생성 성공 여부**로 확정합니다.

1. `PRODUCTION_QUEUE.md`를 앞에서부터 확인합니다.
2. Batch의 CLAIM 파일이 없으면 `create file` 방식으로 생성을 시도합니다.
3. 생성에 성공한 세션만 해당 Batch를 소유합니다.
4. 다른 세션이 직전에 같은 파일을 만들었다면 생성 실패/충돌이 발생합니다.
5. 실패한 세션은 사용자에게 묻지 않고 즉시 다음 Batch로 이동합니다.
6. CLAIM 성공 전에는 실제 가사와 완성 Style Prompt를 작성하지 않습니다.
7. 다른 세션의 CLAIM 파일은 수정하거나 삭제하지 않습니다.

## CLAIM 상태

### IN_PROGRESS

```text
# PRODUCTION CLAIM

- Tracks: 001~003
- Status: IN_PROGRESS
- Lyrics: IN_PROGRESS
- Text QA: NOT_STARTED
```

### COMPLETE

담당 Track 파일 저장과 세션 내부 QA가 끝나면 동일 CLAIM 파일을 갱신합니다.

```text
# PRODUCTION CLAIM

- Tracks: 001~003
- Status: COMPLETE
- Lyrics: COMPLETE
- Text QA: COMPLETE
```

### RELEASED

세션이 실제 제작을 중단하고 Batch를 다시 작업 가능 상태로 돌릴 필요가 있을 때만 별도 유지보수 세션 또는 사용자 결정으로 사용합니다.

일반 제작 세션은 다른 세션의 `IN_PROGRESS` CLAIM을 자동으로 `RELEASED` 처리하거나 빼앗지 않습니다.

`RELEASED` CLAIM을 다시 선점할 때는 기존 파일의 최신 SHA를 읽은 뒤 `IN_PROGRESS`로 조건부 갱신을 시도합니다. 동시에 여러 세션이 재선점을 시도하면 최신 SHA로 갱신에 성공한 한 세션만 소유권을 가집니다.

## 병렬 안전 규칙

- `IN_PROGRESS`: 건너뜀
- `COMPLETE`: 건너뜀
- 파일 없음: 생성 시도
- `RELEASED`: 최신 SHA 기반 재선점 시도
- 알 수 없는 상태: 자동으로 수정하지 않고 건너뜀

CLAIM 파일은 완료 뒤에도 삭제하지 않습니다. 영구 작업 이력으로 남깁니다.

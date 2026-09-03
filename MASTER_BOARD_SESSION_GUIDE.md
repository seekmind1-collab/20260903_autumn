# MASTER BOARD SESSION GUIDE

## 목적

새로운 대화 세션에서 기존 프로젝트를 이어 받아 30곡 단위의 MASTER BOARD를 추가하기 위한 운영 문서입니다.

## 세션 단위

- Batch 01: Track 001~030 — 기존 `MASTER_BOARD.md`
- Batch 02: Track 031~060 — `MASTER_BOARD_031_060.md`
- Batch 03: Track 061~090 — `MASTER_BOARD_061_090.md`
- Batch 04: Track 091~100 — `MASTER_BOARD_091_100.md`

한 세션에서는 하나의 Batch만 기획합니다.

## 새 기획 세션 시작 순서

1. `seekmind1-collab/suno-music-master` 확인
   - `START_HERE.md`
   - `CORE_RULES.md`
   - `PROJECT_TEMPLATE.md`
   - `QA_CHECKLIST.md`
   - `TRACK_TEMPLATE.md`
2. `seekmind1-collab/20260903_autumn` 확인
   - `README.md`
   - `MASTER_BOARD_INDEX.md`
   - 이전 MASTER BOARD 파일
   - `DUPLICATION_INDEX.md`
3. 이전 Batch에서 사용한 제목 핵심어, 상황, 관계 단계, Hook 문법, 장르/BPM/보컬/언어 분포를 요약합니다.
4. 새 30곡의 전체 방향과 분포를 먼저 결정합니다.
5. 새 30곡 Decision Gate를 작성합니다.
6. 이전 Batch 및 새 Batch 내부 중복을 검토합니다.
7. 사용자 승인 전에는 실제 가사와 완성 Style Prompt를 작성하지 않습니다.
8. GitHub에는 새 MASTER BOARD와 갱신된 `DUPLICATION_INDEX.md`를 저장합니다.

## 새 MASTER BOARD 필수 열

| No. | Title | 구체적 상황 | 관계 단계 / 화자 | 감정 방향 | Hook 아이디어 / 첫 문장 | Primary Genre | BPM | Vocal | Language Mode | Idol Style | Hook Language | English Placement | Structure | 차별점 | Status |
|---:|---|---|---|---|---|---|---:|---|---|---|---|---|---|---|---|

## 30곡 설계 원칙

- 30곡의 구체적 상황은 가능한 한 서로 다르게 설계합니다.
- 이전 Batch에서 많이 사용한 상황과 관계 유형은 새 Batch에서 비중을 낮춥니다.
- 같은 Primary Genre를 연속 배치하지 않습니다.
- 같은 BPM 구간을 3곡 이상 연속 배치하지 않습니다.
- 동일 보컬 유형, 동일 구조, 동일 Hook 문법을 연속 사용하지 않습니다.
- 제목 핵심어가 이전 전체 Track과 직접 겹치지 않는지 확인합니다.
- 가을을 낙엽, 단풍, 가을밤 같은 제한된 이미지로 반복하지 않습니다.
- 연애뿐 아니라 친구, 가족, 직장, 자기 정리, 낯선 사람, 오래된 관계 등으로 분산합니다.
- 실제 가사 작성은 하지 않습니다.

## 새 세션 시작 프롬프트

아래 형식을 새 대화에 사용할 수 있습니다.

```text
@GitHub

`seekmind1-collab/suno-music-master`와
`seekmind1-collab/20260903_autumn`을 실제로 확인한 뒤 작업해줘.

이번 세션은 2026 가을 SUNO 프로젝트의 다음 MASTER BOARD를 추가하는 기획 세션이야.

먼저 아래를 확인해줘.

공통 저장소:
- START_HERE.md
- CORE_RULES.md
- PROJECT_TEMPLATE.md
- QA_CHECKLIST.md
- TRACK_TEMPLATE.md

프로젝트 저장소:
- README.md
- MASTER_BOARD_INDEX.md
- 기존 MASTER BOARD 파일들
- DUPLICATION_INDEX.md
- MASTER_BOARD_SESSION_GUIDE.md

이번 담당 범위는 Track XXX~XXX야.

이번 세션에서는 실제 가사를 작성하지 마.
먼저 기존 Track들과 제목, 상황, 관계 단계, Hook, 장르, BPM, 보컬, 언어 중복을 검토한 뒤 새로운 30곡의 MASTER BOARD를 설계해줘.

완료 후:
1. 새 MASTER BOARD 파일 생성
2. DUPLICATION_INDEX.md 누적 갱신
3. MASTER_BOARD_INDEX.md 상태 갱신

사용자 승인 전 Track 상태는 PLANNED로 유지해줘.
```

## 작사 단계

MASTER BOARD 기획 세션과 실제 작사 세션은 분리합니다.

새 Track을 실제로 제작할 때는 `ONE_TRACK_SESSION_GUIDE.md`를 따르며 반드시 `1곡 = 1개 독립 대화 세션`으로 진행합니다.

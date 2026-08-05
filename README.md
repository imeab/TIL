# TIL - Git & GitHub 기초

> 날짜: 2026-08-03

---

# DOS 명령어

Git 사용 전 기본 터미널 명령어 학습

| 명령어 | 설명 |
| --- | --- |
| `cls` | 화면 지우기 |
| `cd` | 디렉토리 이동 |
| `dir` | 파일 및 폴더 확인 |
| `type` | 파일 내용 확인 |
| `mkdir` | 폴더 생성 |

경로 이동

- `.` : 현재 위치
- `..` : 상위 경로

---

# Git 기본 개념

Git은 **버전 관리(형상 관리) 도구**이다.

파일 변경 사항을 Snapshot 형태로 기록하여 버전을 관리한다.

## Git 작업 흐름

```text
Working Directory
        ↓
git add
        ↓
Staging Area
        ↓
git commit
        ↓
Repository
```

---

# Git 기본 명령어

## 저장소 생성

```bash
git init
```

`.git` 폴더를 생성하여 Git 저장소로 만든다.

## 상태 확인

```bash
git status
```

현재 파일 변경 상태를 확인한다.

## 스테이징 추가

```bash
git add 파일명
git add .
```

변경 파일을 Staging Area에 추가한다.

## Commit

```bash
git commit -m "메시지"
```

변경 사항을 저장한다.

### Commit Convention

| 타입 | 의미 |
|---|---|
| feat | 기능 추가 |
| fix | 버그 수정 |
| docs | 문서 수정 |
| refactor | 리팩토링 |
| chore | 설정 변경 |
| test | 테스트 추가 |

---

# Git 설정

Git 설정은 적용 범위에 따라 나뉜다.

| 옵션 | 설명 |
|---|---|
| `--local` | 현재 저장소 적용 |
| `--global` | 사용자 전체 적용 |
| `--system` | 모든 사용자 적용 |

우선순위

```text
local > global > system
```

사용자 설정 예시

```bash
git config --global user.name "이름"

git config --global user.email "이메일"
```

---

# Commit 기록 확인

## git log

Commit 기록 확인

```bash
git log
```

주요 옵션

```bash
git log --oneline  # 한 줄 출력

git log --graph    # 그래프 형태

git log --all      # 모든 브랜치 확인
```

---

# git diff

변경 사항 비교

```bash
git diff
```

Working Directory의 변경 내용을 확인한다.

```bash
git diff --staged
```

Staging 영역의 변경 내용을 확인한다.

---

# Branch

Branch는 독립적인 작업 공간이다.

기능별 개발을 분리하여 협업할 수 있다.

## Branch 명령어

확인

```bash
git branch
```

생성

```bash
git branch feature/login
```

생성 후 이동

```bash
git switch -c feature/login
```

---

# Branch Naming Convention

| 이름 | 용도 |
|---|---|
| /feature | 기능 개발 |
| /fix | 버그 수정 |
| /hotfix/ | 긴급 수정 |
| /release | 배포 준비 |

예시:

```text
feature/login

fix/login-error
```

---

# 💡 오늘 느낀 점

Git은 단순히 코드를 저장하는 도구가 아니라 버전을 관리하고 협업하기 위한 필수 도구라는 것을 배웠다.

특히 Git의 기본 흐름인 **add → commit → branch** 과정을 이해할 수 있었다.

# 1,2주차 회고

## Git

- Git Init
- Git Status
- Git Add
- Git Commit
- Git Log
- Git Restore
- Git Reset
- Git Branch
- Git Switch
- Git Checkout

### 🔥Git Init

- `git init`은 Git 저장소를 초기화하는 명령어  
  이 명령을 사용하면 해당 디렉토리 내에 Git 버전 관리 시스템이 활성화된다
- Git을 사용하려면 먼저 프로젝트 폴더나 디렉토리에서 `git init`을 실행해야 한다. 이를 통해 해당 폴더는 일반 폴더에서 Git 저장소로 변환된다
- `git init`은 Git을 시작하는 첫 단계로, 이후 다른 Git 명령어들이 정상적으로 작동할 수 있도록 환경을 설정하는 명령어
- ⚠️ **Root 위치에서 git init 하지 말기 -> 필요한 폴더에서 설정**

```javascript
cd // root 이동
mkdir git-practice // root에 git-practice란 폴더 생성
cd git-practice // git-practice 폴더로 이동
git init // git-practice 폴더를 Git 시작하기 위해 초기 환경 설정
```

### 🔥Git Status

- `git status` 명령어는 현재 Git 저장소의 상태를 확인
- `"nothing to commit, working tree clean"` 메시지는 현재 작업 디렉토리에 변경 사항이 없음을 나타냄.
- <span style="color:red">변경된 파일명이 빨간색으로 표시될 경우</span>: 이는 `Working Directory`(작업 디렉토리)에서 수정된 파일을 의미
- <span style="color:green">변경된 파일명이 초록색으로 표시될 경우</span>: 이는 `Staging Area`(스테이징 영역)에서 준비된 파일을 나타냄

---

### 🔥Git Add

- `git add` 명령어는 변경된 파일을 Staging Area(스테이징 영역)로 이동시켜, 커밋을 준비하는 역할
- `git add 파일명` 시 특정 파일을 스테이징 영역에 추가
- `git add .` 시 현재 디렉토리 내 모든 변경된 파일을 스테이징 영역에 추가

```javascript
git add .       // 현재 디렉토리 내 새로운 파일 및 수정된 파일을 스테이징 (삭제된 파일 제외)
git add *       // 현재 디렉토리 내 새로운 파일 및 수정된 파일을 스테이징 (삭제된 파일 제외)
git add --all   // 수정, 삭제, 새 파일 모두 스테이징
git add -u      // 수정, 삭제된 파일만 스테이징(새 파일 제외)
```

### 🔥Git Commit

- `git commit` 명령어는 작업한 내용을 저장소에 기록하여, 버전 관리를 시작하는 중요한 작업. 이 커밋 작업을 통해 코드가 추적되고, 변경 사항이 기록됨

1.  메시지 작성 커밋 : `git commit -m "메시지"`  
    커밋 메시지를 바로 작성하여 vim을 사용하지 않고 커밋을 완료
2.  기본 커밋 : `git commit`  
    Git은 기본적으로 vim 에디터를 열어 커밋 메시지를 작성하도록 함. 이때, 메시지를 통해 변경된 내용을 설명하고 커밋을 완료

### 🔥Git Log

- `git log` 명령어는 Git에서 커밋 기록을 조회할 수 있는 명령어
- 이를 통해 저장소의 변경 이력을 확인하고, 커밋된 내용들을 추적
- `git log --oneline` 명령어는 각 커밋을 한줄로 간략히 출력(커밋해시/커밋메시지만 출력)
- `git log --oneline --graph` 명령어는 커밋 내역을 그래프 형태로 시각화하여 출력. 브랜치와 병합 상태도 함께 확인

```
git log
git log --oneline
git log --oneline --graph
```

### 🔥Git Restore

- `git restore`\*\*` 은 Git에서 작업한 내용을 되돌리는 명령어
- 스테이징 영역이나 작업디렉토리에서 수정한 파일을 복구할 때 사용
  ​

```javascript
git restore <파일명> ///<파일명>을 마지막 커밋한 상태로 돌림 [작업디렉토리]
git restore --staged <파일명> ///스테이징 영역에 추가된 파일을 스테이징 영역에서 제거 [스테이징영역]
git restore .  ///현재 디렉토리 내 수정된 모든 파일을 되돌림
```

### 🔥Git Reset

- `git reset`은 특정 커밋으로 이동하면서 변경 사항을 되돌리는 명령어
- 옵션별 동작 방식
  1.  soft : 커밋만 취소, 변경 사항은 그대로 유지
  2.  mixed : 커밋 + 스테이징 영역 초기화 (작업 디렉토리는 유지)
  3.  hard : 커밋 + 스테이징 영역 + 작업 디렉토리 변경 사항 모두 삭제
      ​

```javascript
git reset --soft HEAD~1 ///마지막 커밋 취소 (변경 사항 유지) * 파일변경 및 git add 는 유지
git reset --mixed HEAD~1 ///마지막 커밋 + 스테이징 영역 초기화 * 파일변경사항은 유지
git reset --hard HEAD~1 ///마지막 커밋 + 스테이징 영역 + 작업 디렉토리 초기화 *파일변경사항삭제`
​
///HEAD~N : N은 숫자임에따라 커밋취소 위치조정가능
```

### 🔥Git Branch

- `git branch`는 새로운 브랜치를 생성하고 관리하는 명령어  
   \- 기본브랜치가 master 또는 main으로 설정되어 있다.
  ​

```javascript
git branch <브랜치명> /// 새로운 브랜치 생성
git branch  /// 현재 존재하는 브랜치 목록 확인
git branch -d <브랜치명>/// 브랜치 삭제
```

### 🔥Git Switch

- `git switch`는 브랜치를 변경하는 명령어 (checkout의 일부 기능 대체)
  ​

```javascript
 git switch <브랜치명> ///해당 브랜치로 이동
 git switch -c <새로운 브랜치명> ///새로운 브랜치 생성 후 이동
```

### 🔥Git Chekout

- `git checkout`은 브랜치를 변경하거나 특정 커밋으로 이동하는 명령어
- 현재는 `git switch`와 `git restore`로 기능이 분리됨
  ​

```javascript
git checkout <브랜치명> ///해당 브랜치로 이동
git checkout -b <새로운 브랜치명> ///새로운 브랜치 생성 후 이동
git checkout <커밋 해시> ///특정 커밋으로 이동
```

## Figma

## Html & Css

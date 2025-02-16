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

## HTML

- HyperText 마크업 언어(HTML)는 웹에 표시되는 문서의 구조를 설명하는 표준 마크업 언어

```HTML
<!--HTML의 기본구조-->
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="utf-8" />
      <title>Machine Learning Workshop</title>
      <meta name="viewport" content="width=device-width" />
    </head>
    <body>

    </body>
  </html>
```

### 📖 문서형 선언

1. HTML5 문서형 선언

```HTML
<!DOCTYPE html>
```

2. HTML4.01 문서형 선언

```HTML
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
```

3. XHTML 1.0 문서형 선언

- XHTML 1.0은 HTML을 XML 형식에 맞게 엄격하게 작성하도록 만든 표준
- XHTML 문서는 XML 문법을 따라야 하므로, 다음과 같은 규칙이 필요
  - 모든 태그는 반드시 소문자로 작성해야 함.
  - 모든 태그는 닫아야 함. `(<br> → <br />`)
  - 속성 값은 반드시 따옴표로 감싸야 함. (width=100 → width="100")

```HTML
   <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```

|     버전      |                특징                 |     사용 여부     |
| :-----------: | :---------------------------------: | :---------------: |
|   **HTML5**   | 간단한 `<!DOCTYPE html>`, 최신 표준 | ✅ 현재 주로 사용 |
| **HTML4.01**  |    구버전, 일부 비표준 요소 허용    |  HTML5로 대체됨   |
| **XHTML 1.0** |    XML 문법을 따름, 엄격한 문법     |

### 📖 시맨틱 HTML

- #### 이미지 태그 `<img>`

|  속성   | 설명                                                                                                             |
| :-----: | :--------------------------------------------------------------------------------------------------------------- |
|   alt   | 이미지가 로드되지 않거나, 시각적으로 볼 수 없는 사용자에게 이미지의 내용을 설명하는 역할. 웹 접근성 개선에 중요. |
|   src   | 이미지의 기본 경로 설정.                                                                                         |
| srcset  | 여러 해상도의 이미지를 제공하여 반응형 이미지 적용 가능.                                                         |
|  sizes  | 뷰포트 크기에 따라 표시할 이미지 크기를 지정.                                                                    |
| loading | **지연 로딩(Lazy Loading)**을 적용하여 화면에 보일 때만 이미지를 로드함. **성능 최적화**에 도움.                 |
|         |

<img src="../assets/images/jjang.jpg" alt="음료마시는짱구" width="100" height="100" >

```html
<img
  src="../assets/images/jjang.jpg"
  alt="음료마시는짱구"
  srcset="../assets/images/jjang.jpg 400w, ../assets/images/jjang-xl.jpg 800w"
  sizes="(max-width: 800px) 400px, 800px"
  loading="lazy"
/>
```

1. 적절한 확장자 사용의 필요

- ✅ WebP, Avif, Svg : 파일 크기가 작고 품질이 좋음
- ❌ PNG, JPG는 필요할 때만 사용 : 파일 크기가 상대적으로 큼

2. SVG 관련

- `<img src="icon.svg" alt="홈 아이콘" />`

- `<svg>태그` 직접 사용 시 `alt속성`을 사용할 수 없음  
   -> 대체 텍스트를 제공하려면 `aria-label` 또는 `<title>태그`를 사용해야 함.
  | 속성 | 설명 |
  |------------|-----------------------------------------------------------|
  | `aria-label` | SVG가 중요한 의미를 가질 때 대체 텍스트 제공. 버튼, 링크 등 **클릭 가능한 요소에 적합**. |
  | `<title>` | 스크린 리더가 읽을 수 있으며, 툴팁으로도 표시될 가능성이 있음. **정보 제공용 SVG에 적합**. |

  - 클릭 가능한 SVG (예: 버튼 아이콘) → aria-label 사용
    ```html
    <button aria-label="메뉴 열기">
      <svg>...</svg>
    </button>
    ```
  - 정보 제공용 SVG (예: 아이콘, 로고) → `<title>` 사용

    ✅ title 태그를 추가하면 스크린 리더가 읽을 수 있으며, 툴팁 역할도 가능.

    ```html
    <svg>
      <title>홈 아이콘</title>
      <path d="..." />
    </svg>
    ```

- #### 피규어 태그 `<figure>`

  \- `<figure>` 태그는 이미지, 그래프, 코드, 표 등을 포함하는 **자급자족형 콘텐츠(Self-contained Content)**를 감싸는 시맨틱 태그

  ✅ 주로 `<figcaption>` 태그와 함께 사용하여 설명을 추가  
  ✅ 이미지뿐만 아니라 코드, 비디오, 오디오, 표에도 사용 가능

  ```html
  <figure>
    <img src="image.jpg" alt="설명" />
    <figcaption>이미지 설명 텍스트</figcaption>
  </figure>
  ```

- #### 하이퍼링크 태그 `<a>`

  - 하이퍼링크는 사용자가 웹 페이지를 탐색할 수 있도록 연결해주는 요소

  ```html
  <a href="https://example.com" target="_blank" rel="noopener noreferrer"
    >예제 링크</a
  >
  ```

  1. **href**
     | 값 | 설명 |
     | ------ | ------------------------------------------------------------------------------------- |
     | URL | 클릭 시 이동할 웹 주소 설정 `<a href="https://example.com">웹사이트 이동</a>` |
     | mailto | 클릭 시 이메일 클라이언트 실행 `<a href="mailto:example@email.com">이메일 보내기</a>` |
     | tel | 클릭 시 전화 연결 `<a href="tel:010-1234-5678">전화 걸기</a>` |

  2. **target**  
     💡 `target="\_blank"` 사용 시 보안 이슈 해결을 위해 `rel="noopener noreferrer"` 추가 권장!
     | 값 | 설명 |
     |------------|------------------------------------|
     |\_blank| 새 탭 또는 새 창에서 링크 열기|
     |\_self| **현재 창(기본값)**에서 링크 열기|
     |\_parent| 부모 프레임에서 링크 열기 (프레임 사용 시)|
     |\_top| 최상위 창에서 링크 열기 (프레임|

  3. **rel**
     | 값 | 설명 |
     | --- | ---- |
     |nofollow| 검색 엔진이 링크를 따라가지 않도록 설정 (SEO 최적화에 사용)|
     |noopener| 새 창(\_blank)에서 열린 페이지가 부모 창을 조작하지 못하도록 차단 (보안)|
     |noreferrer| 링크를 클릭한 페이지의 referrer(출처) 정보를 전달하지 않음|

  4. **download**  
     링크를 클릭하면 해당 파일을 다운로드

  ```html
  <a href="file.zip" download>파일 다운로드</a>
  ```

- 하이퍼링크의 웹접근성 : `aria-label`, `title`

  ```html
  <a href="https://example.com" aria-label="홈페이지로 이동">
    <img src="home.png" alt="홈" />
  </a>

  <a href="https://example.com" title="클릭하면 홈페이지로 이동">홈페이지</a>
  ```

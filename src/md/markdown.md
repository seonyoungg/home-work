# <span style="color:#F2F2F2">마크다운(MarkDown)이란?</span>

**마크다운(Markdown)** 은 읽기 쉽고 쓰기 쉬운 문서 형식을 목표로 만들어졌으며, 특히 가독성을 가장 중요하게 한다.

마크다운 문서는 복잡한 태그 없이도 일반 텍스트처럼 보이며, HTML로 변환이 가능하다. 여러 텍스트-HTML 필터(Setext, atx, Textile, reStructuredText 등)에서 영향을 받았지만, 가장 큰 영감의 원천은 일반 텍스트 이메일 형식이다.

## <span style="color:#F2F2F2">마크다운의 특징</span>

✅ **간결한 문법**  
구두점 문자를 활용하여 직관적으로 의미를 표현  
예) `**강조**` → **강조**

✅ **가독성 강조**  
마크다운 문서는 마크업된 코드처럼 보이지 않고, 일반 텍스트처럼 쉽게 읽을 수 있음  
목록, 인용문 등의 형식이 일반 텍스트에서도 자연스럽게 보이도록 설계됨

✅ **인라인 HTML 지원**  
마크다운은 HTML을 완전히 대체하는 것이 아니라, HTML과 함께 사용할 수 있도록 설계됨  
마크다운에서 다룰 수 없는 포맷은 직접 HTML 태그를 사용하여 작성 가능

✅ **출판을 위한 형식**
HTML은 출판 형식, 마크다운은 쓰기 형식으로 구분  
문서를 쉽고 빠르게 작성한 후 HTML로 변환하여 웹에서 활용 가능

## <span style="color:#F2F2F2">마크다운 사용 가능 플랫폼</span>

- 개발 관련 플랫폼 : GitHub, GitLab, Jupyter Notebook
- 블로그 및 CMS : Velog, Hugo, Hexo, Ghost
- 문서 및 노트 앱 : Notion, Obsidian, Typora
- 협업 도구 : Slack, Discord, Trello
- 웹 및 기타 : Reddit, Stack Overflow, MkDocs

<details> 
<summary style="color:#F2B705">💡사용 가능 플랫폼 관련 설명 더보기</summary>

1.  📌코드 및 개발 관련 플랫폼

    - GitHub : README.md, 이슈, PR 설명 등에 사용
    - GitLab : GitHub과 유사하게 지원
    - Bitbucket : Git 저장소 내 문서 작성 가능
    - SourceForge : 프로젝트 문서화에 사용
    - Jupyter Notebook : Markdown 셀을 이용해 문서 작성 가능

2.  📌블로그 및 CMS

    - Velog : 개발자 블로그 플랫폼 (일부 GitHub과 다를 수 있음)
    - Hugo : 정적 사이트 생성기 (마크다운 기반)
    - Hexo : 개발 블로그용 정적 사이트 생성기
    - Ghost : 마크다운 지원 블로그 플랫폼
    - Tstory : 직접 지원하지 않지만 HTML로 변환하여 사용 가능

3.  📌문서 작성 및 메모 앱

    - Notion : 마크다운 입력 및 일부 변환 가능
    - Obsidian : 마크다운 기반 강력한 노트 앱
    - Joplin : 오픈소스 마크다운 노트 앱
    - Zettlr : 연구 및 논문 작성용 마크다운 에디터
    - Bear : iOS/macOS용 마크다운 지원 메모 앱

4.  📌마크다운 전용 에디터

    - Typora : 심플한 마크다운 에디터
    - Mark Text : 무료 오픈소스 마크다운 에디터
    - iA Writer : 깔끔한 마크다운 글쓰기 도구

5.  📌협업 및 커뮤니케이션

    - Slack : 일부 마크다운 문법 지원 (굵게, 기울임 등)
    - Discord : 코드 블록, 인라인 코드 등 지원
    - Mattermost : 슬랙 대체 협업 도구 (마크다운 지원)
    - Trello : 카드 설명에 마크다운 사용 가능

6.  📌웹 및 기타 도구

    - Reddit : 게시글 및 댓글에서 마크다운 사용 가능
    - Stack Overflow : 코드 블록 및 포맷팅에 활용
    - Docusaurus : 문서화 웹사이트 구축 도구
    - MkDocs : Python 기반 문서 사이트 생성기
    - Read the Docs : 오픈소스 문서화 플랫폼

    </details>

---

## <span style="color:#F2F2F2">마크다운 요소</span>

- 헤더
- 줄바꿈
- 인용구
- 목록

### 1️⃣ 헤더

- Sectext 스타일(밑줄방식) : H1, H2만 가능

  - '=' : H1 (제목 1단계)
  - '-' : H2 (제목 2단계)
  - 밑줄(= 또는 -)의 개수는 많아도 상관없음
  - <details>
      <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

    ```
    SectextStyle H1
    =============

    SectextStyle H2
    -------------
    ```

    # SectextStyle H1

    ## SectextStyle H2

    </details>

- Atx 스타일(해시방식) : H1 ~ H6 모두 가능

  - 1~6개를 사용하여 제목을 표시
  - 개수가 많을수록 작은 제목이 됨
  - 선택적으로 닫는 # 를 추가할 수도 있지만, 필수는 아님
  - <details>
      <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

    ```
    # AtxStyle H1

    ## AtxStyle H2

    ### AtxStyle H3

    #### AtxStyle H4

    ##### AtxStyle H5

    ###### AtxStyle H6
    ```

    # AtxStyle H1

    ## AtxStyle H2

    ### AtxStyle H3

    #### AtxStyle H4

    ##### AtxStyle H5

    ###### AtxStyle H6

    </details>

### 2️⃣ 줄바꿈

- 방법(1) : 문장 끝에 공백(space) 2개 추가 후 Enter
- 방법(2) : `<br />` 태그 사용 (HTML 방식)

- <details>
    <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

  ```
  Enter 한 번만 누르는 경우,
  이 문장은 줄 변경되지 않음.

  `<br/>`태그를 활용한 줄변경은<br />
  이렇게 줄 변경 처리가 됨.
  ```

  Enter 한 번만 누르는 경우,
  이 문장은 줄 변경되지 않음.

  `<br />`태그를 활용한 줄변경은<br />
  이렇게 줄 변경 처리가 됨.

  </details>

### 3️⃣ 인용구

- 각 줄 앞에 > 를 붙이면 인용문이 된다.

  - <details>
      <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

    ```
    > 별(안도현) <br/>
    > 별을 쳐다보면<br/>
    > 가고싶다
    >
    > 어두워야 빛나는<br/>
    > 그 별에<br/>
    > 셋방을 하나 얻고 싶다<br/>
    ```

    > 별(안도현) <br/>
    > 별을 쳐다보면<br/>
    > 가고싶다
    >
    > 어두워야 빛나는<br/>
    > 그 별에<br/>
    > 셋방을 하나 얻고 싶다<br/>

    </details>

- 중첩된 인용구 : > 기호 여러 개 사용시 중첩된 인용문 사용 가능(3개까지 사용 가능)
- 인용구 안에 다른 요소 포함하기 : 헤더, 목록, 코드블록 등 포함 가능

  - <details>
      <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

    ````
    > ##### 인용문안의 헤더(H5)
    >
    > > 별을 쳐다보면<br/>
    > > 가고싶다
    >
    > ```
    > #인용문안의 코드블록
    > console.log("Markdown")
    > ```
    ````

    > ##### 인용문안의 헤더(H5)
    >
    > > 별을 쳐다보면<br/>
    > > 가고싶다
    >
    > ```javascript
    > #인용문안의 코드블록
    > console.log("Markdown")
    > ```

    </details>

### 4️⃣ 목록(순서가 있는 목록과 없는 목록)

- 순서가 있는 목록

  - 숫자 뒤에 .(점) 을 붙여 작성한다.
  - <details>
      <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

    ```
    1. 첫 번째 항목
    2. 두 번째 항목
    3. 세 번째 항목
    ```

    1. 첫 번째 항목
    2. 두 번째 항목
    3. 세 번째 항목

    </details>

- 순서가 없는 목록

  - \*, +, - 기호를 사용하여 만든다.
  - <details>
      <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

    ```
    * Red
    + Blue
    - Green
      - Green-light
        - Green-dark
    ```

    - Red

    * Blue

    - Green
      - Green-light
        - Green-dark

    </details>

> ####### 참고 사이트🖥️
>
> - https://daringfireball.net/projects/markdown/syntax
> - https://support.typora.io/Markdown-Reference/
> - 문장예시 : https://tsi18708.tistory.com/98

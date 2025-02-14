# <span style="color:#F2F2F2">마크다운(MarkDown)이란?</span>

> <span style="color:#F2F2F2">**마크다운(Markdown)** 은 읽기 쉽고 쓰기 쉬운 문서 형식을 목표로 만들어졌으며, 특히 가독성을 가장 중요하게 한다.</span>
>
> 마크다운 문서는 복잡한 태그 없이도 일반 텍스트처럼 보이며, HTML로 변환이 가능하다. 여러 텍스트-HTML 필터(Setext, atx, Textile, reStructuredText 등)에서 영향을 받았지만, 가장 큰 영감의 원천은 일반 텍스트 이메일 형식이다.

## <span style="color:#F2F2F2">마크다운의 특징</span>

1. **간결한 문법✨**  
   구두점 문자를 활용하여 직관적으로 의미를 표현  
   예) `**강조**` → **강조**

2. **가독성 강조👀**  
   마크다운 문서는 마크업된 코드처럼 보이지 않고, 일반 텍스트처럼 쉽게 읽을 수 있음  
   목록, 인용문 등의 형식이 일반 텍스트에서도 자연스럽게 보이도록 설계됨

3. **인라인 HTML 지원💻**  
   마크다운은 HTML을 완전히 대체하는 것이 아니라, HTML과 함께 사용할 수 있도록 설계됨  
   마크다운에서 다룰 수 없는 포맷은 직접 HTML 태그를 사용하여 작성 가능

4. **출판을 위한 형식📖**  
   HTML은 출판 형식, 마크다운은 쓰기 형식으로 구분  
    문서를 쉽고 빠르게 작성한 후 HTML로 변환하여 웹에서 활용 가능

## <span style="color:#F2F2F2">마크다운 사용 가능 플랫폼</span>

|     **카테고리**     |            **플랫폼**            |
| :------------------: | :------------------------------: |
| **개발 관련 플랫폼** | GitHub, GitLab, Jupyter Notebook |
|  **블로그 및 CMS**   |     Velog, Hugo, Hexo, Ghost     |
| **문서 및 노트 앱**  |     Notion, Obsidian, Typora     |
|    **협업 도구**     |      Slack, Discord, Trello      |
|    **웹 및 기타**    |  Reddit, Stack Overflow, MkDocs  |

<details> 
<summary style="color:#F2B705">사용 가능 플랫폼 관련 설명 더보기💡</summary>

1. 코드 및 개발 관련 플랫폼 📌

   - GitHub : README.md, 이슈, PR 설명 등에 사용
   - GitLab : GitHub과 유사하게 지원
   - Bitbucket : Git 저장소 내 문서 작성 가능
   - SourceForge : 프로젝트 문서화에 사용
   - Jupyter Notebook : Markdown 셀을 이용해 문서 작성 가능

2. 블로그 및 CMS 📌

   - Velog : 개발자 블로그 플랫폼 (일부 GitHub과 다를 수 있음)
   - Hugo : 정적 사이트 생성기 (마크다운 기반)
   - Hexo : 개발 블로그용 정적 사이트 생성기
   - Ghost : 마크다운 지원 블로그 플랫폼
   - Tstory : 직접 지원하지 않지만 HTML로 변환하여 사용 가능

3. 문서 작성 및 메모 앱 📌

   - Notion : 마크다운 입력 및 일부 변환 가능
   - Obsidian : 마크다운 기반 강력한 노트 앱
   - Joplin : 오픈소스 마크다운 노트 앱
   - Zettlr : 연구 및 논문 작성용 마크다운 에디터
   - Bear : iOS/macOS용 마크다운 지원 메모 앱

4. 마크다운 전용 에디터 📌

   - Typora : 심플한 마크다운 에디터
   - Mark Text : 무료 오픈소스 마크다운 에디터
   - iA Writer : 깔끔한 마크다운 글쓰기 도구

5. 협업 및 커뮤니케이션 📌

   - Slack : 일부 마크다운 문법 지원 (굵게, 기울임 등)
   - Discord : 코드 블록, 인라인 코드 등 지원
   - Mattermost : 슬랙 대체 협업 도구 (마크다운 지원)
   - Trello : 카드 설명에 마크다운 사용 가능

6. 웹 및 기타 도구 📌

   - Reddit : 게시글 및 댓글에서 마크다운 사용 가능
   - Stack Overflow : 코드 블록 및 포맷팅에 활용
   - Docusaurus : 문서화 웹사이트 구축 도구
   - MkDocs : Python 기반 문서 사이트 생성기
   - Read the Docs : 오픈소스 문서화 플랫폼

   </details>

## <span style="color:#F2F2F2">마크다운 요소</span>

- 헤더
- 강조
- 줄바꿈
- 인용구
- 목록
- 코드블록
- 수평선
- 링크
- 이미지
- 체크리스트
- 테이블

### 1️⃣ 헤더

- Sectext 스타일(밑줄방식) : H1, H2만 가능

  - '=' : H1 (제목 1단계)
  - '-' : H2 (제목 2단계)
  - 밑줄(= 또는 -)의 개수는 많아도 상관없음
    <details>
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
    <details>
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

### 2️⃣ 강조

- 별표(\*) 와 밑줄(\_) 을 사용하여 텍스트를 강조할 수 있다.

  |       **형식**        |            **사용법**            |          **결과**          |
  | :-------------------: | :------------------------------: | :------------------------: |
  | **단순 강조(기울임)** |     `*텍스트*` or `_텍스트_`     |          _텍스트_          |
  |       **굵게**        |   `**텍스트**` or `__텍스트__`   |         **텍스트**         |
  |   **기울임 + 굵게**   | `***텍스트***` or `___텍스트___` |        **_텍스트_**        |
  | **강조구분문자표시**  |   `\*텍스트\*` or `\_텍스트\_`   | \*텍스트\* 또는 \_텍스트\_ |

  <details>
    <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

  ```
  _한 개 사용시 기울임_
  __두 개 사용시 굵게__
  ___세 개 사용시 기울임+굵게___
  \*강조구분문자표시\*
  ```

  _한 개 사용시 기울임_
  **두 개 사용시 굵게**
  **_세 개 사용시 기울임+굵게_** \*강조구분문자표시\*

  </details>

- 물결(~)을 사용하여 취소선을 적용할 수 있다.
  <details>
    <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

  ```
  ~~텍스트에 취소선 적용하기~~
  _**~~강조텍스트에 취소선 적용하기~~**_
  ```

  ~~텍스트에 취소선 적용하기~~  
  _**~~강조텍스트에 취소선 적용하기~~**_

  </details>

### 3️⃣ 줄바꿈

- 방법(1) : 문장 끝에 공백(space) 2개 추가 후 Enter
- 방법(2) : `<br />` 태그 사용 (HTML 방식)

  <details>
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

### 4️⃣ 인용구

- 각 줄 앞에 > 를 붙이면 인용문이 된다.

  <details>
      <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

  ```
  > 가나다라마 <br/>
  > 바사아자차<br/>
  > 카타파하
  >
  > 고노도로모보소<br/>
  > 오조초<br/>
  > 초토포호<br/>
  ```

  > 가나다라마 <br/>
  > 바사아자차<br/>
  > 카타파하
  >
  > 고노도로모보소<br/>
  > 오조초<br/>
  > 초토포호<br/>

    </details>

- 중첩된 인용구 : > 기호 여러 개 사용시 중첩된 인용문 사용 가능(3개까지 사용 가능)
- 인용구 안에 다른 요소 포함하기 : 헤더, 목록, 코드블록 등 포함 가능

  <details>
      <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

  ````
  > ##### 인용문안의 헤더(H5)
  >
  > > 가나다라마 <br/>
  > > 바사아자차<br/>
  > > 카타파하
  >
  > ```
  > #인용문안의 코드블록
  > console.log("Markdown")
  > ```
  ````

  > ##### 인용문안의 헤더(H5)
  >
  > > 가나다라마 <br/>
  > > 바사아자차<br/>
  > > 카타파하
  >
  > ```javascript
  > #인용문안의 코드블록
  > console.log("Markdown")
  > ```

    </details>

### 5️⃣ 목록(순서가 있는 목록과 없는 목록)

- 순서가 있는 목록

  - 숫자 뒤에 .(점) 을 붙여 작성한다.
    <details>
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
    <details>
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

### 6️⃣ 코드블록

- <span style="color:#FF4858;">❗코드블록 내에서는 마크다운 문법이 적용되지 않음</span>
- 방법(1) : 4칸의 공백 또는 1개의 탭 사용
- 방법(2) : 백틱(```)
  <details>
      <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>
    🔹기본

  ````
  ```
  코드블록 만들기😉
  ```
  ````

  ```
  코드블록 만들기😉
  ```

  🔹응용

  ````
  ```javascript
  // 특정 프로그래밍 언어 지정 시
  // 문법 강조(styntax highlighting) 적용
  console.log("Seonyoung")
  ```
  ````

  ```javascript
  // 특정 프로그래밍 언어 지정 시
  // 문법 강조(styntax highlighting) 적용
  console.log("Seonyoung");
  ```

    </details>

### 7️⃣ 수평선

- 세 개 이상의 -, \*, \_ 를 사용하여 수평선을 만들 수 있다.
  <details>
    <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

  ```
  ---
  - - -
  ***
  ___
  ```

  ***

  ***

  ***

  ***

      </details>

### 8️⃣ 링크

- 인라인 링크 : [텍스트] 뒤에 (URL)를 직접 입력
  <details>
      <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

  ```
  [예시링크](link_URL "선택적 제목")
  [깃허브](https://github.com/ "깃허브홈페이지연결")
  ```

  [예시링크](link_URL "title")  
   [깃허브](https://github.com/ "깃허브홈페이지연결")

    </details>

- 참조 스타일 링크 : 링크를 문서 아래쪽에서 따로 관리하는 방식으로, 가독성이 높아짐  
  <span style="color:#FF4858;">❗참조할 링크를 문서 아래쪽에 위치시켜야 사용 가능</span>

    <details>
      <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

  🔹링크 정의를 통한 사용

  ```
  [깃허브][Github]에 연결됩니다!

  ❗하단에 참조링크 위치되어 있어야 함
  [Github]: link_URL "깃허브홈페이지연결"
  ```

  [깃허브][Github]에 연결됩니다!

  🔹단축키를 통한 사용  
   <span style="font-size:0.875rem">\- 단축키 생략 시 링크 텍스트 자체가 식별자로 사용</span>

  ```
  [구글][id]에 연결됩니다!
  [id]에 연결(이 id는 google.com으로 정의되어 있음)

  ❗하단에 참조링크 위치되어 있어야 함
  [id]: link_URL "구글홈페이지연결"
  ```

  [구글][id]에 연결됩니다!  
   [id]에 연결

    </details>

### 9️⃣이미지

#### 링크와 비슷하나 맨 앞에 "!" 추가

- 인라인 이미지 : 이미지 파일 경로로 이미지 직접 삽입

  <details>
      <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

  ```
  ![햄터](파일경로)
  ![망그러진곰](파일경로 "title사용 시 이미지에 마우스 올렸을 때 문구표시")
  ```

  ![햄터](../assets/images/mh.jpg) ![망그러진곰](../assets/images/mh2.jpg "오토바이타는 햄터귀여워")

    </details>

- 링크 이미지 : 이미지 URl을 통한 이미지 삽입

  <details>
      <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

  ```
  ![망곰이귀여워](img_URL)
  ```

  ![망곰이귀여워](https://mblogthumb-phinf.pstatic.net/MjAyNDA0MDFfMTQ4/MDAxNzExOTQ1NTI2Nzc2.6nIwAVgdrCKOGo4sqQduEBZ-w3WScl5NraMBhFfbLTAg.vFq11mDNrbmjOL3QW3JJ3aYWHt6fwBOTpCzU8_ETo3kg.PNG/2.png?type=w800)

    </details>

- 이미지 태그 사용 시 크기 조정 가능
  <details>
    <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

  ```
  <img src="파일경로 또는 img_URL" alt="이미지관련정보" width="100" height="100" >
  ```

  <img src="../assets/images/yurang.jpg" alt="울면서공부하는망곰이" width="100" height="100" >
  <img src="https://mblogthumb-phinf.pstatic.net/MjAyNDA0MDFfMTQ4/MDAxNzExOTQ1NTI2Nzc2.6nIwAVgdrCKOGo4sqQduEBZ-w3WScl5NraMBhFfbLTAg.vFq11mDNrbmjOL3QW3JJ3aYWHt6fwBOTpCzU8_ETo3kg.PNG/2.png?type=w800" width="100" height="100">
  </detail>

- 이미지를 링크로 사용하기
    <details>
      <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

  ```
  [![alt text](파일경로 또는 img_URL)](link_URL)
  <a href="link_URL">
    <img src="파일경로 또는 img_URL" alt="이미지관련정보" width="200px">
  </a>
  ```

  [![alt text](../assets/images/elephant.jpg)](https://github.com)
  <a href="https://github.com/">
  <img src="../assets/images/rabbit.jpg" alt="토끼탈을쓴망곰이" width="100px">
  </a>
  </detail>

### 🔟 체크리스트

- 완료된 항목은 [x]로 표시
- 미완료된 항목은 [ ]로 표시
  <details>
    <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

  ```
  - [x] 완료된 항목
  - [ ] 미완료된 황목
  ```

  - [x] 완료된 항목
  - [ ] 미완료된 황목  
         </detail>

### ⏸️ 테이블

- 기본 테이블 : 헤더 셀을 구분하려면 3개 이상의 `-`(하이픈)을 사용하고, 셀 구분은 `|`로 함

  <details>
    <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

  ```
  | 헤더1 | 헤더2 | 헤더3 | 헤더4 |
  | ---   | ---   | ---   | ---   |
  | 셀1   | 셀2   | 셀3   | 셀4   |
  | 셀5   | 셀6   | 셀7   | 셀8   |
  | 셀9   | 셀10  | 셀11  | 셀12  |

  ```

  | 헤더1 | 헤더2 | 헤더3 | 헤더4 |
  | ----- | ----- | ----- | ----- |
  | 셀1   | 셀2   | 셀3   | 셀4   |
  | 셀5   | 셀6   | 셀7   | 셀8   |
  | 셀9   | 셀10  | 셀11  | 셀12  |

  </detail>

- 정렬된 테이플 : `:` 를 사용하여 각 열의 정렬을 지정할 수 있음
    <details>
      <summary style="color:#0099DD; font-weight:600">마크다운 문법</summary>

  ```
  | 헤더1 | 헤더2  | 헤더3  |
  | :---  | :---:  | ---:   |
  | Left  | Center | Right  |
  | 1     | 2      | 3      |
  | 4     | 5      | 6      |
  | 7     | 8      | 9      |
  ```

  | 헤더1 | 헤더2  | 헤더3 |
  | :---- | :----: | ----: |
  | Left  | Center | Right |
  | 1     |   2    |     3 |
  | 4     |   5    |     6 |
  | 7     |   8    |     9 |

    </detail>

---

> #### 참고 사이트🖥️
>
> - [daringfireball](https://daringfireball.net/projects/markdown/syntax "마크다운참조")

<!-- 8. 링크 정의 -->

[Github]: https://github.com "깃허브홈페이지연결"
[id]: https://google.com "구글홈페이지연결"

# Atom

<br>


## 0. 참고 링크
* 다운로드 : https://atom.io/
* 단축키 및 설정 : http://naradesign.net/wp/2016/10/12/2212/
* Atom 스니펫 설정 : http://recoveryman.tistory.com/237


<br>

## 1. 기본 정보
* 프로젝트 추가 : File > Add Project Folder
* 사이드바 : View > Toggle Tree View (Sidebar Toggle)
* 셋팅 : `File > Settings (windows)` | `Atom > Preferences (mac)`
* package 검색 : Settings > install > packages 검색
* 설치된 package 확인 : settings > packages


<br>

## 2. 기본 단축키 및 설정

| 기능                  | 단축키                                      |
| ------------------- | ---------------------------------------- |
| Settings            | `ctrl` + `,`                             |
| Tree View (사이드바) 보기 | `ctrl` + `\`                             |
| 멀티 커서               | `Ctrl` + 클릭                              |
| 동일 구문 찾기(멀티블럭 상태)   | 블럭 지정 후, `Ctrl` + `d`                    |
| 자동 줄바꿈              | Setting (`ctrl` + `,`) > Editor > Soft Wrap |

<br>


## 3. 테마 설정
* 테마 설치 : Settings > install > themes 검색
* 테마 선택 : Settings > themes > UI Theme / Syntax Theme
* 추천테마 : one dark (기본)


<br>

## 4. 단축키 수정

(1) Setting (`Ctrl` + `,` ) > Keybindings > 필요한 기능 검색
* Keystroke 목록 앞의 아이콘을 클릭하여 해당 코드 복사


(2) `(1)` 상단의 your keymap file 링크 클릭 or File > Keymap 클릭
* keymap.cson 파일에 `(1)` 에서 복사한 코드 붙여넣기

  ```cson
  'atom-text-editor:not([mini])':
  	'ctrl-e': 'emmet:expand-abbreviation'
  	'ctrl-shift-w': 'emmet:wrap-with-abbreviation'

  'atom-workspace, atom-workspace atom-text-editor':
  	'ctrl-shift-M': 'markdown-preview-plus:toggle'
  	'ctrl-shift-X': 'markdown-preview-plus:toggle-render-latex'
  ```

* cf) `ctrl-shift-w` 기본 값이 아톰을 닫는 단축키이므로 의도치 않게 에디터가 꺼지는 것을 막기 위해 Emmet의 wrap width abbreviation 의 단축키로 지정


<br>

## 5. 주요 package 모음

! 지나치게 많은 package를 설치할 경우, 프로그램이 느려질 수 있으니 주의



### 5-1. emmet
	코드 자동완성 기능
	cheat-sheet 읽어보고 눈에 익힐 것

* cheat-sheet : http://docs.emmet.io/cheat-sheet/





### 5-2. atom-live-server
	라이브 서버실행


### 5-3. open-in-browsers
	멀티 브라우저 지원


### 5-4. PlatformIO IDE Terminal

```
터미널 패키지
```

* 터미널 toggle 단축키 : ctrl + `


* 상세설명 : https://atom.io/packages/platformio-ide-terminal



### 5-5. color-picker
	ctrl + alt + c


### 5-6. pigments
	A package to display colors in project and files.

* 설명 : https://atom.io/packages/pigments


### 5-7. indent-guide-improved
	탭 세로 안내선 추가


### 5-8. linter-htmlhint / linter-csshint
	linter-htmlhint : Atom 내에서 자동으로 html 유효성 검사
	linter-csshint : Atom 내에서 자동으로 CSS 유효성 검사

* 위 두 개의 패키지중 하나를 설치한 후, Atom 을 다시 실행하면 의존 패키지 설치 여부를 묻는다.
  * 의존 패키지 : `linter`, `linter-ui-default`
* 순차적으로 의존 패키지 설치



### 5-9. aligner
	멀티라인 정렬
	Easily align multi-line with support for different operators and custom configurations
	Ctrl + alt + /



### 5-10. space-tab
	탭을 스페이스로 스페이스를 탭으로 변경
	Ctrl + Alt + [
	Ctrl + Alt + ]



### 5-11. DocBlockr
	Docblock completion
	주석을 쉽게 만들어 주는 기능
	jsDoc 등의 형식을 빠르게 만들어 준다.

* 설명 : https://atom.io/packages/docblockr


### 5-12. Markdown Preview Plus (MPP)
	마크다운 파일 프리뷰
	Ctrl + Shift + m : 프리뷰 토글
	Ctrl + Shift + x : Math Rendering 토글
	단축키를 사용하려면 keymap.cson 파일에 해당 내용 추가

### 5-13. date
	현재 날짜, 시간 입력, 형식 셋팅 가능


* 기본 셋팅
  * 형식참고 : https://date-fns.org/docs/format
  * Date Format : YYYY-MM-DD
  * Time Format : HH:mm
  * Date Time Form : YYYY-MM-DD HH:mm


* 단축키 설정 (keymap.cson)
  ```json
  'atom-text-editor':
    'ctrl-d': 'date:date'
    'ctrl-shift-d': 'date:time'
    'ctrl-shift-alt-d': 'date:datetime'
  ```

<br>

## 6. 개인 셋팅 상황

* `File > Config` :  `File > Setting` 에서 수정한 내용이 config.cson 파일로 설정되어 있으며 직접 수정 가능.

  * 개인 셋팅 상황 (변경 중)

  ```json
  "*":
    "atom-package-deps":
      ignored: [
        "linter-ui-default"
      ]
    core:
      telemetryConsent: "no"
      themes: [
        "one-dark-ui"
        "base16-tomorrow-dark-theme"
      ]
    date:
      dateFormat: "YYYY-MM-DD"
      dateTimeFormat: "YYYY-MM-DD HH:mm"
    editor:
      fontSize: 12
      invisibles:
        cr: ""
        eol: ""
      preferredLineLength: 400
      scrollPastEnd: true
      showIndentGuide: true
      showInvisibles: true
      softWrap: true
      tabLength: 4
      tabType: "hard"
    "exception-reporting":
      userId: "8cdcead5-8d36-40bd-b647-aa29ff5a9f69"
    "linter-ui-default":
      panelHeight: 113
      showPanel: true
    minimap:
      charHeight: 1
    welcome:
      showOnStartup: false
    whitespace:
      ignoreWhitespaceOnCurrentLine: false
  ```


* `File > Keymap`
  * keymap.cson 파일을 수정하여 에디터의 바로가기 키 설정 변경

  ```json
  'atom-text-editor':
    'ctrl-k ctrl-k': 'editor:upper-case'
    'ctrl-k ctrl-l': 'editor:lower-case'
    'ctrl-shift-alt-m': 'markdown-preview:toggle'
    'ctrl-d': 'date:date'
    'ctrl-shift-d': 'date:time'
    'ctrl-shift-alt-d': 'date:datetime'
  ```

* `File > Snippets`
  * snippets.cson 파일을 수정하여 스니펫 설정

  ```json
  '.source.css':
    '가상선택자 after를 사용한 플롯 해제':
    'prefix': 'clear'
    'body': 'after {content:\'\'; display:block; visibility:hidden; clear:both; overflow:hidden; width:0; height:0;}'
  ```


* `File > Stylesheet`

  * style.less 파일을 수정하여 에디터의 스타일을 변경할 수 있다.
  * ex) 커서 수정

  ```less
  // style the background color of the tree view
  .tree-view {
    // background-color: whitesmoke;
    background-color: #111;
  }

  // style the background and foreground colors on the atom-text-editor-element itself
  atom-text-editor {
    // color: white;
    // background-color: hsl(180, 24%, 12%);
    background-color: #111;
  }

  // style UI elements inside atom-text-editor
  atom-text-editor .cursor {
    // border-color: red;
    border-width: 2px;
    border-color: #9ad392;
  }
  ```



<br>

---

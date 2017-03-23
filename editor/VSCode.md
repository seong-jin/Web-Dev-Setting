# Visual Studio Code

<br>

## 0. 참고링크
* 다운로드 : https://code.visualstudio.com/
* Documentation : https://code.visualstudio.com/docs
* 각종 확장 검색 : https://marketplace.visualstudio.com/VSCode


<br>

<br>



## 1. 주요 확장 모음



<details>

<summary>주요 확장 세부 정보</summary>



### 1-1. View In Browser
* 브라우저 보기 : `Ctrl` + `F1`
* 브라우저 셋팅 : 파일 > 기본 설정 > 설정
  ```json
  {
    "view-in-browser.customBrowser": "firefox"
  }

  // 브라우저 : firefox, chrome, iexplore, Safari
  // mozilla 인식되지 않고 firefox 로 인식됨
  ```
  cf) Firefox 로 파일을 열 때는 `mozilla` 또는 `firefox`로 값을 넣어줄 것


<br>



### 1-2. ESLint

* 문법 오류 감지

<br>




### 1-3. Guides
* Tab 세로 가이드 라인

<br>




### 1-4. Sass
* Sass 구문강조, 자동완성 및 기본 스니펫 제공


* Snippets
  * `var` : declare a new variable
  * `mixin` : declare a new mixin
  * `if` : base for an @if statement
  * `for` : base for a @for loop
  * `each` : base for a @each loop
  * `while` : base for a @while loop




<br>

### 1-5. vetur

* Vue.js  구문 강조
* `.vue` 파일이 아닐 경우, 기본적으로 구문 강조 적용 안됨




#### ◎ 구문 강조 설정 방법

1. 우측 하단의 `언어모드 선택` 클릭 
2. 명령창에 `vue` 입력
3. `HTML` 파일일 경우 `Vue-html` 선택
   * 언어모드가 `HTML` 에서 `Vue-html` 로 변경된다.
4. 그 외의 파일에서 구문 강조를 확인 하려면 언어 모드를  `Vue` 를 선택한다.



<br>

### 1-6. Path Intellisense

- 파일 경로 및 파일명 자동완성 기능



<br>

### 1-7. Align

- 텍스트 정렬 및 다중 커서 정렬


- `ctrl` + `alt` + `a`



<br>



### 1-8. Document This

* JSDoc 을 위한 주석문 생성
* _"Document This"_ is a Visual Studio Code extension that automatically generates detailed _**JSDoc comments**_ for both TypeScript and JavaScript files.
* 설명 : https://marketplace.visualstudio.com/items?itemName=joelday.docthis




#### 1-8-1. Tags

Supports JSDoc and Closure Compiler tags :

> @class, @description, @enum, @export, @function, @implements, @interface, @param, @private, @returns, @static, @template, @type and @memberOf.



#### 1-8-2. Document This

`Ctrl` + `Alt` + `D` + `D`

> Generates documentation for whatever the caret is on or inside of.




#### 1-8-3. Document Everything
`Ctrl` + `Alt` + `D` + `E`
> Generates documentation for all symbols that are supported by the extension.



#### <s>1-8-4. Document Everything Visible</s>

`Ctrl` + `Alt` + `D` + `V`

> Generates documentation for exported, public and protected symbols in the document.



<br>



### 1-9. Color Picker

- [3. 단축키 설정](#3-단축키-설정) 에서 단축키 변경
  - 변경 전 : Alt + C  P
  - 변경 후 :  `Alt` + `C` + `P`

<br>





### 1-10. TabSpacer

| 단축키                    | 기능 설명             |
| ---------------------- | ----------------- |
| `Ctrl` + `Shift` + `S` | 공백을 탭으로 변경        |
| `Ctrl` + `Shift` + `T` | 탭을 공백으로 변경        |
| `Ctrl` + `Shift` + `Z` | 탭모양 - 탭/공백 토글로 지정 |



<br>

### 1-11. Insert Date String

* 현재 날짜(및 시간)를 자동으로 표시
* 기본 단축키 : `ctrl` + `shift` + `i` 


* [2. 기본 설정 수정](#2-기본-설정-수정) 에서 기본 날짜형식 변경
  * 변경 전 : `YYYY-MM-DD hh:mm:ss`
  * 변경 후 : `YYYY-MM-DD` 
* 날짜 형식변경 및 날짜입력 : `ctrl` + `shift` + `alt` + `i`  입력 후, 명령창에서 형식 변경




<br>



### 1-12. vscode-icons

* VS Code Icons theme
* 탐색기 및 탭의 아이콘 변경



<br>

### 1-13. Autoprefixer 

* CSS 벤더 프리픽스를 자동으로 붙여주는 플러그인
* 참고 URL
  * https://github.com/postcss/autoprefixer 
  * https://twitter.com/autoprefixer



</details>

<br><br>



## 2. 기본 설정 수정

<details>

<summary>기본 설정 수정 세부 정보</summary>



### 2-1. 기본 설정 확인 

1. 파일 > 기본 설정 > 설정
2. `setting.json` 
   * 좌측 : 기본 설정 (변경 안됨)
   * 우측
     *  `사용자 설정` : 언어 식별자 집합에 대해 재정의할 설정을 구성합니다.
     *  `작업 영역 설정` : 설정을 이 파일에 넣어서 기본 설정과 사용자 설정을 덮어씁니다.
3. 각자 스타일로 셋팅
   * `기본 설정`에서 설정값 가져오기
     * ​원하는 설정에 마우스 오버시 보이는 `연필 아이콘` :pencil2:  클릭
     * 변경하고 싶은 설정값 클릭
     * 우측의 사용자 설정에 자동으로 수정된 설정값이 추가된다.
   * `사용자 설정` 에 직접 입력

<br>



### 2-2. 사용자 설정에 추가한 코드

```json
{
  "[]": {},

  "editor.tabSize": 2,
  "editor.lineHeight": 20,
  "window.zoomLevel": 1,
  "files.trimTrailingWhitespace": true,
  "editor.wordWrap": "on",
  "editor.renderWhitespace": "all",
  "editor.renderControlCharacters": true,
  "editor.insertSpaces": false,
  "editor.renderIndentGuides": false,
  "view-in-browser.customBrowser": "chrome",
  "emmet.triggerExpansionOnTab": false,
  "emmet.syntaxProfiles": {},
  "insertdatestring.format": "YYYY-MM-DD",
  "workbench.activityBar.visible": true,
  "editor.minimap.enabled": true,
  "editor.minimap.renderCharacters": true,
  "editor.minimap.maxColumn": 40,
  "workbench.iconTheme": "vscode-icons",
  "editor.fontFamily": "Consolas, 'Courier New', monospace",
  "vsicons.projectDetection.autoReload": true
}
```



<br>

### 2-3. Programming Language 별 셋팅 방법

**◎ 참고자료** : [Language specific editor settings](https://code.visualstudio.com/docs/customization/userandworkspace#_language-specific-editor-settings)

ex) `tabSize`를 **기본** 2로 하고 **JavaScript** 에서는 4로 하고 싶을 때

```json
{
  "editor.tabSize": 2,
  
  "[javascript]": {
    "editor.tabSize": 4
  }
}
```



</details>

<br><br>



## 3. 단축키 설정

<details>

<summary>단축키 설정 세부 정보</summary>



### 3-1. 단축키 설정 확인

1. 파일 > 기본 설정 > 바로 가기 키
2. `keybindings.json` 
   - 좌측 : `기본 키 바인딩` (변경 안됨)
   - 우측 : `keybindings.json`
3. 각자 스타일로 셋팅



#### ◎ 참고자료 :  [VS Code 기본 단축키 일람 PDF 문서](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)



### 3-2. keybindings.json 에 추가한 코드 


```
// 키 바인딩을 이 파일에 넣어서 기본값을 덮어씁니다.
[
  // emmet 실행
  { "key": "ctrl+e",
    "command": "editor.emmet.action.expandAbbreviation",
	"when": "editorTextFocus && !editorHasMultipleSelections && !editorHasSelection && !editorReadonly && !editorTabMovesFocus" },
  // 계산
  { "key": "ctrl+shift+y",
	"command": "editor.emmet.action.evaluateMath",
	"when": "editorHasCompletionItemProvider && editorTextFocus && !editorReadonly" },
  // 요소 감싸기
  { "key": "ctrl+w",
	"command": "editor.emmet.action.wrapWithAbbreviation",
	"when": "editorHasCompletionItemProvider && editorTextFocus && !editorReadonly" },

  // 블럭지정 또는 포커스된 문자 - 소문자로
  { "key": "ctrl+l ctrl+l",
	"command": "editor.action.transformToLowercase",
	"when": "editorTextFocus" },
  // 블럭지정 또는 포커스된 문자 - 대문자로
  { "key": "ctrl+l ctrl+k",
	"command": "editor.action.transformToUppercase",
	"when": "editorTextFocus" },

  // 컬러 피커 사용
  { "key": "alt+c alt+p",
	"command": "extension.colorHelper.pick",
	"when": "editorTextFocus" }

]
```



</details>

<br><br>



## 4. Snippet



<details>

<summary>Snippet 세부 정보</summary>

### 4-1. Snippet 설정




1.  명령어 창 열기
    * 파일 > 기본 설정 > 사용자 코드 조각 
    * `ctrl` + `shift` + `p` 
2.  `snippet` 검색 → `Preferences Snippets` 선택
3.  코드 조각의 언어 선택 : `html` ,  `javascript` 등 입력할 언어 선택
4.  해당 json 파일이 열리면 아래와 같은 형식으로 내용 수정



```
{
  // Place your snippets for HTML here. Each snippet is defined under a snippet name and has a prefix, body and
  // description. The prefix is what is used to trigger the snippet and the body will be expanded and inserted. Possible variables are:
  // $1, $2 for tab stops, $0 for the final cursor position, and ${1:label}, ${2:another} for placeholders. Placeholders with the
  // same ids are connected.
  // Example:
  "Print to console": {
  "prefix": "log",
  "body": [
  "console.log('$1');",
  "$2"
  ],
  "description": "Log output to console"
}
```



<br>

### 4-2. HTML Snippet



#### ◎ HTML5 기본 템플릿 : `html!`

```json
{
  "html5 doctype": {
    "prefix": "html!",
    "body": [
      "<!DOCTYPE html>",
      "<html lang=\"ko\">",
      "<head>",
      "<meta charset=\"UTF-8\">",
      "<meta name=\"viewport\" content=\"width=device-width, initial-scale=1.0\">",
      "<meta http-equiv=\"X-UA-Compatible\" content=\"ie=edge\">",
      "<title>$1</title>",
      "</head>",
      "<body>",
      "$2",
      "</body>",
      "</html>"
    ],
    "description": "html5 doctype"
  }
}
```



<br>

#### ◎ Vue 기본 템플릿 :  `vue!`

```json
{
  "html5 vue template": {
    "prefix": "vue!",
    "body": [
      "<!DOCTYPE html>",
      "<html lang=\"ko\">",
      "<head>",
      "<meta charset=\"UTF-8\">",
      "<meta name=\"viewport\" content=\"width=device-width, initial-scale=1.0\">",
      "<meta http-equiv=\"X-UA-Compatible\" content=\"ie=edge\">",
      "<title>$1</title>",
      "<style>",
      "	[v-cloak] {display:none;}",
      "</style>",
      "<!-- Vue JS 로드 -->",
      "<script src=\"https://unpkg.com/vue\"></script>",
      "</head>",
      "<body>",
      "",
      "<!-- root vue instance → mounted elementNode -->",
      "<div id=\"app\">",
      "	",
      "</div>",
      "",
      "",
      "<script>",
      "var vm = new Vue({",
      "	el: '#app',",
      "	data: {",
      "		",
      "	}",
      "});",
      "</script>",
      "</body>",
      "</html>"
    ],
    "description": "html5 Vue template"
  }
}
```



<br>



### 4-3. JavaScript Snippet



#### ◎ console.log 기본 템플릿 : `log!`

```json
{
  "Print to console": {
    "prefix": "log!",
    "body": [
      "console.log('$1');",
      "$2"
    ],
    "description": "Log output to console"
  }
}
```



<br>

#### ◎ function 기본 템플릿 : `fun!` / `func!`

```json
{
  "Print to basic function": {
    "prefix": "fun!",
    "body": [
      "function() {",
      "	$1",
      "}"
    ],
    "description": "Make Basic function"
  },

  "Print to common function ": {
    "prefix": "func!",
    "body": [
      "function $1 ($2) {",
      "	",
      "}"
    ],
    "description": "Make common function"
  }
}
```



<br>

#### ◎ IIFE Pattern 기본 템플릿 : `iife!`

```json
{
  "Print to IIFE": {
    "prefix": "iife!",
    "body": [
      "(function(global){",
      "	'use strict';",
      "		$1",
      "	});",
      "})(window);"
    ],
    "description": "Make Basic IIFE"
  }
}
```



</details>



<br><br>









---


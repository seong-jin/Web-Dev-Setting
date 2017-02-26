# Visual Studio Code



## 0. 참고링크
* 다운로드 : https://code.visualstudio.com/
* Documentation : https://code.visualstudio.com/docs
* 각종 확장 검색 : https://marketplace.visualstudio.com/VSCode






## 1. 주요 확장 모음



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


-

### 1-2. ESLint
	문법 오류 감지
-


### 1-3. Guides
	Tab 세로 가이드 라인
-


### 1-4. Sass
```
Indented Sass syntax highlighting, autocomplete & snippets for VSCode
```

* Snippets
  ```
  Snippets have been reduced to a few time savers.

  var - declare a new variable
  mixin - declare a new mixin
  if - base for an @if statement
  for - base for a @for loop
  each - base for a @each loop
  while - base for a @while loop
  ```


-

### 1-5. Color Picker

* 단축키 : Alt + C  P →  `Alt` + `C`  and after,  `Alt` + `P` 로 변경


-

### 1-6. Document This

* "Document This" is a Visual Studio Code extension that automatically generates detailed JSDoc comments for both TypeScript and JavaScript files.
* 설명 : https://marketplace.visualstudio.com/items?itemName=joelday.docthis



##### Functionality
Supports JSDoc and Closure Compiler tags :
	@class, @description, @enum, @export, @function, @implements, @interface, @param, @private, @returns, @static, @template, @type and @memberOf.


##### Document This
`Ctrl` + `Alt` + `D` and again `Ctrl` + `Alt` + `D`
	Generates documentation for whatever the caret is on or inside of.

##### Document Everything
`Ctrl` + `Alt` + `D` and after, `Ctrl` + `Alt` + `E`
	Generates documentation for all symbols that are supported by the extension.

##### Document Everything Visible
`Ctrl` + `Alt` + `D` and after `Ctrl` + `Alt` + `V`



	Generates documentation for exported, public and protected symbols in the document.


-



### 1-7. TabSpacer

| 단축키                    | 기능 설명             |
| ---------------------- | ----------------- |
| `Ctrl` + `Shift` + `S` | 공백을 탭으로 변경        |
| `Ctrl` + `Shift` + `T` | 탭을 공백으로 변경        |
| `Ctrl` + `Shift` + `Z` | 탭모양 - 탭/공백 토글로 지정 |



-

### 1-8. Insert Date String

```
Insert the current date and time according to configured format.
```

* 기본 날짜형식 : YYYY-MM-DD hh:mm:ss  →  `YYYY-MM-DD` 로 변경
* 기본 단축키 : `ctrl` + `shift` + `i` 
* 날짜 형식변경 및 날짜입력 : `ctrl` + `shift` + `alt` + `i`  입력 후, 명령창에서 형식 변경




-

### 1-9. Path Intellisense 

```
Visual Studio Code plugin that autocompletes filenames.

파일 경로 및 파일명 자동완성 기능
```



-



### 1-10. Align

```
Supports text alignment and multi-cursor alignment.
```

* `ctrl` + `alt` + `a`



-

## 2. 기본설정 수정
	파일 > 기본 설정 > 설정
	setting.json 의 사용자 설정 수정
	각자 스타일로 셋팅



```json
{
	"editor.tabSize": 2,
	"editor.lineHeight": 20,
	"window.zoomLevel": 1,
	"files.trimTrailingWhitespace": true,
	"editor.wordWrap": false,
	"editor.renderWhitespace": "none",
	"editor.renderControlCharacters": true,
	"editor.insertSpaces": false,
	"editor.wrappingColumn": 0,
	"editor.renderIndentGuides": false,
	"editor.cursorStyle": "underline",
	"view-in-browser.customBrowser": "chrome",
	"emmet.triggerExpansionOnTab": false,
	"emmet.syntaxProfiles": {},
	"insertdatestring.format": "YYYY-MM-DD",

	"[]": {}
}
```



**※ Programming Language 별 셋팅 방법** 

* 참고자료 : [Language specific editor settings](https://code.visualstudio.com/docs/customization/userandworkspace#_language-specific-editor-settings)

- ex) tabSize를 기본 2로 하고 javascript 에서는 4로 하고 싶을 때

```json
{
  "editor.tabSize": 2,
  
  "[javascript]": {
    "editor.tabSize": 4
  }
}
```







---








## 3. 단축키 설정 수정
	파일 > 기본 설정 > 바로가기키
	keybindings.json 수정
	각자 스타일로 셋팅

* 참고 자료 :  [VS Code 기본 단축키 일람 PDF 문서](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)



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



---



## 4. Snippet



* 파일 > 기본 설정 > 사용자 코드 조각



1.  명령어 창 열어 snippet 검색 :  `ctrl` + `shift` + `p`  snippet
2.  사용자 코드 조각 열기 - Preferences Snippets 선택
3.  html / javascript 등 언어 선택
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



* html 파일에서 `html!` 를 `HTML5 기본 템플릿` `스니펫`으로 설정한 코드

```json
{
	"html5 doctype": {
		"prefix": "html!",
		"body": [
			"<!DOCTYPE html>",
			"<html lang='ko'>",
			"<head>",
			"<meta charset='UTF-8'>",
			"<meta name='viewport' content='width=device-width, initial-scale=1.0'>",
			"<meta http-equiv='X-UA-Compatible' content='ie=edge'>",
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





---


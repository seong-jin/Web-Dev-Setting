# Atom




## 0. 참고 링크
* 다운로드 : https://atom.io/
* 단축키 및 설정 : http://naradesign.net/wp/2016/10/12/2212/
* Atom 스니펫 설정 : http://recoveryman.tistory.com/237




## 1. 기본 정보
* 프로젝트 추가 : File > Add Project Folder
* 사이드바 : View > Toggle Tree View (Sidebar Toggle)
* 셋팅 : `File > Settings (windows)` | `Atom > Preferences (mac)`
* package 검색 : Settings > install > packages 검색
* 설치된 package 확인 : settings > packages




## 2. 기본 단축키 및 설정

| 기능                  | 단축키                                      |
| ------------------- | ---------------------------------------- |
| Settings            | `ctrl` + `,`                             |
| Tree View (사이드바) 보기 | `ctrl` + `\`                             |
| 멀티 커서               | `Ctrl` + 클릭                              |
| 동일 구문 찾기(멀티블럭 상태)   | 블럭 지정 후, `Ctrl` + `d`                    |
| 자동 줄바꿈              | Setting (`ctrl` + `,`) > Editor > Soft Wrap |




## 3. 테마 설정
* 테마 설치 : Settings > install > themes 검색
* 테마 선택 : Settings > themes > UI Theme / Syntax Theme
* 추천테마 : one dark (기본)




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


### 5-4. color-picker
	ctrl + alt + c


### 5-5. pigments
	A package to display colors in project and files.

* 설명 : https://atom.io/packages/pigments





### 5-6. indent-guide-improved
	탭 세로 안내선 추가


### 5-7. linter-htmlhint
	Atom 내에서 자동으로 html 유효성 검사


### 5-8. aligner
	멀티라인 정렬
	Easily align multi-line with support for different operators and custom configurations
	Ctrl + alt + /



### 5-9. space-tab
	탭을 스페이스로 스페이스를 탭으로 변경
	Ctrl + Alt + [
	Ctrl + Alt + ]



### 5-10. DocBlockr
	Docblock completion
	주석을 쉽게 만들어 주는 기능
	jsDoc 등의 형식을 빠르게 만들어 준다.

* 설명 : https://atom.io/packages/docblockr




### 5-11. Markdown Preview Plus (MPP)
	마크다운 파일 프리뷰
	Ctrl + Shift + m : 프리뷰 토글
	Ctrl + Shift + x : Math Rendering 토글
	단축키를 사용하려면 keymap.cson 파일에 해당 내용 추가



---


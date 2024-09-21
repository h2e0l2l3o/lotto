# 로또 번호 생성기
랜덤으로 로또 번호 생성하는 웹페이지

## 스타일
- `box-shadow`: CSS에서 요소에 그림자를 추가할 때 사용하는 속성 (여러 값을 받을 수 있으며, 각각의 값은 그림자의 위치, 흐림 정도, 퍼짐 정도 등을 설정)

    ```css
    box-shadow: [offset-x] [offset-y] [blur-radius] [spread-radius] [color];
    ```

    + offset-x: 그림자의 가로 방향 거리. 양수일 경우 오른쪽으로, 음수일 경우 왼쪽으로 이동.
    + offset-y: 그림자의 세로 방향 거리. 양수일 경우 아래쪽으로, 음수일 경우 위쪽으로 이동.
    + blur-radius (선택 사항): 그림자의 흐림 정도. 값이 클수록 그림자가 더 부드럽게 퍼짐.
    + spread-radius (선택 사항): 그림자의 확산 정도. 양수면 그림자가 확산되고, 음수면 축소됨.
    + color (선택 사항): 그림자의 색상. 생략 시 기본값은 요소의 텍스트 색상.

    - inset 속성: 기본적으로 그림자는 요소 외부에 표시되지만, inset 키워드를 사용하면 그림자를 요소 내부로 적용 가능.

- `animation`: CSS 요소에 애니메이션 효과 적용할 때 사용. @keyframes로 정의한 애니메이션을 어떻게 적용할지를 설정하는 속성.
  + animation-name: 적용할 애니메이션의 이름 (keyframes에서 정의한 이름).
  + animation-duration: 애니메이션이 한 번 재생되는 시간을 설정 (예: 2s는 2초).
  + animation-timing-function: 애니메이션의 속도 변화를 설정 (기본값: ease, 옵션: linear, ease-in, ease-out 등).
  + animation-delay: 애니메이션이 시작되기 전 대기 시간을 설정 (예: 1s).
  + animation-iteration-count: 애니메이션이 반복되는 횟수를 설정 (infinite로 무한 반복 가능).
  + animation-direction: 애니메이션의 재생 방향을 설정 (normal, reverse, alternate 등).
  + animation-fill-mode: 애니메이션이 완료된 후에도 효과가 남는지 설정 (forwards, backwards 등).

- `@keyframes`: 애니메이션의 단계별 스타일 변화를 정의.
  + 0% ~ 100%: 애니메이션 진행 단계. 0%는 애니메이션의 시작, 100%는 끝을 의미


- `text-shadow`: CSS에서 텍스트에 그림자를 적용하는 속성
  + `text-shadow: [수평-오프셋] [수직-오프셋] [블러-반경] [그림자-색상];`
    - 수평-오프셋 (horizontal offset): 그림자가 텍스트에서 수평으로 얼마나 이동할지 설정 (양수: 오른쪽, 음수: 왼쪽).
    - 수직-오프셋 (vertical offset): 그림자가 텍스트에서 수직으로 얼마나 이동할지 설정 (양수: 아래, 음수: 위).
    - 블러 반경 (blur radius): 그림자가 얼마나 흐릿할지 설정 (값이 클수록 흐려짐, 선택 사항).
    - 그림자 색상 (shadow color): 그림자의 색상을 지정 (선택 사항, 기본은 텍스트 색상).

## **@** 뒤에 오는 거?? 

**CSS 규칙이나 디렉티브로, 특정 상황이나 조건에 따라 CSS 스타일을 적용하거나, 애니메이션, 미디어 쿼리 등을 설정할 때 사용**
아래는 요청하신 내용을 **마크다운 문법**으로 작성한 예시입니다.

### 1. `@media`
미디어 쿼리를 사용하여 화면 크기, 해상도, 기기 특성에 따라 다른 스타일을 적용할 수 있습니다.

**예시:**
```css
@media (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```
- 화면의 너비가 600px 이하일 때 `body`의 배경색을 변경.

---

### 2. `@keyframes`
애니메이션의 단계별 스타일 변화를 정의합니다.

**예시:**
```css
@keyframes fade-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```
- `fade-in` 애니메이션은 요소의 투명도(`opacity`)를 0에서 1로 변화시킵니다.

---

### 3. `@font-face`
사용자 정의 글꼴을 정의하여 웹페이지에서 사용합니다.

**예시:**
```css
@font-face {
  font-family: 'MyCustomFont';
  src: url('myfont.woff2') format('woff2');
}
```
- `MyCustomFont`라는 폰트를 정의하고, 이를 웹에서 사용.

---

### 4. `@import`
외부 스타일시트를 불러올 때 사용합니다.

**예시:**
```css
@import url('style.css');
```
- `style.css`라는 외부 스타일시트를 현재 CSS 파일에 불러옵니다.

---

### 5. `@supports`
브라우저가 특정 CSS 기능을 지원하는지 확인하고, 지원할 경우 스타일을 적용합니다.

**예시:**
```css
@supports (display: grid) {
  .container {
    display: grid;
  }
}
```
- 브라우저가 `grid`를 지원할 경우 `.container`에 `grid` 레이아웃을 적용.

---

### 6. `@page`
인쇄(media type: print)할 때 페이지의 레이아웃을 설정하는 데 사용됩니다.

**예시:**
```css
@page {
  margin: 1cm;
}
```
- 인쇄 페이지의 여백을 1cm로 설정.

---

### 7. `@charset`
CSS 파일의 문자 인코딩을 정의합니다. 일반적으로 파일의 맨 처음에 위치해야 합니다.

**예시:**
```css
@charset "UTF-8";
```
- CSS 파일이 UTF-8 인코딩을 사용하고 있음을 명시.

---

### 8. `@namespace`
XML 기반 문서에서 사용되는 CSS 선택자에 네임스페이스를 정의할 때 사용합니다.

**예시:**
```css
@namespace svg "http://www.w3.org/2000/svg";
svg|circle {
  fill: red;
}
```
- SVG 요소에 대한 네임스페이스를 정의하고, 특정 네임스페이스의 `circle` 요소에 스타일 적용.

---

### 9. `@counter-style`
사용자 정의 리스트 스타일을 만들 때 사용됩니다.

**예시:**
```css
@counter-style custom-list {
  system: numeric;
  symbols: '*' '**' '***';
  suffix: '. ';
}
```
- `custom-list`라는 이름의 사용자 정의 리스트 스타일을 정의.

---

### 10. `@viewport`
뷰포트 관련 속성을 설정할 때 사용됩니다. (특히 구형 IE 지원)

**예시:**
```css
@viewport {
  width: device-width;
  zoom: 1.0;
}
```
- 뷰포트의 너비를 장치의 너비에 맞추고, 초기 줌 레벨을 1로 설정.

## JS 
- `join`: join() 메서드는 **배열의 모든 요소를 문자열로 병합하여 반환**하며, 각 요소는 지정된 구분자(기본값은 콤마 ,)로 연결됨.
- `includes`: 배열에 특정 요소가 포함되어 있는지 여부를 확인(**true 또는 false**를 반환)
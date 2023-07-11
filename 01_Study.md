- git ignore 생성

```bash
$ npx add-gitignore node osx windows visualstudiocode
```
---
<details>
<summary> index.html 작성 </summary>

```html
<!DOCTYPE html>
<html lang="ko">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>UI 디자인(설계) with CSS 변수</title>
  <meta name="description" content="Figma의 로컬 변수를 CSS 변수로 변환해 개발에 활용">
</head>

<body>
  <div>
    modal dialog
  </div>
</body>

</html>
```
</details>

<details>
<summary>package.json 생성 후 수정</summary>

```bash
$ git init
```

```json
{
  "private": true,
  "name": "uix",
  "version": "1.0.0",
  "description": "디자인 → 개발 핸드오프 프로세스에 대해 학습합니다.",
  "scripts": {
    "serve": ""
  }
}
```
</details>

<details>
<summary>패키지 설치 후 package.json 수정</summary>

```bash
$ pnpm add -D live-server
```

```json
// package.json

{
  "scripts": {
    "serve": "live-server --host=localhost --port=3000 --no-browser"
  },
}
```
</details>

- 실행

```bash
$ pnpm serve
```
---
- 모듈 생성

<details>
<summary>variables.css</summary>

```css
/* src/main.css */

@import './variables.css'
```

```css
/* src/variable.css */

/* figma css 붙여넣기 */
```
</details>

<details>
<summary>normalize.css</summary>

- [Normalize.css](https://necolas.github.io/normalize.css/)

  - npm install

  ```bash
  $ npm install normalize.css
  ```

  - 붙여넣기

  ```css
  /* src/main.css */

  @import './initialize.css';
  ```

  ```css
  /* src/initialize.css */

  /* 스니펫을 사용해 붙여넣거나, 
  normalize
  사이트 코드 붙여넣기 */
  ```
</details>

<details>
<summary>base 코드</summary>

```css
/* src/main.css */

@import './base.css';
```

  - font 설정

  ```css
  /* src/base.css */

  :root {
    font-size: 10px;
    background-color: var(--color-white);
    box-sizing: border-box;

    & body {
      font: 1.6rem/1.5 Pretendard, sans-serif;
      color: var(--color-black);
    }
  }
  ```

  - nesting body

    Can I use css nesting? 검색 시

    Nesting의 경우 대부분의 브라우저가 지원하지만, Samsung Internet은 아직 지원하지 않음

  - button 설정

    enabled 버튼에 커서를 가져다 대면 pointer,

    disabled 버튼에 커서를 가져다 대면 not-allowed

    ```css
    /* src/base.css */

    button {
      cursor: pointer;

      &:disabled {
        cursor: not-allowed;
      }
    }
    ```
</details>

<details>
<summary>components.css</summary>

```css
/* src/main.css */

@import './components.css';
```

- 예시

```css
/* src/components.css */

.ModalDialog {
  background: var(--surface-secondary);
  color: var(--surface-brand);
}
```

```html
<!-- index.html -->
...
<div class="ModalDialog">
  <h1>modal dialog</h1>
  <button>button</button>
  <button disabled>button</button>
</div>
...
```
</details>

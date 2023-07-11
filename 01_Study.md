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
<summary>패키지 설치 후 package.json 수정</summary>mmary>

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
- css 파일 생성

```css
/* src/main.css */

@import './variables.css'
```

```css
/* src/variable.css */

/* figma css 붙여넣기 */
```
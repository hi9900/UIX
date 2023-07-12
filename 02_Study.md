- 마크업 부여

  > Tree 구조 보기
  >
  >  개발자 모드 패널: Accessibility -> 실험적 기능 체크 후 리로드하면 여러 기능이 표시됨
  >
  >  Tree 구조 보기: 우측 위 사람모양 아이콘

  - 디비전은 아무런 의미가 없기 때문에 의미를 부여해야 함

  - [WAI-ARIA](https://developer.mozilla.org/ko/docs/Web/Accessibility/ARIA)에 따르면 역할을 부여할 수 있음

  ```html
  <!-- index.html -->

  <div class="ModalDialog" role="dialog" aria-modal="true">
  </div>
  ```

  `role="dialog"`: dialog 역할 부여 

  `aria-modal="true"`: modal 기능의 상태를 가짐

---

- Figma VScode extension


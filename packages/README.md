# Stencil + Vue Integration
- ref : [stencil docs](https://stenciljs.com/docs/vue)
- example project set up like this:
    ```
    top-most-directory/
    └── packages/
        ├── vue-library/
        │   └── lib/
        │       ├── plugin.ts
        │       └── index.ts
        └── stencil-library/
            ├── stencil.config.js
            └── src/components
    ```

## 적용 결과
- stencil로 만든 컴포넌트를 활용하여 vue에 적용할 수 있음. => monorepo 형태
- lerna는 stencil로 만든 컴포넌트들을 하나로 묶어 vue 프로젝트에 연결해주는 정도의 역할만함
- stencil로 구성된 레포지토리가 있다면 이를 이용하여 구성해볼 수 있을 것 같음
- 그러나, 현재 우리 디자인 시스템의 구조로 활용하기에는 다소 복잡하다는 생각이 듦.

### 적절하지 않다고 느끼는 부분
- stencil을 이용하여 디자인 컴포넌트들을 만든 후, 동기화 과정이 번거롭게 느껴진다. 
    - 물론, 단순히 pull을 하면되긴 하지만 뭔가 이력 추적을 하기에 복잡하다고 느껴지니까..
    - 이것은 monorepo의 어쩔 수 없는 한계인가.
    - 단순히 사용성을 떠나서 프로젝트의 구조가 너무 커진다. 각각의 FE 레포마다 stencil 폴더가 중복으로 있다고? (물론 같은 라이브러리를 쓴다는 것도 비슷한 개념일지도...)
    
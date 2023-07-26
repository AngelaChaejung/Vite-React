- Vite의 장점!
  CRA 대신 Vite를 사용하면 개발할 때 속도가 더 빠르고 메모리도 적게 잡아먹게된다!

- 어떻게 시작하나요?

```
npm create vite@latest

or

yarn create vite

or

pnpm create vite
```

프로젝트 생성 후 `npm install`을 직접 해야함!

`npm run dev`

- Vite는 개발서버 포트가 3000이 아닌, 5173포트를 쓴다.
  localhost:5173로 접속!

- CRA는 webpack으로 번들링 하는데, 코드가 업데이트되면 자바스크립트 코드로 새로 번들링을 매번한다.
  그래서 앱이 커질 수록 느려지는데, Vite는 첫번재 실행에서 전체를 한번 번들링 한 후 변경된 부분만 새로 번들링을 한다.
  webpack은 NodeJs로 만들어졌고, esbuild는 Go로 만든 프로그램. (그래서 더 빠름)

- main.tsx가 시작점.

- 유의해야 할 차이점

  1.  절대경로로 import
      `import Cards from “/src/components/cards.jsx”`

  2.  환경 변수
      `VITE_API_KEY = 1234567890..`
      그리고 가져다 쓸 때도 `process.env.REACT_APP_API_KEY`가 아닌, `import.meta.env.VITE_API_KEY`

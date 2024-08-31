Welcome to Blink Me The Decentralised Buy Me a coffeee!!!!!!


## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.



:root {
  @apply bg-slate-900 leading-relaxed text-slate-400 antialiased selection:bg-teal-300 selection:text-teal-900 scroll-smooth;
  font-family: Inter, sans-serif;
  font-feature-settings: 'liga' 1, 'calt' 1; /* fix for Chrome */

  --secondary-glow: conic-gradient(
    from 10deg at 50% 50%,
    #eb7494 0deg,
    #4b3d9e 55deg,
    #97b5da 120deg,
    #0099ca 160deg,
    transparent 360deg
  );

  --third-glow: conic-gradient(
    from 90deg at 50% 50%,
    #ff8b7e 0deg,
    #6c54d6 160deg,
    #7ed2da 120deg,
    #46f171 55deg,
    transparent 360deg
  );
}

@supports (font-variation-settings: normal) {
  :root {
    font-family: InterVariable, sans-serif;
  }
}

body {
  @apply font-inter;
}

.main {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 40vh 0 0 0;
  min-height: 100vh;
}

.mainDiv {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-family: 'Prospect';
  font-size: 3rem;
}

.research {
  margin: 2rem 0;
  border-radius: 3vh;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  font-size: 1.5rem;
  font-family: 'Helvetica';
  padding: 0 1rem;
}

.line {
  background-color: black;
  display: flex;
  flex-direction: row;
  height: 50vh;
  width: 1px;
}
body::before,
body::after {
  content: '';
  position: absolute;
  z-index: -1;
  opacity: 0.8;
}

body::before {
  background: var(--third-glow);
  border-radius: 50%;
  width: 50vw;
  height: 50vw;
  margin-left: -200px;
  filter: blur(90px);
  top: calc(50vh - 50vw / 2);
  left: calc(50vw);
}

body::after {
  background: var(--secondary-glow);
  border-radius: 50%;
  width: 500px;
  height: 700px;
  filter: blur(90px);
  top: calc(50vh - 50vw / 2);
  left: calc(50vw - 50vw / 2);
}

@keyframes animateBefore {
  0% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(200px) scale(0.8);
  }
  100% {
    transform: translateY(0);
  }
}

@keyframes animateAfter {
  0% {
    transform: translateX(0);
  }
  50% {
    transform: translateX(-250px) scale(1.2);
  }
  100% {
    transform: translateX(0);
  }
}

body::before {
  /*...previous props*/
  animation: animateBefore 7s cubic-bezier(0.47, 0, 0.745, 0.715) infinite;
}

body::after {
  /*...previous props*/
  animation: animateAfter 7s cubic-bezier(0.47, 0, 0.745, 0.715) infinite;
}
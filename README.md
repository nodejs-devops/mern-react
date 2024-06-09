# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

```sh
npm create vite@latest .
```

```
React
Javascript
```

```sh
npm install
npm run dev

npm install --save-dev prettier eslint eslint-plugin-react eslint-config-prettier eslint-plugin-jsx-a11y
npx eslint src
npx eslint src --fix
npx eslint src
npm pkg set scripts.lint="eslint src"
npm run lint
npm install --save-dev husky lint-staged

git init -b master
git add package.json
git commit -am "chore: Initial commit"

npm pkg set scripts.prepare="husky install"
npm run prepare
npx husky add .husky/pre-commit "npx lint-staged"

git add .
git commit -m "chore: basic project setup"
```

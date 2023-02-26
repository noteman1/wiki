# NEXT.js 프로젝트 시작하기

```bash
npx create-next-app@latest --typescript
or
npx create-next-app@latest my-project --typescript --eslint

cd {project_name}
npm install --save-dev --save-exact prettier
echo {}> .prettierrc.json
```

```json
{
  "trailingComma": "es5",
  "tabWidth": 2,
  "semi": true,
  "singleQuote": true
}
```

```bash
npm install --save-dev eslint-config-prettier
```

.eslintrc.json
```json
{
  "extends": ["next/core-web-vitals", "prettier"]
}
```

## Saas

```bash
npm install --save-dev sass
```

## tailwindcss

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```
tailwind.config.js
```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./app/**/*.{js,ts,jsx,tsx}",
    "./pages/**/*.{js,ts,jsx,tsx}",
    "./components/**/*.{js,ts,jsx,tsx}",
 
    // Or if using `src` directory:
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
globals.css
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```
## extra
```bash
npm i classnames
```

## extra

```bash
npm install react-icons
npm install next-seo
npm install next-sitemap
```

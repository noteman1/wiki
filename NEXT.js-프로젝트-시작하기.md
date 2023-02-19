# NEXT.js 프로젝트 시작하기

```bash
npx create-next-app@latest --typescript

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

## extra

```bash
npm install react-icons
npm install next-seo
```

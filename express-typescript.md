```bash
mkdir {project_name}
cd {project_name}
npm init -y
npm i express morgan
npm i -D nodemon typescript ts-node @types/node @types/express @types/morgan
npx tsc --init
```

```json
"script": {
  "start": "ts-node src/index.ts",
  "dev": "nodemon --exec ts-node src/index.ts"
}
```
```bash
mkdir {project_name}
cd {project_name}
npm init -y
npm i express morgan
npm i -D nodemon typescript ts-node @types/node @types/express @types/morgan
npx tsc --init
```

package.json
```json
"script": {
  "start": "ts-node src/index.ts",
  "dev": "nodemon --exec ts-node src/index.ts"
}
```

## DATABASE
```bash
npm i pg typeorm reflect-metadata
npm i bcryptjs class-validator class-transformer
npm i -D @types/bcryptjs
```

initial typeorm and config
```
npx typeorm init --name MyProject --database postgres
```
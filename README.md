# Express + TypeScript Starter

This project is a simple Express server built with TypeScript. It includes basic setup instructions, configuration files, and development scripts.

## Installation

```bash
npm init -y
npm install express --save
npm install -D typescript
npx tsc --init
npm install --save-dev @types/express
```

## Project Structure

```
project-folder/
├── src/
│   └── server.ts
├── dist/
├── tsconfig.json
└── package.json
```

## tsconfig.json

Below is the configuration used in this project:

```json
{
  "compilerOptions": {
    "rootDir": "./src",
    "outDir": "./dist",
    "module": "nodenext",
    "target": "esnext",
    "types": [],
    "noUncheckedIndexedAccess": true,
    "exactOptionalPropertyTypes": true,
    "strict": true,
    "isolatedModules": true,
    "noUncheckedSideEffectImports": true,
    "moduleDetection": "force",
    "skipLibCheck": true
  }
}
```

## Server Code (server.ts)

```ts
import express, { Request, Response } from "express";

const app = express();
const port = 5000;

app.get("/", (req: Request, res: Response) => {
  res.send("Hello World!");
});

app.listen(port, () => {
  console.log(`Example app listening on port ${port}`);
});
```

## package.json Scripts

```json
{
  "scripts": {
    "dev": "npx tsx watch ./src/server.ts"
  }
}
```

## Run the Server

```bash
npm run dev
```

The server will start on port **5000**.

## Notes

* `tsx` is used for fast TypeScript execution in development.
* Build output will appear in the `dist` folder when using `tsc`.

Happy coding!

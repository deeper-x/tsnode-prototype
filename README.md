# tsnode-prototype
Typescript project on node/vscode - first configuration:

1. npm init -y
2. mkdir lib; mkdir src;
3. npm install typescript @types/node ts-node nodemon tslint
4. npx tsc --init --rootDir src --outDir lib --esModuleInterop --target es6 --lib 'es6, dom' --module commonjs
5. touch src/index.ts
6. tslint --init (tslint usually in: ./node_modules/tslint/bin/tslint)
7. edit package.json: 

```
"scripts": {
"start": "npm run build:live",
"build": "tsc -p .",
"build:live": "nodemon --watch 'src/**/*.ts' --exec 'ts-node' src/index.ts"
}
```
# Run
1. npm start

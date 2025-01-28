## Reproduce Error
```bash
cd ./theme/
npm pack
cp my-theme-0.0.0.tgz ../page/my-theme-0.0.0.tgz
cd ../page/
npm install
npm run docs:dev // works
npm run docs:build // error
```
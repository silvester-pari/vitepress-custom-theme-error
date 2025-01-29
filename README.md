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
## Issue discussion
https://github.com/vuejs/vitepress/issues/4529

## Solution
https://github.com/vuejs/vitepress/issues/4529#issuecomment-2619825367
```js
// page/.vitepress/config.mjs
[...]
vite: {
  ssr: {
    noExternal: ['my-theme']
  }
}
```

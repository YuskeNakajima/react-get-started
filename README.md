<h1 style="text-align: center;">Reactの始め方</h1>

## プロジェクト作成
```bash
yarn create vite
```
- react
- typescript

## ルートディレクトリからパス指定できるようようにする
### tsconfig.json
追記
- compilerOptions.baseUrl
- compilerOptions.paths
```json
{
  "compilerOptions": {
    "baseUrl": ".",
    "paths": {
      "@/*": ["src/*"]
    }
  }
}
```

### vite.config.ts
resolveを追記
```typescript
export default defineConfig({
    plugins: [react()],
    resolve: {
        alias: [{find: '@', replacement: '/src'}]
    }
})
```

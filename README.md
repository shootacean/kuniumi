# Kuniumi

- https://kenall.jp/
- [ ] TDDで都道府県取得APIをつくる
- [ ] テストコードを書く
- [ ] どっかの都道府県マスタデータから都道府県マスタテーブルをつくるCLIを実装する

[開発ドキュメント雑まとめ](https://zenn.dev/mssknd/scraps/ea69fdd71c6c71)

## Architecture
- TypeScript
- NestJS
- TypeORM
- Open API
- gRPC
- GraphQL

## Log

やったことを残していく

### NestJSをインストールする

```fish
$ pnpm dlx nest new kuniumi
$ pnpm i
$ pnpm run start:debug
$ curl localhost:3000
Hello World!
```

### pnpmでnodeのバージョンを管理する

- [pnpm env <cmd> | pnpm](https://pnpm.io/ja/cli/env)
- [.npmrc | pnpm](https://pnpm.io/ja/npmrc#package-import-method)

```fish
$ pnpm env use -g 16.17.0
$ echo 'use-node-version = 16.17.0' >> .npmrc
```

### サンプルコードにテストを入れる → すでに入ってる

```fish
$ pnpm run test
```

```ts
// コントローラーのメソッドを叩いてユニットテストしている
expect(appController.getHello()).toBe('Hello World!');
```

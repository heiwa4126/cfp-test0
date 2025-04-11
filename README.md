# cfp-test0

Cloudflare Pages の練習で、
GitHub 連携無しで始めてみたもの。

"Assets only"(スタティック)なコンテンツのみ。

## 手順

```sh
pnpm create cloudflare@latest cfp-test0
# "Hello World example" を選ぶ
# "Assets only" を選ぶ
# Gitはお好みで
cd cfp-test0
pnpm dev  # ローカルでテスト
```

## デプロイ

テンプレートから生成したプロジェクトで

```sh
pnpm run deploy
```

すると、中身は `wrangler deploy` なんで Pages でなくて Workers になってしまうので注意。

`wrangler pages deploy` 的にやらないと...

```sh
# Cloudflareにcfp-test0という名前のPagesプロジェクトを作る。認証にブラウザを使う
wrangler pages project create cfp-test0 --production-branch main


```


## Pages の制限

Free 枠の場合
ビルド(デプロイ)は月 500 回まで。
ただし「プレビューデプロイ」は無制限
(GitHub や GitLab との接続が必要)
なので活用する。

詳細: [Limits · Cloudflare Pages docs](https://developers.cloudflare.com/pages/platform/limits/)

## 関連リンク

- [wrangler - npm](https://www.npmjs.com/package/wrangler)
- [workerd - npm](https://www.npmjs.com/package/workerd)

workerd 面白い。

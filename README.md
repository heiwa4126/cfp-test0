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
pnpm run deploy # CloudFlareにデプロイ
```

Free 枠の場合
ビルド(デプロイ)は月 500 回まで。
ただし「プレビューデプロイ」は無制限
(GitHub や GitLab との接続が必要)
なので活用する。

詳細: [Limits · Cloudflare Pages docs](https://developers.cloudflare.com/pages/platform/limits/)

## 関連リンク

- [wrangler - npm](https://www.npmjs.com/package/wrangler)
- [workerd - npm](https://www.npmjs.com/package/workerd)

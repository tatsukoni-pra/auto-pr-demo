# 備考
## Github側で必要な設定
`Settings > Actions > General > Workflow permissions` の設定について

- `Read and write permissions` を選択
- `Allow GitHub Actions to create and approve pull requests` にチェック

をつけないと、権限エラーでスクリプトが失敗する。

![スクリーンショット 2024-03-08 0 50 58](https://github.com/tatsukoni-pra/auto-pr-demo/assets/90994143/5f04976a-11ef-4c89-830f-2a7f615c2c2e)

## 既にPR作成済の場合の挙動
- `main`ブランチから`prod`ブランチにマージするPRが既に存在している場合、PR自動作成に失敗する

![スクリーンショット 2024-03-10 0 57 41](https://github.com/tatsukoni-pra/auto-pr-demo/assets/90994143/860f5366-ea35-4b12-99bc-1546df8c2761)

## Prod to Main のPRをmainブランチにマージした際の挙動
- prod宛のPRが自動作成される
- marge PR が差分として表示される（[PR](https://github.com/tatsukoni-pra/auto-pr-demo/pull/9)）

![スクリーンショット 2024-03-10 1 07 08](https://github.com/tatsukoni-pra/auto-pr-demo/assets/90994143/4eacb642-fb4f-4484-88d9-b6d5dc4010bd)

# 参考記事
- https://zenn.dev/kshida/articles/auto-generate-release-pr-with-github-actions
- https://cli.github.com/manual/gh_pr_create

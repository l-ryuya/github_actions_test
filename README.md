# github_actions_test

### github actionsのテスト用リポジトリです
### テスト処理をブランチで分ける

> 公式demoプッシュしてみる

> actions/checkoutでリポジトリのクローンを行う
  - actions/checkout でリポジトリのクローンを行う
  - actions/checkout@v4 を使用すると、ワーキングツリー（現在のブランチの内容のみ） が取得される
  - GitHub Actions 上では、push されたブランチの内容のみがチェックアウトされる
  - 他のブランチの情報が必要な場合は、fetch-depth: 0 や ref オプションで明示的に指定する必要がある
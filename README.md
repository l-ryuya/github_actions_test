# github_actions_test

### github actionsのテスト用リポジトリです
### テスト処理をブランチで分ける

> 公式demoプッシュしてみる

> actions/checkoutでリポジトリのクローンを行う
  - actions/checkout でリポジトリのクローンを行う
  - actions/checkout@v4 を使用すると、ワーキングツリー（現在のブランチの内容のみ） が取得される
  - GitHub Actions 上では、push されたブランチの内容のみがチェックアウトされる
  - 他のブランチの情報が必要な場合は、fetch-depth: 0 や ref オプションで明示的に指定する必要がある
    - fetch-depth:（デフォルト１）
    - ref:（デフォルト pushしたブランチ）

      ```
        uses: actions/checkout@v4
        with:
          fetch-depth: 番号指定(例2だった場合)

          ===========下記 git log 履歴===========
          Date:   Mon Jun 30 12:55:05 2025 +0900
          git log 2

          Date:   Mon Jun 30 12:53:50 2025 +0900
          git log確認
      ```
      ```
        uses: actions/checkout@v4
        with:
          ref: ブランチ名
      ```
  - 他ブランチからmainブランチへプルリク時のブランチはどうなる？？？
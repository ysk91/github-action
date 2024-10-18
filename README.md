# github-action

## できること

- issueが新規作成されたとき、Projectに紐づける
- issueのテンプレートを設定する
  - このとき、タイトル、ラベル、担当者のデフォルト値を設定できる
  - Projectに紐づいたStatusは設定できない

## Tips

- インストールされているソフトウェア一覧
  - https://github.com/actions/runner-images
- actionsのマーケットプレイス
  - https://github.com/marketplace?type=actions
- issueテンプレート
  - https://docs.github.com/ja/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository

## actions

- https://github.com/actions/add-to-project
  - issueの作成時にProjectを紐づける
- https://github.com/actions/github-script
  - 紐づけたProjectのStatusをToDoに変更する

## 運用

- issueの作成
  - リポジトリからissueを作成する
    - slackのワークフローから作れないかな？
  - Projectに紐づけられるため、Projectを見ればリソース管理ができる
- issue一覧ページの操作
  - 作成したissueの`開始日`と`完了日`を設定する
  - issue内に要件、スケジュールを記載する
  - エンジニア、QAも必要に応じてコメントを追加する
- 実装〜リリース
  - 今まで通り
- issueのStatusを`Done`にする
  - issueが自動でアーカイブされ、一覧から消える
  - issue自体は残るため、リポジトリから確認できる


### 参考

- Github Projectsとタスクリストでissue管理を試行錯誤しているPMの話
  - https://zenn.dev/ncdc/articles/55cc05c1a65292
- プロジェクト管理ツールとしてGitHubを"普通に"使う
  - https://qiita.com/itkr/items/0d4c0015da28827b2bb7

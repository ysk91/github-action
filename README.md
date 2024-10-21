# github-action

## できること

- issueのテンプレートを設定する
  - このとき、タイトル、ラベル、担当者のデフォルト値を設定できる
  - issueが新規作成されたとき、Projectに紐づける
- Project Workflowを設定する
  - Projectに紐づいたissueのStatusをToDoに変更する
  - issueがcloseされたとき、StatusをDoneに変更する
  - StatusがDoneになったとき、issueをcloseする
- Projectのビュー設定
  - カンバンでStatus確認
  - stg環境の開始日、完了日を一覧表示

## Tips

- インストールされているソフトウェア一覧
  - https://github.com/actions/runner-images
- actionsのマーケットプレイス
  - https://github.com/marketplace?type=actions
- issueテンプレート
  - https://docs.github.com/ja/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository
  - formテンプレート
    - https://docs.github.com/ja/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms

## ~actions~ 別機能で実現するため不要

- https://github.com/actions/add-to-project
  - issueの作成時にProjectを紐づける
- https://github.com/actions/github-script
  - 紐づけたProjectのStatusをToDoに変更する

## 運用

- issueの作成
  - リポジトリからissueを作成する
    - 作成時に要件、slack履歴を記載する
    - slackのワークフローから作れないかな？
  - Projectに紐づけられるため、Projectを見ればリソース管理ができる
  - Project Workflowにより、自動でToDoが付与される
- issue一覧ページの操作
  - 作成したissueの`開始日`、`完了日`、`stg開始日`、`stg完了日`を設定する
  - （任意）issue内にスケジュールを記載する
  - エンジニア、QAも必要に応じてコメントを追加する
- 実装〜リリース
  - 今まで通り
  - issue内のチェックリストを使用するかどうかはチームの判断に任せる
- issueのStatusを`Done`にする
  - issueが自動でcloseされ、一覧から消える
  - issue自体は残るため、リポジトリから確認できる


### 参考

- Github Projectsとタスクリストでissue管理を試行錯誤しているPMの話
  - https://zenn.dev/ncdc/articles/55cc05c1a65292
- プロジェクト管理ツールとしてGitHubを"普通に"使う
  - https://qiita.com/itkr/items/0d4c0015da28827b2bb7
- リニューアルされた GitHub Projects のオートメーションを使ってみる
  - https://developer.mamezou-tech.com/blogs/2022/10/22/renewed-github-projects-automation/

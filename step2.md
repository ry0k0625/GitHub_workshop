# 第2回 GitとGitHubの連携
60-90分程度で完了．

## Gitで管理したくないファイル
同じリポジトリ上には入れるがgit管理をしない方法について知ろう．
  1. .ignoreを作成する．
  2. .ignore上に管理したくないファイル名を書く．(例: test.md，*.png) :*でファイル形式を指定して一括管理できる．
  3. .ignoreをadd，commitする．


## ファイルの細かい修正を保存したのを取り消したい時
  - git commit --amend


## Git/GitHubの連携

GitHubのアカウント(リモート)とGit(ローカル)を連携しよう

### アカウントの作成

GitHubでアカウントを作成する．
https://github.com/login


### 連携をしよう
- keyを作成する
  - [新しい SSH キーを生成して ssh-agent に追加する](https://docs.github.com/ja/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) 参照のこと．
- keyを取得する
  - \Users\名前\ .ssh にある id_ed数字.pubをVScodeで開く
  - copy
- GitHubのSettingのSSH and GPG keysから Add new SSH Keyを作成．(ノートパソコン1 等の名前を付ける．)
# 第4回 GitとGitHubの連携

2024年5月14日実施．

## 1. 前回の復習

- `fast-forward`，`non-fast-forward`の確認，conflictの発生しないmerge，発生するmerge
- `rebase`：やりたかったら勝手にやってみてください


## 2. リモートで管理する

GitHub上で作成したリポジトリをローカルで作業できるようにしよう．（実は今までやってたことよりもこちらの方が一般的）

### 2.1 GitHub上で作成したリポジトリをGit上(local)で開けるようにする

- `git clone "リポジトリのSSHリンク"`：リポジトリのクローンを作成する．

### 2.2 Gitでした作業をGitHub上に保存する

毎回作業後にこれをすることを忘れないこと．

- `git push -u origin "branch名"`：作業したbranchをGitHub上にpushする．初回だけは`-u`が必要．
- `git push origin "branch名"`：作業したbranchをGitHub上にpushする．


### 2.3 GitHub上に保存されている状態をlocalに引き継ぐ

毎回作業前にこれをすることを忘れないこと．

#### 2.3.1 fetchとmergeの2手順を踏む場合
- `git fetch origin "branch名"`：手順1 リモートからorigin/masterブランチに下ろしてくる
- `git merge origin/"branch名"`：手順2 origin/masterブランチからmasterブランチへ下ろしてくる

#### 2.3.2 pull
- `git pull origin "branch名"`：下ろしてきたいbranchを指定してlocalに引き継ぐ．
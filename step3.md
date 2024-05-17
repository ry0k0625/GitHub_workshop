# 第3回 ブランチ操作，コンフリクトの対処
2024年5月10日実施．

## 1. Linuxコマンドを知ろう
Linuxのコマンドを使いこなそう．
- `touch "テキスト名"`.txt: ファイルを作るコマンド.
- `cp fuyou.txt fuyou/fuyou.txt`
- `ls -la`: ファイル一覧の表示
- `mv fuyou.txt iranai.txt`: ファイルの名前を変更
- `git add . `:全部をアップロード
- `git rm iranai.txt`: ファイルを削除する
- `git rm -r fuyou/` : ディレクトリごと削除する．

## 2. ブランチ操作
よく言われるのが「三日前の自分は他人だと思え！」である．ブランチを切って作業することで作業の効率化を目指そう．

参考資料 [ロボ太さんスライド](https://speakerdeck.com/kaityo256/github-branch)

### 2.1. Fast-forwardでやってみよう
1. `git branch branch_ff`：branch_ffというラベルを作成する
2. `git switch branch_ff`：視点(HEAD)をmain からbranch_ffに変更する
3. .mdに修正を加え，ステージング，コミット
4. F1 + log で状態を確認する
5. `git swich main`：mainに移動する
6. `git merge branch_ff`：branchをmainに結合させる


### 2.2. Non-fast-forwardでやってみよう
1. `git branch branch_nff`：branch_ffというラベルを作成する
2. `git switch branch_nff`：視点(HEAD)をmain からbranch_ffに変更する
3. .mdに修正を加え，ステージング，コミット
4. F1 + log で状態を確認する
5. `git swich main`：mainに移動する
6. `git merge --no-ff branch_ff`：branchをmainに結合させる


### 2.3. 差分の取り方
前日の記録と差分を取る．
hash値の見方：F1+logで出てくる一番左の値(hash値)
![alt text](<hash値.png>)
図で言う「5a0795a」がhash値↑

- `git diff "hash値"`：差分を取る
- `git diff "hash値"`>diff.txt：差分を出力


### 2.4. conflictが生じない複数のmergeをやってみよう
branchを切って違う箇所を変更させる．2回mergeを行うが，その場合conflictは発生せずmergeを行うことができる．
__いつか追記します__

### 2.5. conflictをやってみよう
実際にbranchを切ってplanAとplanBを作成してconflictを発生させよう．
(略)
conflictが生じたらVScode上で対処できる．
__いつか追記します__
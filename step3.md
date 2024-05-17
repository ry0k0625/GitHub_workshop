# 第3回 ブランチ操作，コンフリクトの対処
2024年5月10日実施．

## 1. Linuxコマンドを知ろう
Linuxのコマンドを使いこなそう．
- touch .txt: ファイルを作るコマンド.
- cp fuyou.txt fuyou/fuyou.txt
- ls -la: ファイル一覧の表示
- mv fuyou.txt iranai.txt: ファイルの名前を変更
- git add . :全部をアップロード
- git rm iranai.txt: ファイルを削除する
- git rm -r fuyou/ : ディレクトリごと削除する．

## 2. ブランチ操作
よく言われるのが「三日前の自分は他人だと思え！」である．ブランチを分けて作業することで作業の効率化を目指そう．

参考資料 [ロボ太さんスライド](https://speakerdeck.com/kaityo256/github-branch)

### 2.1 Fast-forwardでやってみよう
1. 
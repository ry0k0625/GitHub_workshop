# 第1回 Introduction

2024年5月7日実施．かかった時間は2時間程度だったが，VSCodeのインストールが全員済んでいたため，そうでない場合はさらに時間がかかるかもしれない．

## 1. Git/GitHubの概念を知ろう

Git/GitHubの概念について知る．
- 参考資料([ロボ太さんのスライド](https://kaityo256.github.io/github/)参照)



## 2. 環境構築

### 2.1. Gitのインストール

 [Git Download リンク](https://git-scm.com/downloads) から.exeファイルをダウンロードしてインストールする．
 
 ※作業中のタグをmaster表記かmain(変更可)で選択する場面があるのでそこでmainを選択すること．これはmaster/slaveが現在の風潮に反しているためである．

- Gitでの設定：Git Bash上で入力する
  - ユーザ名の設定
    - git config --global user.name "ryoko_lab_Desktop"：Gitでのユーザ名になるので，Desktopや家のパソコンと使い分ける人はそれがわかるようなユーザ名にすると良い．（要確認）
    - git config --global user.email "ry@gmail.com"
  - Gitで使用するエディタを変更する
    - git config --global core.editor "code --wait"


### 2.2. VSCodeの拡張機能のインストール

インストールしてほしい拡張機能（一部班によって異なる）
- code-eol
- Git History
- GitLens
- Image preview
- Japanese Language
- LaTeX Workshop
- Markdown All in One
- Markdown PDF
- MATLAB
- Modern Fortran
- Print
- Word Counter
- WSL


### 2.3. setting.jsonの書き換え

担当のドクターの先輩が公開してくださっているものを使用した.
自力でいじれる場合はこの限りではないが，先輩と同じ環境だと指導がしやすいのである程度統一されることが望ましい．

link：[松川さんsetting.json](https://gist.github.com/Yuki-MATSUKAWA/465ecd0ebcbd157e48ac1e3619c9a08c)



## 3. 実際にGitを使ってみよう

### 3.1. local上でGitサーバー上で管理するディレクトリを作成する

手順1. mkdir git_tmp：フォルダを作成する
手順2. cd git_tmp：git_tmpを開き，中へ入る
手順3. git init：「.git」ディレクトリが作成される．（git_tmpはサーバー上で管理されるようになった）

### 3.2. Markdown方式で文書を作成しよう

touch git_practice.mdで文書を作成．内容は git_practice.md 参照．

### 3.3. 作成した文書をサーバーで保存しよう

手順1. Ctrl + S でローカルに保存する．
手順2. git add git_practice.md でステージングする．(「git add .」全てのファイルをステージングできる)
手順3. git commit -m "initial commit" でサーバーに保存する．
手順4. git diff git_practice.md --color-word で差分の確認ができる．もしくは F1 + log で球と線の状態が確認できる．


### 3.4. VSCodeのGitBash上の日本語が文字化けする場合への対処

基本的には問題はないが，気になるようであれば[リンク](https://qiita.com/OharanD/items/616021c72f8890a429dd)を参照し，設定を変更すること．


# github-learn

## git　チートシート

[参考URL１](https://training.github.com/downloads/ja/github-git-cheat-sheet.pdf)

# コマンド集

### gitの設定
gitを使用する際に必要なユーザ情報の設定方法
  - `git config user.name "[name]"` コミット操作に記録される作業者の名前を設定します
  - ` git config user.email "[email address]"` コミット操作に記録される作業者のメールアドレスを設定します
 
`--global`を`git config`の後に付けてコマンドを打つと作業PCでログイン中のユーザが操作できる全てのローカルリポジトリのユーザ設定を行えます。
`--global`を付けない場合は上記ユーザ設定のコマンドを打ったローカルリポジトリのみユーザ設定が行われます。


### リポジトリの作成方法
リポジトリを作業PCに新規作成、もしくは既存のインターネット上にあるリポジトリを作業PCに構築する方法
- ` git init [project-name]` 作業PCにリポジトリを新規作成します
- ` git clone [url]` コマンドを打った時点での全てのバージョン情報(作業内容)を含んだインターネット上にあるプロジェクト(リポジトリ)を作業PCへコピーします

### 変更内容の確認・登録
gitに登録する変更内容に関するコマンド
- `git status` 変更、もしくは新規追加したファイルの一覧を表示します *
- `git diff` ステージング前のファイルにおける変更前と変更後の差分を表示します *
- `git add [file]` 指定したファイルをステージングエリアへ移動します *
- `git diff --staged` ステージング後のファイルにおける変更前と変更後の差分を表示します *
- `git reset [file]` 指定したファイルをステージングエリアから作業エリアへ戻します *
- `git commit -m "[descriptive message]"` ステージングエリアに登録されているファイルの変更内容をバージョン管理へ登録します、その際変更内容を端的に示したコメントを登録することで他の作業者が作業内容を理解しやすくします *

*がついているものについてvscodeではコマンドを使用せずにvscode側の機能で作業が行えます

### ブランチに関する操作
ブランチの作成、統合、作業ブランチの切り替え、ブランチの削除に関するコマンド
- `git branch` 作業中のリポジトリに登録されている全てのローカルブランチ一覧を表示します *
- `git branch [branch-name]` 指定した名前でブランチを新規作成します *
- `git checkout [branch-name]` 指定したブランチへ作業ブランチを切り替えます *
- `git merge [branch]` 指定したブランチの変更内容を現在の作業ブランチに統合します *
- ` git branch -d [branch-name]` 指定したブランチを削除します *

*がついているものについてvscodeではコマンドを使用せずにvscode側の機能で作業が行えます

### ファイルに関する操作
ファイルの削除、ファイル名の変更操作に関するコマンド
- `git rm [file]` 指定したファイルを現在作業中のブランチから削除して削除したことをステージングに登録します *
- `git rm --cached [file]` 指定したファイルをgitのバージョン管理からのみ削除をします、作業ブランチ上では削除は行われません
- `git mv [file-original] [file-renamed]` `[file-original]`で指定したファイルを`[file-renamed]`で指定したファイル名に変更してコミットを行います

*がついているものについてvscodeではコマンドを使用せずにvscode側の機能で作業が行えます

### コミット前の変更内容に関する操作
対応中の作業を一時中断して退避、復旧させるコマンド
- ` git stash` 作業ブランチにあるコミット前の変更ファイル全てを一時保存領域に保存します *
- `git stash pop` 直近に一時保存領域へ保存された内容を現在の作業ブランチに戻します *
- `git stash list` 一時保存領域に保存されている保存内容の一覧を表示します *
- ` git stash drop` 直近に一時保存領域へ保存された内容を削除します *

*がついているものについてvscodeではコマンドを使用せずにvscode側の機能で作業が行えます

### 履歴に関する操作
ブランチの作業内容履歴に関するコマンド
- `git log` 作業ブランチのこれまでの変更履歴一覧を表示します
- ` git log --follow [file]` 指定したファイルの名前変更を含む全ての変更履歴一覧を表示します
- `git diff [first-branch]...[second-branch]` 2つのブランチ間の差分を表示します
- `git show [commit]` 指定されたコミットの情報と変更内容を表示します

### コミットの修正に関する操作
間違ったコミットの削除、巻き戻しを行うコマンド
- `` 
- `` 

### 変更内容の同期、統合に関する操作
リモートとローカルリポジトリの同期、ファイルのやりとり、ブランチの統合に関する操作
- ` git fetch` リポジトリから全てのブランチ、変更履歴をダウンロードします
- `git merge [bookmark]/[branch]` `[bookmark]`で指定したブランチの変更内容を`[branch]`で指定した現在のローカルブランチへ統合します
- `git push` ローカルブランチの変更内容をgitのリモートリポジトリへアップロードします
- `git pull` リモートリポジトリの内容をローカルリポジトリへダウンロードして変更内容を統合します





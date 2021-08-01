[初回]ローカルにリポジトリを作成し、リモートにプッシュする際の手順
 git init								現在いるディレクトリをgitで管理するための設定ファイルを生成する。
 git add ファイル名						「ファイル名」の部分にファイル名を指定することで、指定したファイルをインデックスに追加することができます。
 git commit -m "コメント"				メッセージをつけて変更履歴を保存する。
 git branch -M main						デフォルトブランチをmasterからmainに変更する。デフォルトブランチがmainの場合は不要
 git remote add origin リポジトリURL	originという名前でリモートリポジトリのURLを登録する。
 git push origin ブランチ名				ローカルの変更をリモートリポジトリにアップロードする。「ブランチ名」にアップロードしたいブランチの名前を指定します。

---
[2回目以降]ローカルにリポジトリの変更をリモートにプッシュする際の手順

 git add ファイル名						「ファイル名」の部分にファイル名を指定することで、指定したファイルをインデックスに追加することができます。
 git commit -m "コメント"				メッセージをつけて変更履歴を保存する。
 git push origin ブランチ名				ローカルの変更をリモートリポジトリにアップロードする。「ブランチ名」にアップロードしたいブランチの名前を指定します

リモートリポジトリをローカルリポジトリに複製する(ダウンロード)

 git clone リポジトリURL				リモートリポジトリをローカルリポジトリに複製する（ダウンロード）。「リポジトリURL」は複製したいリモート先のURLを指定します。

---
リモートリポジトリの変更をローカルに反映させる

 git fetch origin						リモートリポジトリからローカルにあるリモートリポジトリのコピーに最新情報をダウンロードする
 git merge ブランチ名					ローカルブランチに反映する
 git pull origin ブランチ名				fetchとmergeをまとめて実行できるコマンド

---
ブランチの作成・確認

 git branch								ブランチの一覧を表示する
 git branch ブランチ名					ブランチを作成する。「ブランチ名」の部分に、作成するブランチの名前を指定します
 git checkout ブランチ名				ブランチ名を指定して切り替える
 git checkout -b ブランチ名				ブランチの作成と切り替えをまとめて実行できるコマンド

---
ログの確認・操作

 git log								コミットの履歴を確認する
 git reset								コミット	履歴を元に前の状態に戻す。「コミット」には識別番号を指定します。git reset HEAD^で一つ前に戻すことも可能
 git status								ファイルの追加/変更/削除の確認
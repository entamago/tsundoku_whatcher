# README

## アプリケーション名
積読Watcher

## アプリケーション概要
自身の達成したい目標と学習したいジャンルを決めて、学習内容を可視化する学習サポートアプリケーション。  
使用することで目的を明確にして、学習を継続しやすくする。また積み上げた内容を数値として表示することで自信やモチベーションの向上を図る。  
SNS機能を排除して参考にしたURL以外には遷移しないので、集中して学習がしやすい。

## URL
https://tsundokuwatcher.herokuapp.com/

## テスト用アカウント
Eメール：test@test.com  
パスワード：test1test1


## 利用方法
1. アカウントを作成してログインする
2. 短期目標を設定して、期限と目標達成のための具体的行動計画を明文化する。
3. 学習するジャンルを決めて、ジャンルごとに要約記事を作成する。
4. 期限内に短期目標が達成できたら、目標見直しの達成チェックをチェックする。
5. 達成した目標や作成した記事はトップページから確認できる。また記事は検索可能。
6. 短期目標が達成されたり期限が超過すると新規短期目標の設定を促される。（２へ戻る）

## 目指した課題解決
これから新しく学習を始めたい人が、自分の学習行動を認知しやすくするためのアプリケーション。解決したい課題として挙げられることは以下４点。  
①学習をSNSでのアウトプットしようとすると他者との比較になりやすく、インプット過多になりやすいこと。  
②ノートやパソコンでの情報のまとめは情報量が多くなりやすく、見直しに時間や手間がかかること。  
③ネットなどの情報を参考にするとブックマークなどが煩雑になってしまうこと。  
④目標も期限や内容が曖昧なまま始めると、途中で方向性が変わったりダラダラと作業してしまいやすいこと。

## 洗い出した要件
1. トップページ：ユーザーの情報をひと目でわかるよう表示する
2. ユーザー管理機能：ユーザーごとに情報を表示するため
3. 学習ジャンル機能：ジャンルごとに学習記事を管理する
4. 学習記事機能：学習記事を投稿・編集・削除する機能
5. 学習記事検索機能：見直し・復習しやすいよう検索する
6. 目標管理機能：学習のモチベーションと自信を高める

## 実装した機能についての説明
### ユーザー管理機能
新規ユーザー登録、ログインとログアウトができる
### 学習ジャンル機能
学習するジャンルとその説明を追加・編集・削除ができる
### 学習記事機能
学習した内容を200文字で要約して記事として投稿できる。
投稿した記事は編集・削除ができる。特徴として参考・備考欄にWebサイトのURLを記載すると自動でリンク化される。記事の入力可能文字数はカウントされ、リアルタイムで投稿可能かどうかを判定して表示する。
### 記事検索機能
学習した記事はナビバーにある検索機能を使用してすぐに探すことができる。検索したキーワードがヒットした記事はジャンルに関係なく表示される。また検索のキーワードを入れずに検索すると作成した記事がジャンル関係なく表示される。特徴として見やすいように記事一覧の上下にページネーションを表示している。
### 目標管理機能
学習する上で学習の目的や方向性を見失わないように、短期目標を言語化して表示しておく機能。短期目標には30日以内で期限を設定する必要があり、いつまでに行うかを決めることでダラダラと学習しないよう促す。期限が切れると目標の見直しを促される。


## 実装予定の機能
### 学習記録公開機能
SNSのように相互のコミュニケーションをとるのではなく、APIを使用して積読Watcherの記事を投稿したときに記事のジャンルとタイトルを自動で投稿するような機能。SNSアカウントでのログインと連動してログインしたアカウントへの投稿を自動化できるとよいと考えている。


## データベース設計
![ERD](https://user-images.githubusercontent.com/81839879/130967653-960f4fd2-cbef-40b3-8b5e-0b642315ee40.png)

## ローカルでの動作方法
ローカル環境での動作までに必要なコマンドは以下のとおり
1. git clone <リモートリポジトリのURL>
2. cd アプリケーションのディレクトリ
3. bundle install
4. yarn install
5. rails db:create
6. rails db:migrate
7. rails s



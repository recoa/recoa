□ 課題
コロナで出社管理簿の記載が面倒である
①Excel ベースだとデグレしてしまう
②PMWB 管理だと原本化はできるが Commit が面倒である
※更新処理が重いし時々バッティングするので再 Commit が必要

→Web ベースでサクッと登録したい
　 →SPA、仮想 DOM だと早いらしい

フロントエンド
どうやら React のシェアが高いらしい
バックエンド
Amplify が使いやすいらしい

サーバレスアーキテクチャの選択肢として、AWS の Amplify、Google の Firebase が有力な候補
Amplify vs Firebase
→ 最初に使いやすいのは Firebase。多機能なのは Amplify。

□ やりたいこと
・ユーザ登録機能
・カレンダーで予定を入れられる機能

AMPLIFY でチャットアプリをつくる
https://amplify-sns.workshop.aws/ja/

AWS Amplify と Vue.js でデータ登録取得機能を構築してみました！
https://day-journal.com/memo/try-035/
Vue.js×FullCallendar で WEB カレンダー作成
https://qiita.com/doikatsuyuki/items/344b61459977a7ee2eff
Vue.js×GraphQL(AppSync)×Amplify で TODO リストを作る
https://qiita.com/is_ryo/items/b9feeb017366b0cee544

React Hooks + Redux ToolKit + TypeScript を使って、COVID19 (コロナウイルス)ダッシュボード Web アプリを作ります。
https://nttdatagdpo.udemy.com/course/covid-19-react-live/learn/lecture/20828166#overview

React で fullcalender を使ってカレンダーアプリっぽいことをしてみたのでまとめてみる
https://qiita.com/rpf-nob/items/466d5c8e0204146b2d6f

React Calendar Timeline
https://github.com/namespace-ee/react-calendar-timeline

Material-UI の場所
https://next.material-ui.com/components/material-icons/

社内システムの AWS 構成を紹介してみる
https://qiita.com/nogu-rin/items/301ee04a9d5b4244e8c0

Yahoo! JAPAN トップページを Atomic Design と React・Redux・TypeScript で作り変えたお話
https://techblog.yahoo.co.jp/entry/20191203785540/

GraphQL
Amplify DataStore

AmplifyApp を作成
GraphQL スキーマを作成
スキーマからコードを自動生成
アプリケーションへの組み込み

GraphQL スキーマを定義
Material-UI で画面を定義

$ date +%s
1609756850

Timestamp がとれる

cat >> text
コピペ
Ctrl+d
で、追記できる

schema.graphql
type Post @model {
id: ID!
title: String!
content: String!
price: Int
rating: Float
}

type Post
@model (subscriptions: { level: public })
@auth(rules: [
{allow: owner, ownerField:"owner", provider: userPools, operations:[read, create]}
{allow: private, provider: userPools, operations:[read]}
])
{
type: String! # always set to 'post'. used in the SortByTimestamp GSI
id: ID
content: String!
owner: String
timestamp: AWSTimestamp!
}
git add .
git commit -m "コード整形"
git push origin develop

master リリース
git fetch origin master
git merge origin/master
git push origin master

git add .
git commit -m "memo"
git push origin develop

git add .
git commit -m "API 修正未完了"
git push origin webstudy
git checkout webstudy

Cloud9 のコード整形
Command + Shift + B

git pull origin main --allow-unrelated-histories

新規ブランチの構築

git checkout -b webstudy
git push --set-upstream origin webstudy
Amplify のコンソールでブランチとバックエンドの紐付け

amplify env add
amplify push

TimePicker
https://material-ui-pickers.dev/getting-started/usage

.
├── App.js
├── components
│?? ├── GlobalStyles.js
│?? ├── Logo.js
│?? └── Page.js
├── icons
│?? ├── Facebook.js
│?? └── Google.js
├── index.js
├── layouts
│?? ├── DashboardLayout
│?? │?? ├── index.js
│?? │?? ├── NavBar
│?? │?? │?? ├── index.js
│?? │?? │?? └── NavItem.js
│?? │?? └── TopBar.js
│?? └── MainLayout
│?? ├── index.js
│?? └── TopBar.js
├── mixins
│?? └── chartjs.js
├── routes.js
├── serviceWorker.js
├── theme
│?? ├── index.js
│?? ├── shadows.js
│?? └── typography.js
├── utils
│?? └── getInitials.js
└── views
├── account
│?? └── AccountView
│?? ├── index.js
│?? ├── ProfileDetails.js
│?? └── Profile.js
├── auth
│?? ├── LoginView.js
│?? └── RegisterView.js
├── customer
│?? └── CustomerListView
│?? ├── data.js
│?? ├── index.js
│?? ├── Results.js
│?? └── Toolbar.js
├── errors
│?? └── NotFoundView.js
├── product
│?? └── ProductListView
│?? ├── data.js
│?? ├── index.js
│?? ├── ProductCard.js
│?? └── Toolbar.js
├── reports
│?? └── DashboardView
│?? ├── Budget.js
│?? ├── index.js
│?? ├── LatestOrders.js
│?? ├── LatestProducts.js
│?? ├── Sales.js
│?? ├── TasksProgress.js
│?? ├── TotalCustomers.js
│?? ├── TotalProfit.js
│?? └── TrafficByDevice.js
└── settings
└── SettingsView
├── index.js
├── Notifications.js
└── Password.js

https://github.com/devias-io/material-kit-react

https://material-ui.com/

Iperf
ネットワーク負荷
Jmeter
セッション数

メモリはカスタムでエージェント入れる必要がある
Working with SSM Agent

□ 要件定義
・ログイン
・4 択ボタンがある

□chart_lesson

VSCODE でフォルダを作る
covid
npm install @reduxjs/toolkit
npm install --save react-chartjs-2 chart.js

npm install react-icons --save
npm i --save-dev @types/react-redux
npx create-react-app . --template typescript
npm install --save react-chartjs-2 chart.js
npx create-react-app . --template redux-typescript
npm install axios

npm install react-redux
npm start

npm install -g @aws-amplify/cli@4.16.1
amplify configure
amplify init
amplify env checkout master

Google Chrome 拡張機能の JSON Formatter をインストールして下さい。

https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa?hl=ja-JP

npm install -g @aws-amplify/cli@4.16.1
amplify configure
npm install axios
npm install @material-ui/core
npm install chart.js --save
npm install react-chartjs-2
npm install react-countup
npm install react-icons

git 初期化
rm -rf .git <-- 念の為.git フォルダを削除
git init
git add .
git commit -m "first commit"
git remote add origin git@github.com:recoa/covid.git
git push -u origin master

補足：「Permission denied」でソースコードの push に失敗する場合
端末で GitHub の設定が完了していない場合、「Permission denied」で push に失敗することがあります。その場合は、以下の手順を実施してから再度 push コマンドを実行してください。

公開鍵・秘密鍵のペアを作成します。途中いくつか質問されますが、全てデフォルトで Enter を押してください。

cd ~/.ssh
ssh-keygen -t rsa
~/.ssh/id_rsa.pub というファイルが作成されるので、このファイルの中身をコピーします。

cat id_rsa.pub

ssh-rsa ... から始まる文字列をコピーする

https://github.com/settings/ssh/new にアクセスし、「Title」と「key」を入力します。Title にはアクセスする端末を特定するわかりやすい名前を入力してください。「Key」には先ほどコピーした「ssh-rsa …」から始まる文字列を貼り付けてください。「Add SSH key」を押下すると、公開鍵を登録することができます。

git checkout -b develop
git push --set-upstream origin develop

プロセスを Kill する
lsof -i:8080
kill 8080

git add .
git commit -m "memo"
git push origin develop

git fetch
git branch -a
git pull origin develop:develop
git pull origin covid_api:covid_api

□youtube

$ git clone https://github.com/ogom/react-comment-box-example.git
$ cd react-comment-box-example

# パッケージの更新の確認は npm-check-updates を利用する

$ npm install -g npm-check-updates

# 更新パッケージの確認

$ ncu
Checking react-comment-box-example/package.json
[====================] 22/22 100%
babel-core ^6.18.2 → ^6.26.3
babel-jest ^17.0.2 → ^24.8.0
babel-loader ^6.2.8 → ^8.0.6
babel-preset-es2015 ^6.18.0 → ^6.24.1
babel-preset-react ^6.16.0 → ^6.24.1
css-loader ^0.26.0 → ^3.0.0
enzyme ^2.6.0 → ^3.10.0
jest ^17.0.3 → ^24.8.0
jquery ^3.1.1 → ^3.4.1
postcss-loader ^1.1.1 → ^3.0.0
react ^15.4.1 → ^16.8.6
react-addons-test-utils ^15.4.1 → ^15.6.2
react-dom ^15.4.1 → ^16.8.6
react-hot-loader ^1.3.1 → ^4.12.7
react-redux 5.0.0-rc.1 → 7.1.0
redux ^3.6.0 → ^4.0.4
redux-actions ^1.1.0 → ^2.6.5
style-loader ^0.13.1 → ^0.23.1

# 下記コマンドで package.json を更新

$ ncu -u

$ npm install
$ npm start

git clone -b ブランチ名 https://リポジトリのアドレス
git clone -b covid_api https://github.com/recoa/covid.git
git clone -b youtube-react https://github.com/recoa/youtube-react.git

新しい作業環境で開発リポジトリの master リポジトリを clone したあとにその他のブランチも checkout/pull したいことがある。というか、しないと作業にならない。

よく忘れるのでメモ。

git checkout -b local_branch_name origin/remote_branch_name
git checkout -b covid_api origin/covid_api

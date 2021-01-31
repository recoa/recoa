# recoa

npm install --save react-router-dom
npm install node-sass@4.14.1

npm i --save @fortawesome/fontawesome-svg-core
npm install --save @fortawesome/free-solid-svg-icons
npm install --save @fortawesome/react-fontawesome

//FONTAWESOME から MATERIAL-UI へ変更

npm install @material-ui/core
npm install @material-ui/icons
npm install --save normalize.css

git branch -a
git add .
git commit -m "動画リスト表示まで動作確認"
git push origin master

React Developer Tools
https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=ja

Devtool の表示方法
Ctl+Shift+I は機能
F12 押して右上の「・・・」(縦並び)をクリックして「Dock side」を「undock」に

https://developers.google.com/youtube/v3/docs/videos/list?hl=ja

VSCode でコード整形ツール(Fomatter)を使用したい場合の導入方法メモ。

1. Formatter のデフォルトのショートカットキーである「Ctrl + Alt + F」キーを押下する
   (Mac の場合、英字モードにしてから「Shift + Option + F」を押下)
2. フォーマッターがインストールされていなければ、右下にインストールしますか？という通知が表示される
3. Yes ボタンをクリックする (Install ボタンだったかも)
4. python の場合、「$ python -m pip install -U autopep8 --user」のコマンドがターミナルに表示され、自動で autopep8 のライブラリがインストールされる

これで Ctrl + Alt + F(もしくは Shift + Option + F)を押すとコード整形できるようになります。

保存時にコード整形したい場合
メニューから File -> preferences -> settings
formatOn で検索する
Format On Save にチェックをつける

TestCRLF
=======

・はやりのGitHubを使ってみたよ。
・改行コードで diff が上手く見れずはまってhistoryよごしたよ。
・気兼ねなく試したいので、リポジトリ作ったよ。

詳しくはここ
----------------

[コミット履歴](https://github.com/akagane99/TestCRLF/commits/master) - 改行コードの変換パターンをいろいろ試してみた。

参考URL
----------------

http://d.hatena.ne.jp/dojum/20121126
https://github.com/CreateSomethingWithStarling/HagiBreakout/issues/12
http://d.hatena.ne.jp/couichi/20110207/1297101115

環境
----------------

windows7
GitHub for windows

autocrlf設定
----------------
gitconfig, configで設定可能。
4か所

・C:\Program Files (x86)\Git\etc\gitconfig
・%USERPROFILE%\AppData\Local\GitHub\PortableGit_どーたらこーたら\etc\gitconfig
・%USERPROFILE%\.gitconfig
・ダウンロードしたリポジトリ\.git\config

メモ
----------------

%USERPROFILE%\.gitconfig

上記コンフィグは、下記コマンドで設定、確認ができた。

--- .gitconfig の autocrlf設定

git config --global core.autocrlf true

--- .gitconfig の autocrlf確認

git config --get core.autocrlf

TestCRLF
=======

・はやりのGitHubを使ってみたよ。

・改行コードで diff が上手く見れずはまってhistoryよごしたよ。

・気兼ねなく試したいので、リポジトリ作ったよ。

詳しくはここ
----------------

[html, phpコミット１](https://github.com/akagane99/TestCRLF/commit/f6d6ba81822639be206251a319ed4d6b5a64d55f) 改行コードずれ有り

[html, phpコミット２](https://github.com/akagane99/TestCRLF/commit/95987d979cf30f0a265c3ca8b763fa6cce4579dd) 改行コードずれなし

[html, phpコミット３](https://github.com/akagane99/TestCRLF/commit/b246771aa625f2848bf7f6bb60e28d3ea84afa6d) 改行コードずれなし

[html, phpコミット４](https://github.com/akagane99/TestCRLF/commit/d3c013b3e1c1388fa4b2263568c04aa0e946935e) 改行コードずれ有り

[html, php, text コミット５](https://github.com/akagane99/TestCRLF/commit/34b89f520730ea442cad86f6d83793fdac8e551f) 改行コードずれなし


[コミット履歴](https://github.com/akagane99/TestCRLF/commits/master) - 改行コードの変換パターンをいろいろ試してみた。

結論
----------------

[html, phpコミット４](https://github.com/akagane99/TestCRLF/commit/d3c013b3e1c1388fa4b2263568c04aa0e946935e) 改行コードずれ有り

GitHubはLF, ローカルはCRLFにして、autocrlf = true にして２ファイルをコミットしたが、１ファイル改行変換されず微妙。

[html, php, text コミット５](https://github.com/akagane99/TestCRLF/commit/34b89f520730ea442cad86f6d83793fdac8e551f) 改行コードずれなし

素直に GitHub 及び ローカルの改行コードを同じにして、autocrlf = false が良さそう。

参考URL
----------------

[GitHub for Windowsいろいろ - 役に立ちそうもないTips](http://d.hatena.ne.jp/dojum/20121126)

[そのうちGitの改行コード、空白文字の設定のルールを決める · Issue #12 · CreateSomethingWithStarling-HagiBreakout](https://github.com/CreateSomethingWithStarling/HagiBreakout/issues/12)

[git config の core.safecrlf って何のためよ？ - 必ず隣あり](http://d.hatena.ne.jp/couichi/20110207/1297101115)

環境
----------------

windows7

GitHub for windows

autocrlf設定
----------------
gitconfig, configで設定可能。4か所

・wsysgitの共通設定 - C:\Program Files (x86)\Git\etc\gitconfig

・wsysgitのユーザー毎設定 - %USERPROFILE%\.gitconfig

・GitHub for windowsの設定 - %USERPROFILE%\AppData\Local\GitHub\PortableGit_どーたらこーたら\etc\gitconfig

・各リポジトリの設定 - ダウンロードしたリポジトリ\.git\config

メモ
----------------

・wsysgitのユーザー毎設定 - %USERPROFILE%\.gitconfig

上記コンフィグは、下記コマンドで設定、確認ができた。

--- .gitconfig の autocrlf設定

git config --global core.autocrlf true

--- .gitconfig の autocrlf確認

git config --get core.autocrlf

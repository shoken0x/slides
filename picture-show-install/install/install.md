!SLIDE
# picture-showのインストール手順
#### picture-showの環境構築ではまったので、インストール手順を紹介します

!SLIDE
## picture show とは
* [https://github.com/softprops/picture-show)](https://github.com/softprops/picture-show)
* Markdownからスライドを作成
* Scalaで書かれてます

!SLIDE
## picture show についてわかりやすい説明
* [picture-show でスライドを作りましょう](http://d.hatena.ne.jp/tototoshi/20111026/1319644432)
* インストール方法、使い方が書いてありますので、まずはこちらを読まれることをおすすめします

!SLIDE
## 最終的にはこんな感じで使います
```
$ pshow  #http://localhost:3000 で起動してスライド確認

$ pshow --offline -o=D:\src\git\slides\picture-show-install
#outputに出力
```

!SLIDE
## インストールした環境
* Windows XP
* Java 1.7.0_06
* Scala 2.9.1
* 注意：proxy環境ではproxy情報を環境変数にsetしても最後までインストールできませんでした。。

!SLIDE
## インストールするもの
* sbt
    * 0.11.2を入れる
* conscript
    * 0.4.0を入れる
* バージョン大切
    * 参考：[Scala 2.9.1 + sbt 0.11.2 でpicture-showをインストール](http://kiris.hatenablog.com/entry/2011/12/16/121709)

!SLIDE
## sbtのインストール
* ここからdownload
    * [http://scalasbt.artifactoryonline.com/scalasbt/sbt-native-packages/org/scala-sbt/sbt/0.11.2/](http://scalasbt.artifactoryonline.com/scalasbt/sbt-native-packages/org/scala-sbt/sbt/0.11.2/)
* sbtにパスを通す

!SLIDE
## picture-showのインストール
```
$ git clone https://github.com/kiris/picture-show.git
$ cd picture-show
$ sbt publish-local
```

!SLIDE
## conscriptのインストール
* ここからdownload
    * [https://github.com/downloads/n8han/conscript/conscript-0.4.0.jar](https://github.com/downloads/n8han/conscript/conscript-0.4.0.jar)
```
$ java -jar conscript-0.4.0.jar
installed C:\Documents and Settings\user\bin\cs.bat 
#成功
```
* すかさずcs.batにパスを通す

!SLIDE
## ビルド
```
$ cs kiris/picture-show
Conscripted kiris/picture-show to C:\Documents and Settings\myuser\bin\pshow.bat
#できた！
```

!SLIDE
## もう一回使い方
```
$ pshow  #http://localhost:3000 で起動してスライド確認

$ pshow --offline -o=D:\src\git\slides\picture-show-install
#出力
```
* あとはこのブログを参考にしてください
    * [picture-show でスライドを作りましょう](http://d.hatena.ne.jp/tototoshi/20111026/1319644432)

!SLIDE
## TIPS
* 日本語を表示する際にはUTF-8で保存しましょう
* .mdファイルの最終行は改行しましょう

!SLIDE
## githubでスライドショーしたい！
* gh-pagesを作りましょう

```
#まずはブランチ作成
$ git branch gh-pages
#作ったブランチに作業を移行
$ git checkout gh-pages
#修正を加えてコミットしてから
$ git commit -a
$ git push origin gh-pages
```
* gh-pagesにindex.html他をcommitする

!SLIDE
## ご参考：このスライドのソース
* ソース
* [https://github.com/syokenz/slides/tree/gh-pages/picture-show-install](https://github.com/syokenz/slides/tree/gh-pages/picture-show-install)
* スライド  
* [https://syokenz.github.com/slides/picture-show-install](https://syokenz.github.com/slides/picture-show-install)

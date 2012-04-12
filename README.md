はじめてのSASS
================


色々なサイトを参考にして、

自分用にテンプレートのSASSファイルを作ってみました。


ファイル構成
------------
     　　 |-css
     　　 |  |-style.css
     　　 |-sass
     　　    |-style.scss
     　　    |-core/
                |-_setting.scss
                |-_reset.scss
                |-_layout.scss
                |-_main.scss
                |-_mixin.scss
                |-_print.scss
                

* CSSファイルに変換するSCSSファイルは`style.scss`のみです。
* それ以外のSCSSファイルにはインポート専用ファイルとしてアンダースコア( _ )をつけてます。


Coreディレクトリ
----------------

### 1._setting.scss

Coreディレクトリ内で基礎となるファイルをいれてます。

サポートするブラウザ、画像パス、HTML5の条件分岐、CSS3用ベンダープレフィックスの指定、
フォントサイズの設定（px→％指定に自動的に変更してくれる便利関数）、
リンクの色設定を記述してます。

     　　 |-support
     　　 |-path
     　　 |-html5
     　　 |-CSS3
     　　 |-fontSize
     　　 |-color
 

### 2._reset.scss

[html5doctorのリセットCSS](http://html5doctor.com/html-5-reset-stylesheet/)と
[YUIのリセットCSS](http://yuilibrary.com/yui/docs/cssreset/)をそれぞれ記述し、
`_setting.scss`にあるhtml5の設定を変更することで分岐させてます。

### 3._layout.scss

大まかなレイアウトのCSSを表記。
レスポンシブデザインやグリッドデザイン向けのサイズ計算用mixinもここに記述してます。

     　　 |-layout/
     　　 |  |-responsiveDesign
     　　 |  |-gridDesign
     　　 |-#contents
     　　 |-#header
     　　 |-#footer


### 4._main.scss

スタイルはここに記述していきます。

### 5._mixin.scss

共有できそうな変数やMixinsなどをまとめて入れてます。

     　　 |-Mixin/
     　　 |  |-clearfix
     　　 |  |-min-height
     　　 |  |-inline-block
     　　 |  |-background-size
     　　 |  |-brightness
     　　 |  |-sprite
     　　 |  |-font-family
     　　 |-Mixin(for CSS3)/
     　　 |-border-radius
     　　 |-gradient
     　　 |-text-shadow
     　　 |-box-shadow
     　　 |-box-sizing


### 6._print.scss

印刷用の記述をしてます。


style.scss
----------------
上記のcoreファイルを読み込んでます。



参考サイト
----------------
* [【Sassを覚えよう！】もくじ的なのと参考リンク](http://css-happylife.com/archives/2012/0130_0415.php) -- `CSS HappyLife`
* [NAVERでのSassの使い方](http://tech.naver.jp/blog/?p=1027) -- `NAVER Engineers' Blog`
* [sassを使ってCSSのめんどくさい繰り返し部分を楽に記述する](http://css-eblog.com/sass/sass-loop.html) -- `CSS-EBLOG`
* [Less & Sass Advent calendar 2011](http://atnd.org/events/21919) -- `atnd`
# Vivliostyleで<br>レポートを書こう！ {.cover}

## @yasako {.author-name}

<!-- ![](https://q.trap.jp/api/v3/public/icon/yasako){width=35} -->


# 自己紹介

<div class="horizontal-container">


- traQ ID「**yasako**」（25B）
- 所属している班
  -  SysAd班 / グラフィック班 / CTF班 /<br>アルゴリズム班
- 趣味
  - パソコン / ピアノ / オタマトーン
- 頑張りたいこと
  - Web / 3DCG / CTF / 競プロ


<img src="https://q.trap.jp/api/v3/public/icon/yasako" width="350px" height="350px"/>

<!-- ![](https://q.trap.jp/api/v3/public/icon/yasako){width=350} -->


</div>

# 注意してほしいこと

- 他の組版ソフトと比較することがあります
  - もちろん、他の組版ソフトの方が優れている点もあります。<span style="font-size: 20px">~~他の組版ソフトの方が優れていることが多いです~~ </span>
- Vivliostyleにそこまで詳しいわけではありないため、誤った情報が含まれるかもしれません。
- 公式ドキュメントが最新バージョンに合わせて更新されていないことが多いです。
- 自分用にカスタマイズするには、CSSの知識が必要です。

# Vivliostyleの全体像{.chapter-heading}

# そもそもVivliostyleって？

- CSS組版のためのソフトウェア
  - HTML/CSSなどのWeb技術で組版をする
- traP Tech Book で、PDFを出力する際に使用している<br>らしい...？

# 組版とは？

- 印刷物の紙面に文字や図などを配置し、レイアウトする
- フォント、文字サイズ、行間の広さ、1行の文字数、<br>改行位置、余白....　などについて考える
- 例えば...
  - 見出し：プロポーショナルフォント
  - 本文：等幅フォント

# 組版ソフトの例：Word

- 簡単
- WISIWG（What You See Is What You Get）
- お金がかかる
- 構造化された文章を書くのがつらい
  
# 組版ソフトの例：Word

![](./assets/word_tokikake.png){style="border:1px solid #bbb"}

<!-- <div class="vertical-container"> -->

<!-- <img src="./assets/word_tokikake.png" width="600px" style="margin: 0 auto; border: 1px solid #aaa; overflow: hidden;"> -->



<!-- </div> -->

# 組版ソフトの例：Word

![](./assets/word_tokikake_content.png){style="border:1px solid #bbb"}

<!-- <div class="vertical-container"> -->

<!-- <img src="./assets/word_tokikake_content.png" width="900px" style="margin: 0 auto; border: 1px solid #aaa;"> -->

<!-- </div> -->

# 組版ソフトの例：Indesign

- ほとんど使ったことがないので僕はわかりません
- 組版ソフトウェアのデファクトスタンダードらしい

# 組版ソフトの例：その他

- 朝刊太郎(使ったことはありません)
- 一太郎(使ったことはありません)
- ~~Microsoft Publisher~~
  - 26年でサポートが切れるらしい

# 組版ソフトの例：？？？

<!-- <img src="./assets/powerpoint_poster.jpg" width="350px" style="margin: 0 auto;"> -->

![](./assets/powerpoint_poster.jpg)

<!-- <img src="./assets/powerpoint_poster.jpg"> -->

# 組版ソフトの例：？？？

![](./assets/powerpoint_poster_up.jpg)

<!-- <img src="./assets/powerpoint_poster_up.jpg" width="700px" style="margin: 0 auto;"> -->

# 組版ソフトの例：？？？

![](./assets/powerpoint_poster_down.jpg)

<!-- <img src="./assets/powerpoint_poster_down.jpg" width="700px" style="margin: 0 auto;"> -->

# 組版ソフトの例：PowerPoint

![](./assets/powerpoint_window.jpg)

<!-- <img src="./assets/powerpoint_window.jpg" width="700px" style="margin: 0 auto;"> -->


# 組版ソフトの例：$\mathrm \TeX$

![](./assets/tex_sample.png)
<!-- <img src="./assets/tex_sample.png" width="900px" style="margin: 0 auto; border: 1px solid #aaa;"> -->

# Vivliostyleを用いた組版の流れ

- 入力ファイル
  - 原稿
    - Markdown
    - HTML
  - スタイルファイル
    - 公式・非公式テーマ
    - 自分で作ったCSSファイル

# Vivliostyleを用いた組版の流れ

- 出力ファイル
  - 一時ファイル
    - HTML (Markdownを入力した場合)
    - pablication.json （出力するドキュメントの情報をまとめたファイル）
  - 完成品
    - PDF
    - EPUB

# 内部の仕組み

（詳しくは公式ドキュメントやソースコードを参照のこと）

- Vivliostyle.js
- Vivliostyle CLI
<!-- - を定義したCSSファイルを元に、印刷可能なPDFファイルを生成する。 -->
  - PDF生成には、内部でChromiumを使用している

# Vivliostyleの良い点と欠点{.chapter-heading}

# Vivliostyleの良い点(1/3)

- 環境構築
  - とても簡単
- 執筆
  - Markdownで書ける
  - HTMLも使える
  - Webの知識がそのまま使える
  - TeXの数式が書ける()

# Vivliostyleの良い点(2/3)

- ファイル内にリンクを貼れる
- 図表番号の参照ができる
- 見出しの番号を自由にカスタマイズできる
- ヘッダーとフッターを簡単のカスタマイズできる
- CSSについて分からないことがあったとき、AIに聞いたら大体教えてくれる

# Vivliostyleの良い点(3/3)

- 開発が活発（次の例は Vivliostyle cli）
  - v9.0.0 のリリースは 2025/5/3
  - v9.2.0 のリリースは 2025/6/10
  - 約一か月の間に、最新版のリリースが5回あった

# Vivliostyleの良くない点

- ネットにある情報が少ない
  - ユーザーが少ないため
  - もっといろんな人に広めたい！
- 公式ドキュメントの更新が追いついていない
  - 開発が早いものの、コントリビューターが少ない
- 結局のところ試行錯誤は必要
  - どの組版ソフトも同じ？


# 実際に使ってみる{.chapter-heading}

# インストール・環境構築

- 使い方
    - `npm create book`
      - CLIの質問に答えることで、プロジェクトを作成できる
      - テーマを選択（今回は academic を使用）
    - `npm run preview`
      - ブラウザでプレビューが可能
    - `npm run build`
        - PDFを生成する

# インストール・環境構築


![](./assets/install/install_01.jpg)

<!-- <div class="horizontal-container"> -->
  <!-- <img src="./assets/install/install_01.jpg" style="display: block; margin-left: auto; margin-right: auto; height:70%; padding-block:0.5em;"> -->
<!-- </div> -->

# インストール・環境構築

![](./assets/install/install_02.jpg)

# インストール・環境構築

![](./assets/install/install_03.jpg)

# インストール・環境構築

![](./assets/install/install_04.jpg)

# インストール・環境構築

![](./assets/install/install_05.jpg)

# インストール・環境構築

````.gitignore
# Vivliostyle
.vivliostyle/*
````


# サンプルを出力してみる

（VSCodeでマークダウンを開き、ブラウザでプレビューをを開いている画像）

# サンプルを出力してみる
（出力したPDFの画像）

# 図・表の挿入/参照
```md 画像の挿入
![キャプション](path/filename.png){.fig #figure-filename}
```

- {} の中に書いたclassやidを付与できる
- `figure-filename` は、一意であればなんでもOK

```md 画像の参照
[](#figure-filename){.fig-ref}
```
- マークダウンのリンクを挿入している

# 図・表の挿入/参照

```css
.fig-ref::after {
  content: "図" target-counter(attr(href url), vs-counter-fig);
}
```
- `vs-counter-fig` は Vivliostyle の base theme で定義されたカウンタ


# 数式の挿入

# ノンブル、柱、ヘッダー、フッター

# カウンタ変数の定義

# Running Head

# CSSのカスタマイズの例{.chapter-heading}

# base theme って？

# 枠を実装してみる
- ボーダー
- 見出し要素がある時は背景白の
- 箱を表示

# 数式番号を表示してみる

# 注釈
- 傍注を作る
- URLを注釈にしない

# 今後やってみたいこと

- マークダウン記法を独自に拡張
- tailwind CSSの導入
- 自作スタイルの見た目の改善
  - 余計な余白など

# ちなみに{.cover}


# 

<div class="vertical-container">
<strong style="text-align: center;">このスライドもvivliostyleで作りました</strong>


<!-- ![](./assets/vivliostyle-intro-vscode.png){width=800 style="margin-inline: auto;"} -->

<img src="./assets/vivliostyle-intro-vscode.png" width=800px style="margin-inline: auto;">

</div>

# 参考資料

- [VFMで学会論文を書いてVivliostyleで組んで投稿する［前編］](https://gihyo.jp/article/2025/02/vivliostyle-05)
- <https://github.com/vivliostyle/vivliostyle-cli>


# ご清聴ありがとうございました！！

- [組版とは？](#組版とは)（Word / Indesign / $\mathrm \TeX$）
- [Vivliostyleの良い点と欠点](#vivliostyleの良い点と欠点)
- 実際に使ってみる
- 図・表・数式の挿入/参照
- ノンブル、柱、ヘッダー、フッター
- カウンタ
- Running Head
- 今後やってみたいこと

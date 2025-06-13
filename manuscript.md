# Vivliostyle で<br>レポートを書こう！ {.cover}

## @yasako {.author-name}

<!-- ![](https://q.trap.jp/api/v3/public/icon/yasako){width=35} -->

# 自己紹介

<!-- ![](https://q.trap.jp/api/v3/public/icon/yasako){width=300} -->
<img src="https://q.trap.jp/api/v3/public/icon/yasako" class="float-right"/>

- 名前：yasako
- 学年：25B

# 自己紹介

- 班
  - アルゴリズム班 / CTF 班 / SysAd 班 / グラフィック班
- 趣味

  - パソコン / ピアノ / オタマトーン

- 頑張りたいこと
  - Web / 3DCG / 競技プログラミング / CTF

# 注意してほしいこと

- 他の組版ソフトと比較することがあります
  - もちろん、他の組版ソフトの方が優れている点もあります。<span style="font-size: 20px">~~他の組版ソフトの方が優れていることが多いです~~ </span>
- Vivliostyle にそこまで詳しいわけではありないため、誤った情報が含まれるかもしれません
- 公式ドキュメントが最新バージョンに合わせて更新されていないことが多いです
- 自分用にカスタマイズするには、CSS の知識が必要です

# Vivliostyle の全体像{.chapter-heading}

# そもそも Vivliostyle って？

- CSS 組版のためのソフトウェア
  - HTML/CSS などの Web 技術で組版をする
- traP Tech Book でも、PDF を出力する際に使用しているらしい...？

# 組版とは？

- 印刷物の紙面に文字や図などを配置し、レイアウトする
- フォント、文字サイズ、行間の広さ、1 行の文字数、<br>改行位置、余白....　などについて考える
- 例えば...
  - 見出し：プロポーショナルフォント
  - 本文：等幅フォント

# Vivliostyle を用いた組版の流れ

- 入力ファイル
  - 原稿
    - Markdown
    - HTML
  - スタイルファイル
    - 公式・非公式テーマ
    - 自分で作った CSS ファイル

# Vivliostyle を用いた組版の流れ

- 出力ファイル
  - 一時ファイル
    - HTML (Markdown を入力した場合)
    - pablication.json （出力するドキュメントの情報をまとめたファイル）
  - 完成品
    - PDF
    - EPUB

# 内部の仕組み

（詳しくは公式ドキュメントやソースコードを参照のこと）

- Vivliostyle.js
- Vivliostyle CLI
  <!-- - を定義したCSSファイルを元に、印刷可能なPDFファイルを生成する。 -->
  - PDF 生成には、内部で Chromium を使用している

# Vivliostyle の何が良いの？

- Markdown で書ける
- Web の知識がそのまま使える
- 環境構築が楽
- TeX の数式が書ける
- ファイル内にハイパーリンクを貼れる
- 図表番号の参照ができる
- 見出しの番号を自由にカスタマイズできる
- ヘッダーとフッターを簡単のカスタマイズできる

# 有名な組版ソフトとの違い

- デメリット
  - ネットにある情報が少ない
  - 公式ドキュメントの更新が追いついていない

# bbb

- aaa
  - ファイル内にハイパーリンクを貼れる
  - 図表番号の参照ができる
  - 見出しの番号を自由にカスタマイズできる
  - ヘッダーとフッターを簡単のカスタマイズできる
- デメリット
  - ネットにある情報が少ない
  - 公式ドキュメントの更新が追いついていない

# 実際に使ってみる{.chapter-heading}

# インストール・環境構築

- 使い方
  - `npm create book`
    - CLI の質問に答えることで、プロジェクトを作成できる
    - テーマを選択（今回は academic を使用）
  - `npm run preview`
    - ブラウザでプレビューが可能
  - `npm run build`
    - PDF を生成する

# インストール・環境構築

（CLI の画像）

# サンプルを出力してみる

（VSCode でマークダウンを開き、ブラウザでプレビューをを開いている画像）

# サンプルを出力してみる

（出力した PDF の画像）

# 図・表の挿入/参照

```md 画像の挿入
![キャプション](path/filename.png){.fig #figure-filename}
```

- {} の中に書いた class や id を付与できる
- `figure-filename` は、一意であればなんでも OK

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

# CSS のカスタマイズの例{.chapter-heading}

# base theme って？

# 枠を実装してみる

- ボーダー
- 見出し要素がある時は背景白の
- 箱を表示

# 数式番号を表示してみる

# 注釈

- 傍注を作る
- URL を注釈にしない

# 今後やってみたいこと

- マークダウン記法を独自に拡張
- tailwind CSS の導入
- 自作スタイルの見た目の改善
  - 余計な余白など

# ちなみに{.cover}

#

<div style="text-align: center;">
このスライドもvivliostyleで作りました

<!-- ![](./assets/vivliostyle-intro-vscode.png){width=800 style="margin-inline: auto;"} -->

<img src="./assets/vivliostyle-intro-vscode.png" width=850px style="margin-inline: auto;">

</div>

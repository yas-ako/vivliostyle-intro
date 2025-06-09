# Vivliostyleで<br>レポートを書こう！ {.cover}

## @yasako {.author-name}

<!-- ![](https://q.trap.jp/api/v3/public/icon/yasako){width=35} -->


# 自己紹介

![](https://q.trap.jp/api/v3/public/icon/yasako){width=300 .float-right}


- 名前：yasako
- 学年：25B


# 自己紹介

- 班
  - アルゴリズム班 / CTF班 / SysAd班 / グラフィック班
- 趣味
  - パソコン / ピアノ / オタマトーン

- 頑張りたいこと
  - Web / 3DCG / 競技プログラミング / CTF

# 注意してほしいこと

- 他の組版ソフトと比較することがあります
  - もちろん、他の組版ソフトの方が優れている点もあります。<span style="font-size: 20px">~~他の組版ソフトの方が優れていることが多いです~~ </span>
- Vivliostyleにそこまで詳しいわけではありないため、誤った情報が含まれるかもしれません
- 公式ドキュメントが最新バージョンに合わせて更新されていないことが多いです
- 自分用にカスタマイズするには、CSSの知識が必要です

# Vivliostyleの全体像{.chapter-heading}

# そもそもVivliostyleって？

- CSS組版のためのソフトウェア
  - HTML/CSSなどのWeb技術で組版をする



# 組版とは？

- 印刷物の紙面に文字や図などを配置し、レイアウトする
- フォント、文字サイズ、行間の広さ、1行の文字数、<br>改行位置、余白....　などについて考える
- 例えば...
  - 見出し：プロポーショナルフォント
  - 本文：等幅フォント

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
    - EUPB

# 内部の仕組み

（詳しくは公式ドキュメントやソースコードを参照のこと）

- Vivliostyle.js
- Vivliostyle CLI
<!-- - を定義したCSSファイルを元に、印刷可能なPDFファイルを生成する。 -->
  - PDF生成には、内部でChromiumを使用している

# 実際に使ってみる{.chapter-heading}

# インストール・環境構築

- 使い方
    - npm create book
    - npm run preview
        - ホットリロードありのビューワーが使える
    - npm run build
        - PDFを生成する

# aaa

- メリット
    - Markdownで書ける
    - Webの知識がそのまま使える
    - 環境構築が楽
    - TeXの数式が書ける
    - ファイル内にハイパーリンクを貼れる
    - 図表番号の参照ができる
    - 見出しの番号を自由にカスタマイズできる
    - ヘッダーとフッターを簡単のカスタマイズできる
- デメリット
    - ネットにある情報が少ない
    - 公式ドキュメントの更新が追いついていない

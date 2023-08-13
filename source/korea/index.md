# PyCon Korea 2023

* イベント概要

## 移動

* 20:00過ぎに空港にインチョンに到着
* immigrationがものすごい人(海外パスポート
* 

## 受付

* 少し迷った
* SMSを受け取っているはずだけど受け取れていない。スタッフに助けてもらって受付できた。ありがたい
* SWAG紹介

## オープニング

* なにしゃべってるか当然わからない

## キーノート

* 昔からPythonを使っている方のようで、Python 1, 2, 3での違いについて紹介しているよう。
* strとunicode
* stringメソッド(python 1ではstringの関数だった(知らなかった
  * upper, translate, join
* 並行してその当時の韓国のPythonコミュニティの話をしているっぽい

### RustPython

* RustPythonの紹介
* ruffはRustPythonのParserがあるからできたのか、なるほど
* pylyzer: https://github.com/mtshiba/pylyzer
  * mypy、pyright的なやつのrust実装
  * 作ってるの日本の人だ! https://twitter.com/s_sbym
* Seahorse (Beta) | Solana programs in Python https://seahorse-lang.org/

## 自分の発表

* 最初トラブった
* システムとしてgoogle slideで統一していたが、revealjsだったので個別に対応してもらった
  * ありがとう
  * スタッフとシステムの人にもいろいろ協力してもらった
* 手元のスピーカーノートが確認できなくて積みかけた
* 発表はなんとか終了、質疑応答も4つくらいできた
  * nestできる?
    * 普通にできます。ただあんまりcaseの中にさらにmatchを書くのはないかなーと思う
  * if文とどっちを使うべき?
    * 場合による。リテラルパターンみたいなシンプルなものはif文のままでいいと思う
  * パフォーマンスはどうなっている
    * パフォーマンスの改善は今後も継続的にやっていくという話があったはず
  * 複雑なJSONの処理だとcaseのところがすごく長くなりそう
    * ifとどっちがいいか、実際に書いてみて比較してみるとよいと思う

* 終わった後にも何人かと話ができた。日本語ができる人もいてすごい

### jupyter book

* Jupyter Bookでコンテンツを共有しようという話
* https://jupyterbook.org/en/stable/start/overview.html
* スライドの中で動画で実際のページ(scikit-learn等)の例を説明(イメージしやすい
* ipynbでダウンロードしたり、binder、colabで実行したりできる(へー
* 設定と目次はymlなんだー
* build手順、github pagesでの公開方法

### Improving debuggability of complex asyncio applications

## LT, Closing

* 最初にOrganizerからリボンの話
* PyCon USのをまねした?
* なんかたくさん作ることになって、それをカットして作るの大変だったらしい

* balpan CLIを作った

  * コードにTODOコメントを入れる?
  * tree-sitterってのを使っている?
* KwonHan

  * PSF Directorになったよ
  * アジアはPSFではMinorだよ
  * PyCon US 2023に行った。PyCon Koreaでの10年を発表した
  * メールアドレスが下手でメールが来てなかった
  * 朝スクーター乗ろうとしたけどフンダイのApple Payで決済できなかった→夜の発表になった
  * 韓国で、アジアで2人めのPSF Directorになったよ

## 飲み会

* スタッフとスピーカー飲み会に参加
* チキンとビールの店
* KwonHan、Younggunも一緒
* 参加者が減っているという話を聞いた。日本と状況は似ている感じ
* スポンサーも少ないらしい

## 2日目

* 名札の色が違う
* 1日ごとのチケットがるので日ごとに受付するスタイル。名札の色が変わる

### Pythonで月数百円で社内Slackbotを運営してみた話

* https://2023.pycon.kr/session/44
* Flask + Bolt for Pythonでアプリを作成
* Zappaを使っているらしい
* AWS API Gateway + Lambda
* まずはサイコロ機能を作成
* eventとか使用できるAPI設定とかは私のトークと同じような話をしてるかな
* Notion APIをたたいてページを検索するスラッシュコマンドを作成
* Notionから休みの情報を取得。Block Kitを使用してメッセージをいい感じにする例
* ChatGPTのAPIをたたく機能。async_chatbot_processを使って非同期で実行(へー)
  * Zappaのasynchronous.taskを使用

### 오픈소스와 함께 성장하기 (Feat. Django)

* https://2023.pycon.kr/session/41
* Jordan
* オープンソースにPRを送ると品質の高いレビューが受けられる
* テストコード、チケット管理、CI/CD、ドキュメント、コードレビューといった良いプロジェクト運営を知ることができる
* 普段は経験できないレイヤーについて学ぶことができる。Django ORMへのコントリビュートによってDB、SQLについて深く知る
* 英語とコミュニケーションスキルが成長する
* レビューしてくれた人にグローバルのイベントで会えるかもしれない

* 最初はすでにあるプロジェクトに参加して貢献することがおすすめ
* コード全体が大きいときは興味のあるコンポーネントからはじめる
* 最初の人向けの課題がgithubでラベルが付いているので、そこからはじめる
* ChatGPTを使ってコードを読む

* OSSへのコントリビューションについてのイベントもあるらしい
* Sprintに参加する

### ライトニングトーク

*

### Closing

* aaa

### After Conference

* aa

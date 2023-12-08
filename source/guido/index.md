# Guido氏インタラクティブ記念講演会レポート

鈴木たかのり([@takanory](https://twitter.takanory))です。
2023年11月後半にPythonの作者であるGuido van Rossum氏が来日することとなり、11月30日（木）に急遽イベントが開催されました。
本記事ではそのイベントの内容をレポートします。

## イベント概要

本イベントの概要は以下の通りです。

| 項目| 内容 |
|--|--|
| Web | [Guido氏インタラクティブ記念講演会 PyCon JP枠 - connpass](https://pyconjp.connpass.com/event/301716/) |
| 日時 | 2023年11月30日（木） 15:00-17:00 |
| 会場 | 東京大学 浅野キャンパス 武田ホール |
| 共催 | [東京大学AIセンター](https://www.ai.u-tokyo.ac.jp/ja/)、[情報処理学会](https://www.ipsj.or.jp/)、[NEC](https://jpn.nec.com/)、[日本ディープラーニング協会](https://www.jdla.org/) |
| 協力 |  [一般社団法人PyCon JP Association](https://www.pycon.jp/) |

```{figure} images/banner.png
:width: 400

イベントバナー
```

今回なぜGuido氏が来日したのか、なぜ本イベントが開催されたか背景について簡単に紹介します。

NEC C&C財団は**C&C賞**という情報処理技術などに貢献した人の表彰を毎年行っています。
そして[2023年度C&C賞受賞者](https://www.candc.or.jp/kensyo/2023/2023_prize_cc.html)としてGuido氏が選ばれました。
その表彰式のために初来日することとなったのです。

表彰式準備などのやり取りの中で、情報処理学会副会長でAIセンター教授でもある松原先生から「もう1日滞在を延ばしてイベントをやりませんか？」と提案し、上記4団体での共催でのイベント開催が決定したそうです。
イベントの内容としてGuido氏から「一方的なトークではなく、日本のコミュニティのみなさんと交流したい」という要望がありました。
イベント内容を検討する段階で日本ディープラーニング協会（JDLA）事務局の大谷さんから、PyCon JP Association代表理事の筆者に相談が来ました。
その後、打ち合わせで方針を決め、筆者含むPyCon JPコミュニティが中心となってイベントを運営して、本イベント「インタラクティブ記念講演会」が開催されました。

## イベントタイムテーブル

イベントはざっくり以下のようなタイムテーブルで開催しました。

|時間|内容|
|--|--|
|14:30|開場・受付|
|15:00|開会あいさつ、**GuidoさんにQ&A**、休憩|
|15:45|**Guidoさんに活動を見てもらう**、休憩|
|16:20|**GuidoさんにライブQ&A**|
|16:30|閉会あいさつ、記念撮影|
|16:40|フリータイム|

本レポートではメインコンテンツである、3つの「Guidoさんに○○」について簡単にレポートします。

## GuidoさんにQ&A

「GuidoさんにQ&A」のコーナーでは、事前に参加者からGuidoさんに聞きたいことをフォームで集め、そのうちのいくつかにその場で回答してもらいました。
MCはJDLAのシバタアキラさんとPyCon JP AssociationのJonasさんです。

```{figure} images/qanda.jpg
:width: 600

Q&Aの様子
```

質問に使用したスライドは以下のURLで公開しています。
全部で7つの質問をしました。質問を投稿してくれたみなさん、ありがとうございます。
ここではいくつかの質問とその回答を紹介します。

* [GuidoさんにQ&A](https://docs.google.com/presentation/d/13jBeDL0cHRB9VP8c8kYeMTw323UgxVV1r4rdlecsYNk/edit)

### 「他の人に使ってもらうツール」に大切なこと

* 質問： 「他の人に使ってもらうツール」を作る上で大切なことは何だと思いますか？
* 他の人が何を望んでいるかを知ることは難しく、まずは自分が求めているものを他の人も求めていると考えてはじめることが最初のステップです。
  そのあとは、自分のツールを他の人に見せたり、フィードバックをもらうことができます。
  Pythonは30年間、公開前からそのようにしています。

  ユーザーにフィードバックを求めましょう。
  彼らが求めている機能を追加するのではなく、ユーザーにどういう問題が存在するのかを理解し、その問題を解決する機能を実装します。
  ユーザーが使っているところを見て、ユーザーの声に耳を傾けます。

### GILロックの削除計画

* 質問：GILロックの削除計画について知り興奮しました。最新の情報はありますか？また、今後のPython開発計画において同様にエキサイティングな計画はありますか？
* GILには良い点と悪い点があります。
  GILがあるためにPythonでマルチコアプログラミングが困難であるため、GILを削除したいと考えています。
  その反面、Pythonの実装はGILによってシンプルになっています。
  
  Sam GrossによるGILを除去したPythonのプロトタイプがあります。
  現在、プロトタイプの変更をPythonのメインコードへのマージを進めています。
  ただし、Pythonインタープリターが安定するまでは数年かかります。
  Pythonは年に1回10月にメジャーリリースが行われます（2023年に3.12がリリースされた）。
  Python 3.13からは、ソースコードをbuildするときにGILをオフにするオプションがあります。
  今から約5年後にリリースされるPythonには、GILが存在しない可能性が高いです。
  
  他の最大の開発方針としてはJIT（ジャスト・インタイム・コンパイラ）の計画が進んでいます。
  Python 3.13でオプションで設定できる可能性があります。
  
### Pythonにコミットし続けた理由
  
* 質問：あなたが30年以上Pythonという言語や周辺のコミュニティへコミットし続けていたのは周知の事実です。
  並大抵のことではないですが、何がそれを可能にしたのでしょうか？
* 私が継続できたのはPythonコミュニティの存在によると思います。すべての人々、カンファレンス、ワークショップ、書籍、Webサイト、コア開発チームなど、それらが私をつなぎ止めています。
  Python以前のソフトウェアに対して記事などを書きましたが、成功しなかったためコミュニティとのつながりを感じていません。
  Pythonの成功は私にとっては一種の麻薬のようなものです。
  
* 参考：[#02　Faster CPythonやGILの除去によるPythonの高速化 ―EuroPython Day 2、Day 3セッションレポート | gihyo.jp](https://gihyo.jp/article/2022/09/europython2022-02)

```{figure} images/guido1.jpg
:width: 600

質問に回答するGuidoさん
```

## Guidoさんに活動を見てもらう

2番目は「Guidoさんに活動を見てもらう」のコーナーです。
ここでは、Pythonに関連する自身が関わっている活動を、3分の短い英語プレゼン（ライトニングトーク）で発表してもらいます。
そして、各発表後にGuidoさんから感想などのコメントをもらうというものです。
MCは[PyLadies Tokyo](http://tokyo.pyladies.com/)のなつこさんとまーやさんです。

```{figure} images/pyladies.jpg
:width: 600

MCの2人
```

以下の6名が発表をしてくれました。ありがとうございます。

* CuPy / Kenichi Maehashi
* Active learning to reduce annotation effort / Pieter Blok
* Python as a tool to reverse-engineer hardware / Takumi
* sphinx-new-tab-link / nikkie
* Control Model Train with Python! / Naoki Nakanishi
* My contributions to `comtypes` / Jun Komoda

なお、発表資料は以下のconnpassページですべて公開されています。

* [Guido氏インタラクティブ記念講演会 PyCon JP枠 - Media List - connpass](https://pyconjp.connpass.com/event/301716/presentation/)

ここでは、Pieter BlokさんとJun Komodaの発表を紹介します。

### Active learning to reduce annotation effort / Pieter Blok

1つ目に紹介するのは、東京大学の研究室に所属するPieter Blokさんによる発表です。

```{figure} images/pieter.jpg
:width: 600

Pieter Blokさん
```

自身が研究で行っている、ディープラーニングのためのアノテーションについてです。
画像のアノテーションには時間がかかり、農業の分野で画像にアノテーションするためには専門的な知識も必要です。
そこで、Monte Carlo dropoutという手法を用いて、不確実性の高い画像を抽出し、その画像を再度トレーニングに使用することで、アノテーションが効率的に行われるようになったそうです。

コードは以下のリポジトリにあります。

* [pieterblok/maskal: Active learning for Mask R-CNN in Detectron2](https://github.com/pieterblok/maskal)

Guidoさんからは「農業以外の多くの分野に応用できそう。コードをオープンソース化していることはとても良いことだ。」というコメントがありました。

```{figure} images/guido2.jpg
:width: 600

プレゼンを見てコメントするGuidoさん
```

### My contributions to `comtypes` / Jun Komoda

2つ目に紹介するのは、Jun Komodaさんによる[compytes](https://pypi.org/project/comtypes/)というライブラリへの貢献についての発表です。

```{figure} images/komoda.jpg
:width: 600

Jun Komodaさん
```

comtypesは軽量なPython用のCOM用のパッケージです。
[WindowsのCOM](https://learn.microsoft.com/ja-jp/windows/win32/com/component-object-model--com--portal)とpure Pythonでやりとりするための機能を提供します。

Komodaさんはこのライブラリに静的型付け導入するように貢献をしています。
この貢献により、comtypesを使用したプログラミングで動的に生成されたモジュールに対して型アノテーションの情報が付加されるため、コーディング時にエディターがメソッドやプロパティの一覧を表示できるようになったそうです。

comtypesは現在もPython 2.7をサポートしており、今後はPython 2対応を削除してコードをよりモダンにしていきたいとのことでした。

Guidoさんからは「Python 2.7は過去の遺産なので、Python 2.7対応の削除に取り組んでいくことを嬉しく思います。型アノテーションがあることでエディターで型情報が確認できるのは便利ですね。」といったコメントがありました。

## GuidoさんにライブQ&A

最後のコーナーは「GuidoさんにライブQ&A」です。
ここでは、[slido](https://www.slido.com/)を使って、来場者からその場で集めた質問に対してGuidoさんに回答してもらいます。
「質問が集まらなかったらどうしよう」と運営スタッフは心配していましたが、40個を超える質問がありました。ありがとうございます。

MCの2人は質問を選ぶのが大変そうでした。
MCはふたたびシバタさんとJonasさんです。

```{figure} images/live-qanda.jpg
:width: 600

Live Q&A
```


いくつかの質問とその回答を紹介します。

(TODO: いくつかの質問と回答を載せる)

## 運営裏話

* ステッカー作ったよ
* あとなにかなぁ

## 終わりに

* いろんな人の協力でイベントが成功した。関係者皆さん、とくにGuidoさんに感謝。
* イベント全編や写真は公開予定なので、後日このレポートも更新するし、[PyCon JP Blog](https://pyconjp.blogspot.com/)でもお知らせ予定
* PyCon JP TVでも簡単に紹介したので見てね
* PyCon US 2024でGuidoさんに会わないと。さすがにもう忘れてないはず!!

```{figure} images/party.jpg
:width: 400

関係者を交えての食事会
```

# PyCon Korea 2023

鈴木たかのり([@takanory](https://twitter.com/takanory))です。
2023年8月に韓国のソウルで開催された、プログラミング言語Pythonカンファレンス「PyCon Korea 2023」に参加してきたので、その様子をレポートします。

## PyCon Korea 2023とは

PyCon Koreaは韓国で開催されるPythonに関するカンファレンスです。
2022年は一部オフラインでしたが基本はオンライン開催、2023年は久しぶりのフルでのオフライン開催でした。

PyCon Korea 2023のイベント概要は以下の通りです。

|項目|内容|
|--|--|
|URL|<https://2023.pycon.kr/>|
|日程|チュートリアル、スプリント: 2023年8月11日（金）|
| | カンファレンス: 2023年8月12日（土）、13日（日）|
|場所|韓国、ソウル|
|会場|[Coex](https://www.coexcenter.com/)|
|参加費|1日 80,000 KRW、2日 140,000 KRW|

```{figure} images/pyconkr.png
:width: 600

PyCon Korea 2023 Webサイト
```

筆者は2016年に韓国で開催されたPyCon APAC 2026 in Korea以来の参加です。
2016年の様子は以下のレポートを参照してください。

* [第1回　現地の様子とカンファレンス1日目 ～pandas開発者によるKeynote～ | gihyo.jp](https://gihyo.jp/news/report/01/pycon-apac2016/0001)
* [第2回　カンファレンス2日目 ～Flask開発者・PyPy開発者によるKeynote～ | gihyo.jp](https://gihyo.jp/news/report/01/pycon-apac2016/0002)

## 韓国への移動

韓国へは8月11日(金)の夜に移動しました。
22:20くらいにインチョン国際空港に到着しましたが、海外パスポートの人の入国管理がものすごい行列でした。
結局、空港の外に出られたのが23:50頃で、バスでソウル市内への移動は時間がかかり疲れていたので、タクシーでホテルに移動しました。


```{figure} images/inchon.jpg
:width: 600

インチョン国際空港に到着
```

## カンファレンス1日目

カンファンレンス1日目はCoex（会場）の入り口を間違えて中で少し迷いましたが、無事に会場に着くことができました（Coexはとても広いです）。

```{figure} images/coex.jpg
:width: 600

Coex
```

受付では事前にSMSで送信されたQRコードを使用するそうですが、私は韓国の電話番号を持っていないためそのSMSを受け取れていませんでした。
スタッフの方に名前を告げて無事に受付できました。

```{figure} images/reception.jpg
:width: 600

受付
```

受付ではグッズを受け取りました。
IKEAっぽい黒いバッグの中にパンフレット、Tシャツ、うちわ、ステッカーなどが入ってました。

```{figure} images/bag.jpg
:width: 600

バッグ
```

```{figure} images/tshirts.jpg
:width: 400

Tシャツ
```

オープニングでイベントが始まります。
すべて韓国語なので何についてしゃべっているかは全然わかりません。
写真は過去のPyCon Koreaイベントの様子のようです。

```{figure} images/opening.jpg
:width: 600

オープニング
```

### キーノート1: Pythonの歴史に関するトーク

* [우리 파이썬이의 꼬꼬마 시절](https://2023.pycon.kr/session/47)

1日目はオープニングのあとに2本のキーノートがありました。
スライドも発表言語も残念ながら韓国語です。
1本目のキーノートはかなり初期からPythonを使っている方のようで、Python1、2、3の違いについて紹介していました。

一例として文字列型(str型)の各種メソッドはPython 2から使えるようになっており、Python 1では`string`モジュールの関数だったということが示されました。

```{figure} images/keynote1.jpg
:width: 600

キーノート1
```

他にもstr型とunicode型のことや、過去のPythonと並行して当時の韓国のPythonコミュニティの紹介をしていました。
韓国でもPyConを開催する前にはミートアップなどが行われていることを知ることができました。

### キーノート2: RustPythonとコミュニティ

* [RustPython, 파이썬 커뮤니티로](https://2023.pycon.kr/session/48)

2本目のキーノートはRustPythonと関連するコミュニティに関するトークです。

[RustPython](https://rustpython.github.io/)はRustで実装されたPythonインタープリターです。
通常使っているPythonはC言語で書かれたCPythonですが、他にもJython(Java製)、PyPy(Python製)などがあり、同じようにRustで書かれています。

```{figure} images/keynote2.jpg
:width: 600

キーノート2
```

Rustで書かれた高速なPythonコードの静的解析ツールに[Ruff](https://beta.ruff.rs/docs/)があります。
Ruffは、RustPythonによってRuff製のPythonパーサー「[RustPython parser](https://rustpython.github.io/blog/2020/04/02/thing-explainer-parser.html)」を利用しているそうです。
RustPythonの資産によってRuffが作られたという説明はとても納得しました。
Ruffについては以下の記事も参考にしてください。

* [新しい静的コード解析ツール「Ruff」をご紹介 | gihyo.jp](https://gihyo.jp/article/2023/03/monthly-python-2303)

別の例として[pylyzer](https://github.com/mtshiba/pylyzer)が紹介されていました。
pylyzerはRust製のPythonのコード解析、言語サーバーです。
このツールもRustPython parserを使用しているようです。

### 自身の発表: Introduction to Structural Pattern Matching

* スライド: [Introduction to Structural Pattern Matching](https://slides.takanory.net/slides/20230812pyconkr/)

キーノートの後にランチ休憩を挟んで筆者の発表でした。
あまり準備に時間がとれなかったのと、現地での機材の確認もあったので、昼ご飯はさくっと食べて発表会場に行きました。
発表会場はなかなかの広さです。
キーノートでひと続きになっている5つの部屋を、2部屋(101/102)、1部屋(103)、2部屋(104/105)と分割して使用しています。

```{figure} images/takanory-room.jpg
:width: 600

発表会場
```

今回PyCon Korea側では発表資料をGoogleスライドで統一してほしいという要望がありましたが、私が普段使っているスライドは[sphinx-revealjs](https://sphinx-revealjs.readthedocs.io/en/stable/)を使用しておりGoogleスライドに変更するのは困難です。
そのため、スタッフや配信システム担当の方にもフォローしてもらって、自身のスライドをそのまま仕えあるようになりました。
ありがたいです。

ただ、私の事前の準備に問題があり、スピーカーノートが参照できずトークの前半はだいぶグダグダになっていしまいました。
これは非常に反省すべき点です。

発表ではPython 3.10の新機能であるStructural Pattern Matching（構造的パターンマッチ）の言語仕様と使い方を、サンプルコードを交えて紹介しました。
発表は無事終了し、いくつか質疑応答もできました。
以下に質疑応答の内容を紹介します。

* 質問: 入れ子にできるか
* 回答: if文と同様に普通に入れ子にできます。ただ、あまりcaseの中にさらにmatchを書くことはないと思います
* 質問: if文とどっちを使うべきか
* 回答: 場合によります。リテラルパターンのようなシンプルなものはif文のままでよいと思います
* 質問: パフォーマンスはどうなっているのか
* 回答: Python 3.10の段階では機能がリリースされた段階と認識しています。パフォーマンスの改善は今後も継続的に行われていくという話が、PEP 著者のBrandt Bucker氏からありました
* 質問: 複雑なJSONを処理するときにcaseのところがすごく長くなりそう
* 回答: そうなると思います。ただ、if文をネストして書くのとどっちがわかりやすいか、実際に書いてみて比較してみるとよいと思います

発表が終わった後にも引きつづき何人かとこの発表について話ができました。
この機能に興味を持ってくれて、使い始める人が増えるといいなと思っています。

### ブースの様子

会場の外にはスポンサー企業によるブースやPyCon Koreaのブースがありました。
企業ブースは参加者がよっていて盛り上がっているようです。

```{figure} images/booth1.jpg
:width: 600

企業ブース
```

PyCon Koreaブースではグーズの販売や、スタンプラリーの抽選をしているようです。
傘、ペン、靴下などさまざまなグッズが売っていました。

```{figure} images/booth2.jpg
:width: 600

PyCon Koreaブース
```

### ライトニングトーク

1日目のライトニングトークです。
ライトニングトークは1本5分程度の短いトークが連続するセッションです。

PyCon Korea主催者から、名札の下に付けるリボンを作ったLTがありました。
PyCon USでもあった自分の属性や興味があることを示すリボンです。
たくさんの種類のリボンを作ることになってカットする作業が大変だったようです。

```{figure} images/ribbon.jpg
:width: 600

リボンについてのライトニングトーク
```

また、KwonHan氏のライトニングトークもありました。
KwonHan氏はPyCon KRの立ち上げメンバーであり、筆者の以前からの友人です。
KwonHan氏がPSF（[Pythonソフトウェア財団](https://www.python.org/psf-landing/)）の2023のボードメンバーとなったことや、PyCon US 2023でのライトニングトークのことなどが語られました。

* 参考: [Python Software Foundation News: Announcing the 2023 PSF Board Election Results!](https://pyfound.blogspot.com/2023/06/announcing-2023-psf-board-election.html)


```{figure} images/kwonhan.jpg
:width: 600

KwonHan氏
```

KwonHan氏のPyCon USでのライトニングトークについては以下の記事を参照してださい。

* 参考: [#02 PyCon US 2023 後半のハイライト ―PyScript関連セッションに注目 | gihyo.jp](https://gihyo.jp/article/2023/05/pycon-us2023-002#gh6opS_OFZ)

### 飲み会

カンファンレンス1日目の終了後はスタッフとスピーカーの食事会に参加しました。
チキンとビールのお店です。

```{figure} images/chicken.jpg
:width: 600

骨なしチキンとポテト
```

コロナの影響でリアルイベントに参加者が減っているという話を聞きました。
状況としては日本と似ているなと感じました。

個人的には「若い人は骨なしチキンが好きなので、今回はこの店になった。年が上の人は骨付きチキンが好き」という話がツボでした。
確かに私も骨付きチキンの方が好きだな...

## カンファレンス2日目

このカンファレンスは1日券もあるため、両日受付をする必要があります。
私も受付をしなおして、2日目の名札をもらいました。
名札の色が違うのでわかりやすいなと思います。リボンも付けてみました。

```{figure} images/badge.jpg
:width: 600

名札(左が2日目)
```

### Pythonで安価で社内Slackbotを運営した話

* [Python으로 월 몇 백원으로 사내 슬랙봇 운영해본 이야기](https://2023.pycon.kr/session/44)

Slackbotの運用の話です。
[Flask](https://flask.palletsprojects.com/)と[Bolt for Python](https://slack.dev/bolt-python/concepts)でアプリを作成し、[Zappa](https://github.com/zappa/Zappa)でサーバーレスアプリケーションとしてAWS API Gateway + Lambda上で動作させているそうです。

```{figure} images/slackbot.jpg
:width: 600

Slackのワークフロー
```

まずはrandomモジュールを使用して簡単なサイコロ機能を実装し、そこからボットを拡張していきました。
Notion APIを叩いてページを検索するコマンドや、Notionページからメンバーの休みの情報を返す機能、非同期でChatGTPのAPIを叩く機能などを実装したそうです。

Slackbotでいろいろ楽しようというトークは私もPyConでしていたので、一方的に親近感を感じるトークでした。

### オープンソースと一緒に成長する話

* [오픈소스와 함께 성장하기 (Feat. Django)](https://2023.pycon.kr/session/41)

前日の飲み会でも同席したJordan氏により発表です。
自身がDjangoなどのオープンソースに貢献する中で、自分自身も成長していったというトークです。
オープンソースにPRを送ると品質の高いレビューを受けることで、自身のコード力が上がっていきます。
また、テストコード、チケット管理、CI/CD、ドキュメント、コードレビューといったよいプロジェクト運営を知ることができます。

```{figure} images/jordan.jpg
:width: 600

Jordan氏
```

他にも、普段は経験できないレイヤーについて学ぶ機会があり、例としてDjango ORMへの貢献をするときにDB、SQLについて深く知ることができたそうです。
また、英語とコミュニケーションスキルが成長するということ、レビューしてくれた人などの関係者にグローバルのイベントで会えるかも知れないということが利点として上げられていました。

また、OSSへの貢献の始め方として以下のような考え方、方法がお薦めされていました。

* 最初は、すでに存在するプロジェクトに参加して貢献をはじめる
* コード全体が大きいときは、興味のあるコンポーネントからはじめる
* GitHubの課題に「初心者向けの」のラベルが付いているものがある場合、その課題から着手する
* コードを読むときにChatGPTなどを使用する

そして最後に、韓国で開催されているOSSへの貢献をはじめるイベントや、PyConのスプリントに参加することがお勧めされていました。

オープンソースへの貢献とそれが自身の成長につながるという、とてもよい発表だなと思いました。

### ライトニングトーク

カンファレンス2日目もライトニングトークです。以下のような発表がありました。

```{figure} images/golang.jpg
:width: 600

ライトニングトーク
```

* Golang Koreaの紹介。2023年8月に[GopherCon Korea](https://gophercon.kr/en)が開催されたそうです。これは韓国で最初のGoに関する大規模イベントとのこと
* 大学に通いながらフリーランサーをしている方の発表。Pythonを中学生に教えたり、自らPythonを学びながら楽しんでお金を稼ぐというトーク
* めっちゃハイテンションで内容がウケている人がいました。韓国語なので当然なにもわからず。あとで動画を字幕付きで見てみたい
* Circuit Pythonでハードウェアを作る話
* 過去のPyCon Koreaにボランティアとして参加してきた話。一人での参加だが知り合いが増えた

### クロージング

イベントの最後はクロージングです。
イベントに関連する数字が紹介されていました。
1458日(4年)ぶりの現地開催のイベントで、参加者は1,100名以上、43名のスピーカーなどの数値が紹介されました。

```{figure} images/closing.jpg
:width: 600

クロージングのスライド
```

クロージングのあとはスタッフなどの記念撮影が行われていました。
私も最後の方に韓国の友人であるKwonHan氏、Younggun氏と一緒に記念撮影をしました。
2人とはPyCon US 2023でも一緒に参加し、おそらく東京で開催されるPyCon APAC 2023でも再会できると思います。
また会いましょう！

```{figure} images/korean-friends.jpg
:width: 600

KwonHan氏（左）、Younggun氏と
```

### カンファレンス打ち上げ

* aa

## まとめ

(まとめを書く)

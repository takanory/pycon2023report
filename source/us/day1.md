# Day 1

さてカンファレンス1日目です。
カンファレンス期間中は毎日朝食が出ます。助かりますね。
また、食事は全てベジタリアン用のメニューも用意されています。

```{figure} images/breakfast.jpg
:width: 600

1日目の朝食はブリトー
```

## オープニング

カンファレンスのオープニングはConference ChairであるMariatta([@mariatta](https://twitter.com/mariatta))氏からのあいさつです。
冒頭にPyCon USの20年の歴史を振り返る動画が紹介されました。
今年2023年はPyCon USが2003年に初開催されてから20回目となります（2020年は中止）。

```{figure} images/opening.jpg
:width: 600

Mariatta氏によるオープニング
```

最初に参加者、スタッフ、ボランティア、スポンサーなどへの感謝が述べられました。参加者はこの時点で2,000名ほどだそうです。
その後自らのストーリーが語られました。
Mariattaさん自身は2015年にPSFによる参加費のサポートによってPyCon USに参加し、そこで自分の人生が変わったそうです。
そこでは女性が沢山発表しており、自分もそうなりたいと思い、その後自分も発表できるようになったり、Pythonのコアデベロッパーとなっていったそうです。

そしてPyCon US 2023のイベントの紹介がおこなわれました。
キーノートスピーカー、スペシャルゲスト、89のトークは全て生中継すること、PyLadies Auction、Open Spacesなどなど。
またモバイルアプリの紹介もありました。このアプリはタイムテーブルの確認にとても便利でした。

なお、PyCon US 2023ではマスクの着用は必須です（アメリカの市内はマスクをしている人はあまりいません）。
注意を受けたら名札をスキャンして1ストライク、3回スキャンされたらアウトとなって退場になるそうです。

## Keynote: Ned Batchelder

オープニングのあとは、Ned Batchelder（[@nedbat](https://twitter.com/nedbat)）氏によるキーノートです。
Ned氏が初めて参加したPyCon USは2007年で、そのときのPythonの作者であるGuido氏のトークはPython 3.0についてのものでした（Python 3.0は2008年12月にリリースされています）。

```{figure} images/ned.jpg
:width: 600

Ned Batchelder氏
```

このトークでは「人」についての話がされました。
人は不確かで複雑です。
人には標準が存在しなく、みんな違います。
また、ドキュメントもないし、予測不可能です。
予測不可能なのは隠された状態を持っていることが原因でもあります。
また、人が発するエラーメッセージは明確ではありません。

そんな人に対しての**APIユーザーガイド**を紹介するということがこのトークの目的です。
ただし、自身は心理学者ではなくエンジニアのため、自身の経験に基づいています。
多くの人とのやりとりをリバースエンジニアリングし、うまくいかなった議論のトレースバックをもとにどうすればうまくいったかを考えたものに基づいています。

人とやりとりするメッセージには2つの部分「情報」と「感情」から構成されています。
感情を入れていないメッセージでも人は感情を見つけます。

よりよい対話をするために以下の5点が挙げられました。

* 「イエス」と言う
* より多くの言葉を使う
* 言葉を慎重に選ぶ
* 謙虚であること
* 明示的であること

そして、それぞれについて実際にありそうな会話の例を元に、こう回答するとよいと思うという説明がされました。
1つ例をあげると以下のようなやりとりです。これは「ノーと言わない」という例です。

* Aさん「この配列の長さはどうやったら取得できますか？ `arr = [1, 2, 3]`」
* Bさん「それは配列じゃないです」

こう言われるとAさんは「自分はバカだ！」と思ってしまい、よくない相互作用となります。
この場合は以下のように回答することがおすすめされました。

* Bさん「リストの長さは `len(arr)` で取得できます」
* Aさん「なるほど、リストって言うんですね、ありがとう！」

このように、各注意点ごとにどのようなやりとりをすると、よりよい対話となるかという例があげられていきました。

筆者もこのトークを「わかるなー、確かにあるなー」と思って聞いていました。
自分自身、他の人とやりとりするときに「よくない対話」をしないように気をつけようと思いました。

## Making CPython 3.11 Fast - Inside Python's new specializing, adaptive interpreter.

* スピーカー: Brandt Bucher
* スライド: [inside_cpython_311s_new_specializing_adaptive_interpreter.pdf](https://github.com/brandtbucher/brandtbucher/blob/master/2023/04/21/inside_cpython_311s_new_specializing_adaptive_interpreter.pdf)

キーノートのあとは5つのトラックに分かれてトークがあります（うち1つはスペイン語・ポルトガル語）。
ここではBrandt Bucher氏によるCPython 3.11の中身についてのトークを紹介します。
写真を見てもらうとわかりますが、スライドの日付が2022年となっており「スライドが古いよ！」と会場から声がかかり、その場で日付を直していました。

```{figure} images/brandt.jpg
:width: 600

Brandt Bucher氏
```

Brandt氏は6年前からPythonを使い始め、現在はMicrosoftのFaster CPythonチームに所属しています。
このトークではCPythonでバイトコードでどのように効率化されたかについて紹介していました。

最初に以下のクラスのサンプルコードを提示し、[dis](https://docs.python.org/ja/3/library/dis.html)モジュールの`dis()`関数でバイトコードを取得します。

```python
class Point:
    def __init__(self, x: float, y: float) -> None:
         self.x = x
         self.y = y

    def shifted(self, dx: float, dy: float) -> typing.Self:
         x = dx + self.x
         y = dy + self.y
         cls = type(self)
         return cls(x, y)
```

`dis()`関数にPython 3.11から加わった引数`adaptive=True`を指定すると、特殊なバイトコードを出力します。
すると`sel.y`で属性の値を取得するバイトコードが`LOAD_ATTR`から`LOAD_ATTR_INSTANCE_VALUE`に変わるなど、変化があります。
`LOAD_ATTR_INSTANCE_VALUE`は、クラスが前にアクセスしたときから変わっていない場合に、値の返却が速くなります。

他にも`dy + self.y`の部分が`BINARY_OP`から`BINARY_OP_ADD_FLOAT`に変わります。
これは、左右がどちらも`float`の場合に使用されます。
このように実行時に効率的なバイトコードが使用できるかを確認し、バイトコードを切り替えることで処理の高速化を図っているそうです。

また、[specialist](https://pypi.org/project/specialist/)というライブラリが紹介されました。
`$specialist hoge.py`と実行すると、Pythonコードのどの場所が上記の特殊なバイトコードを使用して最適化されるかを見た目で表現するそうです。

```{figure} images/specialist.png
:width: 600

specialistの実行イメージ
```

CPython 3.12でもさらにバイトコードは改善され、特殊なバイトコードがさらに増えるそうです。
今後も継続的に高速化されていくCPythonに注目です。

````{admonition} PyCon APACブース
このコラムは吉田([@koedoyoshida](https://twitter.com/koedoyoshida))がお届けします。

今回はPyCon APACブースをPyCon USで初出展しました。
PyCon APAC自体は2010年からAPAC地域で持ち回りで開催している国際的なPyConイベントとなりますが、イベント自体は各国のPyConのオーガナイザーが開催しているため、いままではあまり共同ではアピールはしてきませんでした。
今回ブース出展することも有り、共通ロゴやAPAC共通のWebサイト[PyCon APAC Organizers](https://pycon.asia/)を作成しました。

また、APACをアピールできる配布物や出展物を各自持ち寄りました。
PyCon JPからは日本らしく、APACで開催される主要なPyConの紹介とwebサイトを紹介する折り紙などを準備し持ち込みました。

この折り紙は鶴型に折ることができるようになっていて、APACの出展メンバーやブース訪問の参加者の方にAPACの紹介を兼ねてそのまま渡したり、英語での折り方ガイドを見せつつ、一緒に鶴を折ってそれを持ち帰ってもらったりでき、非常に好評でした。

また、PyCon US開催に合わせて[PyCon APAC 2023 CFP(Call for proposal)サイト](https://pretalx.com/pyconapac2023/cfp)をオープンできましたので、そのアピール用の資料等も現地で作成、印刷し配布できました。
APAC地域やそれ以外の国の方含めブースに良く訪問があり、PyCon USに出展してアピールできた事はとても良かったと思います。

```{figure} column-images-booth/boothimageall2.jpg
:width: 600

PyCon APACブースの様子
```

````

## オープンスペース

会期中は小さな会議室でオープンスペースというものが開催されています。
オープンスペースというのは、場所と時間枠が用意してあるので、そこで議論したいことなどがある人が議論したい内容など枠を確保するものです。
[アンカンファレンス](https://ja.wikipedia.org/wiki/%E3%82%A2%E3%83%B3%E3%82%AB%E3%83%B3%E3%83%95%E3%82%A1%E3%83%AC%E3%83%B3%E3%82%B9)とも呼ばれます。

PyCon US 2023ではカンファレンスの3日間毎日、1時間ごとにオープンスペースの枠が用意されていました。
ボードを見てみると技術系だけじゃなく、カンファレンス主催者のミートアップ、高校の先生、自転車・カヤック、広東語をしゃべる人などさまざまです。

```{figure} images/openspaces.jpg
:width: 600

オープンスペースのボード
```

筆者はそのうちの1つ、[Python Bytes](https://pythonbytes.fm/)というポッドキャストの公開収録に参加してみました。
このポッドキャストは過去にも聞いたことがありますが、Pythonに関するさまざまな話題を扱っています。

```{figure} images/pythonbytes.jpg
:width: 600

ホストのMichael氏とBrian氏
```

このときに収録されたポッドキャストはすでに公開されています。
冒頭に参加者の拍手があるのが、公開収録っぽい感じで面白いです。

* [Episode #333 Live From PyCon - \[Python Bytes Podcast\]](https://pythonbytes.fm/episodes/show/333/live-from-pycon)


## Eric Matthes氏との再会

この日は出版社[No Starch Press](https://nostarch.com/)のブースで、書籍「Python Crash Course」のサイン会が行われていました。
筆者は本書の日本語版（[必修編](https://gihyo.jp/book/2020/978-4-297-11570-8)、[実践編](https://gihyo.jp/book/2020/978-4-297-11572-2)）の翻訳者であり、PyCon US 2019年でEric氏にあいさつをしていました。

今回も書籍を購入し、著者のEric Matthes（[@ehmatthes](https://twitter.com/ehmatthes)）氏にサインをしてもらいました。
Eric氏も私のことを覚えていてくれており「日本語版無事出しましたよ」といった話をしました。

```{figure} images/eric.jpg
:width: 600

著者のEric Matthes氏と筆者
```

Eric氏からのサインには「書籍を広めるための、（翻訳の）ハードワークありがとう」というメッセージが書かれていました。
翻訳は大変でしたが、著者に直接感謝されるとやった甲斐があったなと感じます。

```{figure} images/eric-sign.jpg
:width: 600

Eric Matthes氏からのサイン
```


## ライトニングトーク

カンファレンス1日目の最後はライトニングトークです。
出力がカラフルになった[tox](https://tox.wiki/en/latest/) 4の紹介、ソースコードを読みやすくするサービス[Sourcery](https://sourcery.ai/)の紹介、Zen of Pythonについてのトークなどがありました。

スピーカーの一人に謎のマスクマンがいました。
実は彼はフィリピンから参加していたSony Valdez（[@MrValdez](https://twitter.com/MrValdez)）氏で、自身の経験としてのゲーム開発について語り、最後にAPAC地域のPyConについて紹介していました。
これより前にSony氏とはあいさつしてたんですが、マスクをかぶっていたので同じ人だと全然思っていませんでした。


```{figure} images/lt1.jpg
:width: 600

謎のマスクマンによるライトニングトーク
```

## APACメンバーでの夕食とPyParty

PyCon US 2023には日本だけで無く、多数のAPAC地域から参加しているメンバーがいました。
そこで、この日はカンファレンス終了後にみんなで集まって食事をすることにしました。
日本、韓国、台湾、香港、フィリピン、タイ、中国から合わせて20名ほどが参加し、交流を深めました。

```{figure} images/apac-members.jpg
:width: 400

APAC関連の面々
```

ここでの食事はフードコートのためお酒がありません。そこで企業（AWSとSuperblocks）が主催するパーティーに参加してきました。
場所は初日にも訪れたSquatters Pub Breweryです。
このパブは3階建てなんですが、全てを貸し切りでドリンクとフードも全部企業持ちです。太っ腹！！
スポンサー企業に感謝しつつおいしいビールをいただいて、カンファレンス1日目は終わりました。

```{figure} images/pyparty.jpg
:width: 600

PyPartyの様子
```

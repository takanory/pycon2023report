# PyCon Hong Kong 2023 カンファレンスレポート

鈴木たかのり（[@takanory](https://twitter.com/takanory)）です。2023年11月に香港で開催された、プログラミング言語Pythonの国際カンファレンス「PyCon Hong Kong 2023」に参加してきたので、その様子をレポートします。

## PyCon Hong Kong 2023とは

PyCon Hong Kong（以下：HK）は香港で開催されるPythonに関するカンファレンスです。
2015年から開催されており、今回で8回目となります。

PyCon HK 2023のイベント概要は以下の通りです。

|項目|内容|
|--|--|
|URL|<https://pycon.hk/2023/>|
|日程|2023年11月11日（土）|
|場所|香港|
|会場|[The Hong Kong Federation of Youth Groups Building](https://hkfyg.org.hk/en/venue-booking/)|

```{figure} images/pyconhk.png
:width: 600

PyCon Hong Kong 2023 Webサイト
```

筆者は今回が初めてのPyCon HKへの参加であり、香港へ行くのも初めてです。

## カンファレンス前日まで

今回は飛行機の関係で11月9日（木）に移動しました。
ここではカンファレンス前の様子を軽く紹介します。

### 香港への移動

初めて行く香港では、空港でOctopusカードというsuicaのような交通カードを購入し、Airport Expressと地下鉄（MTR）を乗り継いで、スムーズにホテルに到着することができました。

```{figure} images/octopus.jpg
:width: 400

Octopusカードの自動販売機
```

晩ご飯は到着が少し遅かったのもあり、ホテルの近くの店に適当に入って食べました。
漢字なのでなんとなくメニューの意味がわかります。

```{figure} images/kanji-menu.jpg
:width: 400

漢字のメニュー
```

このメニューで「D」を指さしして頼んだんですが、予想通りネギと鶏肉が出てきました。
この料理で48 HKDですが、現在は香港の物価高と円安もあり、1 HKDは約20円となっています。
「これで約1,000円か...」と思いながら食べました。
味は想定通りといった感じです。

```{figure} images/negi-tori.jpg
:width: 600

蔥油雞扒
```

### Speakers Dinner

カンファレンスの前日11月10日（金）の夜には、スピーカーを招待してのディナーがありました。
[Yat Lung Heen](https://www.facebook.com/YATLUNGHEEN/)というお店です。

最初に主催者のSammyとCalvinからあいさつがあり、2つのテーブルに分かれて楽しく会話をしならがらおいしい中華料理を楽しみました。

```{figure} images/speakers-dinner.jpg
:width: 600

主催者あいさつ
```

```{figure} images/dinner1.jpg
:width: 600

筆者のいたテーブル
```

```{figure} images/dinner2.jpg
:width: 600

もう1つのテーブル
```

食べきれない量の中華料理が出てきて、あまった料理は持ち帰り用に詰めてもらっていました。
これって中華料理あるあるなんですかね（台湾でもそんな感じだった）。

Dinnerのあとは一緒にビールを飲んでくれる人がいなかったので、腹ごなしがてら30分歩いて
[Hong Kong Island Taphouse ](https://www.facebook.com/HKIslandTaphouse/)を訪れ、香港のクラフトビールを軽く飲んでから帰りました。

## PyCon Hong Kong 2023

次の日の11月11日(土)がカンファレンス当日です。
MRTでQuarry Bay駅まで行ってから徒歩です。
8階がメインとなるホールとブースがある会場で、10階にTrack 2の部屋があります。

### オープニング

最初はSammy氏によるオープニングです。
今年はWebサイトを見てもわかるとおり、マージャンがデザインのテーマとなっています。
スポンサー紹介、オーガナイザー紹介などが行われました。

```{figure} images/opening.jpg
:width: 600

オープニング
```

続いてプログラム担当のScotty氏よりプログラムの概要が紹介され、そのあとに写真撮影が行われました。
オープニング直後に写真撮影って珍しいなと思いましたが、ホールの座席に詰めて座って集合写真が撮られました。

### キーノート:  Maaya Ishida

オープニングのあとのキーノートは2つの部屋で行われ、私は友人でもあるMaaya Ishidaさん（[@maaya8585](https://twitter.com/maaya8585/)）のキーノートに参加しました。

```{figure} images/maaya.jpg
:width: 600

Maaya Ishida氏
```

* PyLadiesの紹介
* 世界中にたくさんあるよ
* いろんなHQごとに言語があるのでコミュニケーションの問題があるよ
* PyLadies Tokyoのこと
  * 2014年9月発足
  * 1名がPyCon JPでポスターをやったのがきっかけ
  * 現地イベントをちょっとずつ増やしている
  * 9年間毎月実施している(すごい)
  * 女性が一般のコミュニティに参加する最初のステップになれば
  * PyLadies JapanのSlackにいろんなチャンネルがあるよ。スキューバダイビングとか
  * PyLadies Caravanの紹介
* Our Thoughts
  * Don't overdo→燃え尽きないように。スタッフが忙しいときに休める
  * 主催者がやりたいことをやる
  * 楽しむ
* PyLadiesが将来的に不要になるといいなと思っている

Q&A

* メンバーがいなくなっちゃうのはどう?
  * 難しい問題。ただいなくなって誰かが新しく入ってくればいい。いつかまたライフステージが変わったときとかに再度参加してくれるとうれしい。戻れるように場所を維持していきたい
* PyCon JPではchild careを提供しているがPyCon HKでは提供できていない。リソースの問題(Calvin

## 自分の発表

* 30分なのでだいぶとばした
* ChatGPTとつなげられる?
  * APIがあるのでつなげられる。でもSlackオフィシャルでGPTとかとつないだ機能は出ると思います
* Slack SDKを使っている?
  * Slack SDKとBolt for PythonというSlackが提供するSlack Appを作るためのフレームワークを使っている

## PyScript

* Sophiaさん
* 2022 USで発表された
* 使い方は scriptタグを書くだけだよ
  * hello world
  * event handler
* why do use pyscript
  * no instralltion
  * htmlを共有するだけなので簡単、deployも簡単
* DEMO
  * scikit-learnでクラスタリング
  * star warsの出演者の関係をd3.jsで表現
  * Pyxelでのゲームの例
* pyscript.comにサインアップしてね
  * discrodに参加してね
  
Q&A

* GPU使える?
  * 今は対応していない
* どのブラウザーに対応してる
  * スマホブラウザーでも対応している。WebAssemblyに対応していれば対応する
* Syntax highlightに対応していない

## 14:40-15:10	Automating Business Tasks with Langchain and Python

* 🇭🇰 Dr. Chung Ng | PCCW-HKT
* 途中でクイズがあって面白かった

## Automating Victory: Beating browser games with accessible Python | English

* 🇯🇵 Mr. Jon Gaul | HENNGE K.K.
* Mamono Sweeperってのをとくらしい
* https://hojamaka.com/game/mamosui_list.html
* まずは画面を見るところから
  * MSS + OepnCV
* 画面が変わった

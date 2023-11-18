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

### キーノート: Introduce to you! about PyLadies Tokyo

* トーク概要: <https://pycon.hk/2023/introduce-to-you-about-pyladies-tokyo/>
* スピーカー: Maaya Ishida

オープニングのあとのキーノートは2つの部屋で行われ、私は友人でもあるMaaya Ishidaさん（[@maaya8585](https://twitter.com/maaya8585/)）のキーノートに参加しました。

```{figure} images/maaya.jpg
:width: 600

Maaya Ishida氏
```

トークの内容としては最初に[PyLadies](https://pyladies.com/)の紹介があり、世界中に支部がたくさんあること、それぞれの支部で異なる言語を使っているため、コミュニケーションには問題があるという話がありました。

続いてMaayaさんが主催をしている[PyLadies Tokyo](http://tokyo.pyladies.com/)についての紹介がありました。
2014年9月に発足し、そのきっかけは1人の女性PythonistaがPyCon JPでポスターセッションを実施したことがきっかけでした。
コロナ禍でオンラインイベント中心となったが、最近は現地開催のイベントを増やしているとのことです。
また、9年間毎月イベントは開催しているそうです（すごいですね！）。

PyLadies Tokyoは女性が一般のITコミュニティに参加する、最初のステップになればと思っているとのことです。
日本にはPyLadies TokyoだけでなくKyoto、Okinawaもあること、それらのメンバーが集うPyLadies JapanのSlackにはいろいろなチャンネルがって交流しているという話がありました。
また[PyLadies Caravan](http://tokyo.pyladies.com/caravan/)という各地域のPyLadiesとオフラインで交流するイベントも紹介されていました。

トークの後半では「自分たちの思い」として以下の3点が語られました。
コミュニティを継続的に運営するためには、どの点も大事だなと筆者も感じました。

* やり過ぎない→やりすぎると燃え尽きてしまう
* 主催者がやりたいことをやる
* 楽しむ→主催者自体がイベントを楽しむ

最後に、PyLadiesが将来的に不要になるとよいなと思っている、ということが語られました。
これは、女性エンジニアがコミュニティに参加するときに障壁を感じなくなるといいなということだと思います。
多くのエンジニアコミュニティが男女半々くらいの参加者になるといいなーと思いました。

```{admonition} 香港での発表を終えて（Maaya Ishida）
今回は全部のトークスクリプトを作成しました。
事前に会社の同僚に発表練習を見てもらい、内容や発音を確認してもらいました。
今回は技術寄りではなくコミュニティの話なので、伝え方が難しくうまく伝えてないと意味が通じないと思っていました。
そこで、単語のニュアンスがあっているか、難しい単語の場合は別の単語を調べたりしてスクリプトを調整しました。

発表は思ったよりたくさんの人が聞きに来てくれました。
また、発表が終わった後にたくさんの人に声をかけてもらえたのがうれしかったです。
この発表をきっかけに、香港をはじめ各国の女性エンジニアと会話ができてとてもよい経験になりました。
```

### Automate the Boring Stuff with Slackbot(ver.2) 

* トーク概要: <https://pycon.hk/2023/automate-the-boring-stuff-with-slackbotver-2/>
* スピーカー: Takanori Suzuki
* スライド: <https://slides.takanory.net/slides/20231111pyconhk/>

筆者の発表です。
「Automate the Boring Stuff with Slackbot (ver. 2)」と題して、Slack用にbotを作っていろいろいな作業を楽にしよう！というトークをしました。
発表時間が30分で前半をちょっとていねいにしゃべりすぎたようで少し時間が足りなかったです。
途中を少し飛ばしながら、なんとか最後は時間内に発表を終えることができました。

```{figure} images/takanory.jpg
:width: 600

筆者の発表の様子
```

質疑応答では以下のようなやりとりがありました。

* Q: ChatGPTとつなげられますか？
* A: ChatGPTのAPIがあるので、ここに書いてある例と同様につなげることは可能。ただし、SlackがオフィシャルでGPT対応などをすると思います
* Q: Slack SDKを使っていますか？
* A: Slackが提供する[Slack SDK](https://pypi.org/project/slack-sdk/)と[Bolt for Python](https://pypi.org/project/slack-bolt/)というSlackが提供するSlackアプリを作るためのフレームワークを使っています

### PyScript: Empowering Rich Python Applications in the Browser

* トーク概要: <https://pycon.hk/2023/pyscript-empowering-rich-python-applications-in-the-browser/>
* スピーカー: Sophia Yang

Anacondaに所属するSophia Yang氏による[PyScript](https://pyscript.net/)に関する発表です。
PyScriptはWebブラウザ上でPythonが実行できるフレームワークです。
PyCon US 2022にAnacondaのCEOであるPeter Wang氏によって発表されました。

```{figure} images/sophia.jpg
:width: 600

Sophia Yang氏
```

簡単なhello worldの書き方や、イベントハンドラーの指定方法など、基本的なPyScriptでのプログラムの書き方について説明がありました。
PyScriptを使うとWebブラウザ上でPythonが動作するので、PCにPythonをインストールする必要が無く、デプロイもHTMLを配置するだけで簡単だということがメリットとして語られました。
そのあとはデモとして、scikit-learnでのクラスタリング、スターウォーズの出演者の関係をd3.jsで表現、[Pyxel](https://github.com/kitao/pyxel)を使ったゲームといった例で、PyScriptでできることを伝えていました。
Pyxelが動くのは個人的にびっくりしました。

最後に<https://pyscript.com/>にサインアップしてPyScriptのコードを書いてほしいということと、[PyScriptのdiscord](https://discord.gg/HxvBtukrg2)に参加してほしいと伝えていました。

質疑応答では以下のようなやりとりがありました。

* Q: GPUは使えるか？
* A: 今は対応していない、難しい課題です
* Q: どのブラウザーに対応しているか？
* A: スマホブラウザーでも対応している。WebAssemblyに対応したブラウザーであれば対応しています

### Automating Victory: Beating browser games with accessible Python

* トーク概要: <https://pycon.hk/2023/automating-victory-beating-browser-games-with-accessible-python/>
* スピーカー: Jon Gaul

このトークはゲームをプログラムで自動的に解くというチャレンジについての発表です。
対象となるのは[マモノスイーパー](https://hojamaka.com/game/mamosui_list.html)というゲームで、マインスイーパーの拡張版といったゲームです。
Jon氏が言っていましたが上のレベルはまず解けないそうです。

```{figure} images/jon.jpg
:width: 600

Jon Gaul氏
```

このトークではどのようにマモノスイーパーをPythonで自動的に解くのか、そのステップが説明されました。
最初に[MSS](https://python-mss.readthedocs.io/index.html)というライブラリで画面のスクリーンショットを撮り、それを[OpenCV](https://opencv.org/)で画像処理をします。
画像処理したデータを元にマス目を認識し、各マス目をデータ化して計算し、安全なマスをクリックしていくということを繰り返します。
クリック処理には[PyAutoGUI](https://github.com/asweigart/pyautogui)を仕様したとのことです。

問題点としては、もしも画面の構成が変更されると、画面をデータ化する部分やクリックする処理がすべて書き直しとなります。
このあたりはWebスクレイピングにも通じるところがあると思いました。

ゲームを自動的に解くという試みはなかなか面白いなと思いました。
また、このあと実際に手でマモノスイーパーを解いてみましたが、なかなか面白い（そして難しい）という感想をJonさんに伝えました。

### クロージング

イベントの最後はクロージングです。再びSammy氏によりスポンサーやスピーカー、オーガナイザーへの感謝が述べられました。
参加者は最終的に**261名**だったそうで、参加者がかなり増えてよかったなと感じました。

```{figure} images/closing.jpg
:width: 600

参加者数は261名！！
```

PyCon HKのオーガナイザーとボランティアのみなさんにより、無事PyCon HKは終了しました。

```{figure} images/organizers.jpg
:width: 600

オーガナイザーとボランティアのみなさん
```

## Networking Hour

イベント終了後はNetworkng Hourということで、参加者を交えてパーティーがありました。
会場は[KAKI Izakaya](https://www.kakiizakaya.hk/)というお店です。
日本の居酒屋スタイル？のお店のようです。
確かに居酒屋っぽいメニューの枝豆、鶏の唐揚げ、たこ焼き、野菜の天ぷらなどが出てきました。
ただ、鶏の唐揚げにイクラを乗せるのは「日本の感覚じゃない」ということは伝えておきました。

```{figure} images/izakaya.jpg
:width: 600

居酒屋っぽいメニュー
```

パーティーではオーガナイザーであるSammy氏、Calvin氏や、香港から来ていたCheuk氏（彼女はPyCon APAC 2023にも来ていました）などいろいろな人と交流しました。
次はどこのPyCon で会えますかね〜？

```{figure} images/kaki1.jpg
:width: 600

居酒屋っぽいメニュー
```

```{figure} images/kaki2.jpg
:width: 600

居酒屋っぽいメニュー
```

パーティーのあとはCheuk氏やまーや氏などと一緒に[YARDLEYS CAFE・BISTRO・BARS](https://www.yardleybrothers.hk/visit-us)で二次会ビールを楽しみました。
香港島のめちゃくちゃ長いエスカレーターで坂道を登っていくのが面白かったです

## まとめ

PyCon Hong Kong 2023レポートは以上です。
初参加のPyCon Hong Kongは、新しい出会いもあり、これからの盛り上がりに期待できるイベントでした。
香港にはまた訪れたいなと思いました。

筆者がPyCon JP Associationとして行っているYouTubeライブ、[PyCon JP TV](https://tv.pycon.jp/)でも12月1日の回でPyCon Hong Kong 2023について紹介する予定です。
もしよかったらご視聴ください。

* TODO: youtube埋め込み

PyCon Hong Kongの前後は飛行機の都合で1日観光ができたので、香港の街を散歩したり、LEGO Storeに行ったり、ビールを飲んだり、フェリーに乗ったり、エッグタルトを食べたり、飲茶を食べたりしました。
Victoria Peakに行けなかったことが心残りです。

```{figure} images/hongkong.jpg
:width: 600

香港島側から半島側を望む
```

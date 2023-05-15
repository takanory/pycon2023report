# Day 2

カンファレンス2日目の様子をお伝えします。

## Python Steering Council Panel

* スピーカー: [Python Steering Council](https://us.pycon.org/2023/about/keynote-speakers/#python-steering-council)

Pythonは新機能をPEP（ペップ：Python Enhancement Proposal）というドキュメントで提案します。
その採用不採用を判断する中心となるのがSteering Councilで、毎年選挙によってメンバーが決定しています。

最初に[PEP 13 – Python Language Governance](https://peps.python.org/pep-0013/)によってSteering Councilという運営方法が決定しており、現在の5名のメンバーが紹介されました。
Emily Morehouse、Gregory P. Smith、Pablo Galindo Salgado、Thomas Wouters、Brett Cannonの5名で、それぞれ1年、2年、3年、4年、5年目のメンバーです（偶然だそうです）。

```{figure} images/council.jpg
:width: 600

Python Steering Councilメンバー
```

次にPython 3.12の新機能について説明がありました。新機能については[What's New In Python 3.12](https://docs.python.org/3.12/whatsnew/3.12.html)のページで確認できます。
以下が主要な新機能として紹介されました。

* Better f-strings：引用符をネストできるようになった
* サブインタープリターごとのオプションGIL
* 型パラメーターを指定する構文の改善
* エラーメッセージの改善
* distutilsの削除
* 古いunittestのメソッドの削除
* 文字列リテラルでエスケープシーケンスが無効な場合の警告

細かい改善や古い機能の削除が主ですが、サブインタープリターごとのオプションGILが導入されることにより、パフォーマンスにどのような影響が出るのかも気になります。

## PSF Community Lunch

ランチタイムは、通常のランチではなく**PSF Community Lunch**に参加しました。
このランチは、PSF（Python Software Foundation）の報告をランチを食べながら聞くというものです。
参加者は各国のコミュニティを運営しているメンバーや、PSFのボードメンバーなどが多く参加していたという印象です。

```{figure} images/psf-lunch.jpg
:width: 600

PSF Community Lunch
```

PSFの財務状況としては、2020年にパンデミックでPyConを急遽中止になった年は落ち込んでいましたが、その後は順調に回復しているようです。
また、PSFから他の地域への助成金の割合としては、アジア、アフリカがかなり低い割合ということがわかりました。
「アジア・アフリカにもっと助成金を配分すべきではないか」という意見がアジアのメンバーからあげられていました。

## PyScript and the magic of Python in the Browser

* スピーカー: Fabio Pliger

この日のトークからはPyScript関連の発表を紹介します。
PyScriptはWebブラウザ上でPythonが動作する仕組みで、詳細については筆者がgihyo.jpで記事に書きました。

* [WebブラウザでPythonが動作する！PyScriptの詳解 | gihyo.jp](https://gihyo.jp/article/2023/04/monthly-python-2304)

このトークではまず[pyscript.com](https://pyscript.com/)というサイトが紹介されました。
このWebサイトは、エディターが表示されてそこでPyScriptのコードを書いて実行するという、PyScript用のIDE（統合開発環境）を提供するサービスです。
ここで作成したコードをシェアする機能などもあるようです。
興味のある方はユーザー登録してみてください。

他にPyScriptで書かれた[PyperCard](https://pyscript.github.io/pypercard/)（[GitHub](https://github.com/pyscript/pypercard)）というプロダクトが紹介されました。
これはMacの昔あったソフトウェア[HyperCard](https://ja.wikipedia.org/wiki/HyperCard)に着想を得た、PythonのGUIフレームワークです。
使い道はすぐには思いつかないですが面白い試みだなと思っています。

今後の予定としてはVisual PyScriptというGUIでプログラムを書くようなものを作成中だそうです。現在はalphaバージョンとのこと。
他にはpyscript.comで質問に答えてくれるPyScript Assistantというものも提供していくそうです。
Anaconda社を中心に、PyScript関連の開発が幅広く進んでいるなという印象をうけました。

トークの後半では、PyScriptがFFI（[Foreign function interface](https://ja.wikipedia.org/wiki/Foreign_function_interface)）をサポートしている実例として、LEGOのロボットをPyScriptから操作する例をデモしていました。
Webブラウザで動いているPyScriptから、そのPCに接続しているインタフェース経由でLEGOに命令を送っているんでしょうかね？
なにがどうなっていのるかよくわかりませんが、すごいなと感じました。

```{figure} images/pyscript-lego.jpg
:width: 600

PyScriptからLEGOを動かすデモ
```

````{admonition} PyCon JP TVインタビュー

このコラムは寺田 学([@terapyon](https://twitter.com/terapyon))がお届けします。

イベント中に撮影しYouTubeに公開した「PyCon US 2023レポート動画」について紹介します。

現地の雰囲気を知ってもらおうと思い、スポンサーブースなどが設置されているホールを中心に動画を撮影してきました。
公開した動画は、コミュニティ関係者のインタビュー編、スポンサーブース担当者へのインタビュー編、ポスターセッション・ジョブフェアの紹介編に加え、会場全体の雰囲気を紹介するおまけ編の 4 本です。

コミュニティ関係者へのインタビューは、PyCon USのカンファレンスチェアーやPSF担当者、APAC地域のカンファレンス主催者といったコミュニティ関連の方々からメッセージを頂きました。またスポンサーブースの担当者には計9社の方々からメッセージを頂きました。

```{figure} column-images/pyconjptv-interview-pyladies.jpg
:width: 600

PyLadiesブースのインタビューの様子
```

動画のリンクは以下のとおりです。

- [コミュニティ関係者のインタビュー編](https://youtu.be/KGfO8YTvWYs)
- [スポンサーブース担当者編](https://youtu.be/0G0EZWwDZCs)
- [ポスターセッション・ジョブフェアの紹介編](https://youtu.be/BMf6OrbfOOQ)
- [おまけ編](https://youtu.be/QTXT8MF9P8M)

この動画は、毎月Live放送している[PyCon JP TV](https://tv.pycon.jp)の活動の一環として取りまとめました。
また、[2023年5月12日のLive放送](https://www.youtube.com/live/7-UjyXNriwk)で、撮影時のエピソードも交えながらお届けしました。ご覧になっていただくとPyCon USの雰囲気がより分かるかと思います。
````

## ライトニングトーク

カンファレンス2日目の最後もライトニングトークです。
韓国コミュニティのKwonHan（[@darjeelingt](https://twitter.com/darjeelingt)）氏がPyCon Koreaの歴史や、立ち上げる前のことなどを語っていました。
ときどきクスっとする所もありつつ、PyCon Koreaの立ち上げに向けての熱い気持ちが感じられるトークでした。

```{figure} images/kwonhan.jpg
:width: 600

KwonHan氏
```

他には、[pyOpenSci](https://www.pyopensci.org/)のというオープンソースとオープンサイエンスに関するチームの紹介、
[Afro Python](https://afropython.org/)という黒人系のPythonコミュニティの紹介、オープンソースのプロジェクトに参加してもらうために気をつける点の紹介などがされていました。
  
## PyLadies Auction

この日の夜は[PyLadies Auction](https://us.pycon.org/2023/events/pyladies-auction/)に参加しました。
このイベントはチャリティーオークションで、スポンサー企業などが提供したアイテムを参加者が競り合います。
そして、落札した金額はそのままPyLadiesの活動資金として寄付されます。

```{figure} images/items.jpg
:width: 400

Microsoft提供のキーボードと、PostgreSQL提供の編みぐるみ
```

筆者や周りの知り合いもなんとかオークションに参加しようとしますが、あっという間に金額が跳ね上がるため、全く落札できません。
ただ、オークションの競り合いを見ているだけでもとても面白く、PyCon USでイチオシのイベントと言えます。

オークションでは結構悪ふざけしているアイテムもあり、この写真にははTimTamの4種セットが写っていますです。
このセットはDjangoやBeeWareの開発者でもあるRussell Keith-Magee（[@freakboy3742](https://twitter.com/freakboy3742)）氏がオーストラリアから持ってきたものだそうです。
とはいえ、[TimTam](https://ja.wikipedia.org/wiki/%E3%83%86%E3%82%A3%E3%83%A0%E3%82%BF%E3%83%A0)なんて別にアメリカでも売っているはずで、そのお菓子に100ドル以上の価格がついて落札されていました。
それを見て「来年は日本から抹茶のキットカットを持っていくとウケるかも」といった話を日本メンバーでしていました。

```{figure} images/auction.jpg
:width: 600

オークションの様子
```

他にもオークション後半ではアイテムを見せるカメラにたまたま映り込んだボールペンに対して、会場中から「ペン（を売れ）！！」という声がかかり、急遽ペンのオークションが始まりました。
単なるボールペンが300ドルくらいで落札するのは、ここくらいじゃないでしょうか…

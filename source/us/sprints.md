# スプリント

このレポートの最後にスプリントの様子をお届けします。
スプリントは開発イベントで、Python関連のオープンソースプロジェクトのコントリビューター（貢献者）が集まって開発を行います。
また、初心者がプロジェクトに参加する機会でもあります。
PyCon US 2023のスプリントは4月24日(月)〜27日(木)までの4日間開催されました。
筆者は移動の関係でスプリント1日目の昼過ぎまでしか参加できませんでしたが、それでもいくつか出会いがあったので紹介したいと思います。
スプリントについて詳細はPyCon USの以下のページを参照してください。

* [Development Sprints - PyCon US 2023](https://us.pycon.org/2023/events/sprints/)

## どんなプロジェクトがあるか

スプリント期間中はボードに「どの部屋でどのプロジェクトが開発をしているか」が書き出してあります。
参加者はこのボードを見て興味のある部屋を訪れたり、フリースペースで自分の開発を進めたりできます。

ボードを見てみると、以下のようなプロジェクトが参加していることがわかります。

* [BeeWare](https://beeware.org/)、[django-simple-deploy](https://django-simple-deploy.readthedocs.io/en/latest/)、[PyScript](https://pyscript.net/)、[Strawberry GraphQL](https://strawberry.rocks/)、[Pydantic](https://pydantic.dev/)、[GNU Mailman](https://www.gnu.org/software/mailman/)、[Hypothesis](https://hypothesis.readthedocs.io/en/latest/)、[Ruff](https://beta.ruff.rs/docs/)、[mypy](https://mypy.readthedocs.io/en/stable/)、[CircuitPython](https://circuitpython.org/)

みなさんが知っているオープンソースのプロジェクトもあると思います。
興味のあるプロジェクトはありますか？
また、当然ですが[CPython](https://github.com/python/cpython)のスプリントもあります。

```{figure} images/sprints.jpg
:width: 400

スプリントのボード
```

## PyScriptのスプリントに参加

筆者はPyScriptのスプリントに参加しました。
短い時間ではありますが[PyScriptのGitHub](https://github.com/pyscript/pyscript)を参照し、対応出来そうなissueがないかを確認しました。
対応しやすいissueには `good first issue` というラベルが付いているんで、それを見るといいよという説明を受けました。

* [PyScriptのgood first issue](https://github.com/pyscript/pyscript/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22)

この前にgihyo.jpで[PyScriptの記事](https://gihyo.jp/article/2023/04/monthly-python-2304)を書いたときに、`pyodide_http`の使い方についてドキュメントの間違いを見つけていました。
このスプリントでその対応をしようと思っていましたが、すでに対応済みでした（まだリリースはされてなさそうですが）。

* [The novice tutorial reports no patch() attribute · Issue #1291 · pyscript/pyscript](https://github.com/pyscript/pyscript/issues/1291)
* [Add tests for snippets in docs by FabioRosado · Pull Request #1264 · pyscript/pyscript](https://github.com/pyscript/pyscript/pull/1264)

他のissueを見てみましたが、ちょっと短時間では対応できそうな感じのものがなかったため、残念ながらissueの中身を確認するだけで終わってしまいました。

スプリントに参加したときに最初に説明をしてくれたFabio Pliger氏ですが、名札を見てみると「Creator of PyScript」と書いてあります。
Fabio氏はPyScriptの作者であり、カンファレンス2日目に筆者もトークを聞きました。
そこで「PyScriptについて日本語で記事を書いたんですよ」と、さきほどの記事を本人に紹介しました。
Fabio氏からは「PyScriptを広める活動をしてくれてありがとう」と感謝をされました。
記事を書いておくことによって、この記事が名刺代わりになってよかったなと思いました。
あとで英語に翻訳したURLを本人にも共有しておきました。
チラ見してくれているとよいのですが。

```{figure} images/with-fabio.jpg
:width: 400

PyScriptの作者のFabio氏と
```

時間になったので他のスプリント参加者に「移動なのでこれで失礼します。」とあいさつをし、記念撮影をしました。
参加者の一人から「今度、大阪に行くので連絡先を教えて」と言われたので、連絡先を交換しました。
連絡があったら大阪周辺のおすすめのお店情報を、大阪の人の知恵を借りて伝えたいと思います。

```{figure} images/sprinters.jpg
:width: 400

PyScriptのスプリント参加者
```

荷物をスタッフの本部で預かってもらっていたので、ピックアップしに行きました。
そこに[PSFスタッフ](https://www.python.org/psf/records/staff/)のLorenさんやEeさんがいたので、最後にお別れのあいさつをしてPyCon USの会場をあとにしました。

## まとめ

「PyCon US 2023」のレポートは以上です。
2019年から4年ぶりに参加したPyCon USは、活気にあふれており、またAPACメンバーの結束もより強まって参加してよかったなと感じました。

筆者がPyCon JP Associationとして行っているYouTubeライブ、PyCon JP TVでもPyCon US 2023について紹介しています。
一緒に参加した寺田さんの目線からの感想もあるので、ぜひご覧になってください。

<iframe width="560" height="315" src="https://www.youtube.com/embed/7-UjyXNriwk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

また、レポート動画も別途まとめているので、そちらを見てみると現地の雰囲気がより伝わると思います。

* [PyCon JP Blog: PyCon US 2023のレポート動画公開](https://pyconjp.blogspot.com/2023/05/pycon-us-2023-report-video.html)

オフィシャルの発表動画はPyCon USのYouTubeチャンネルで公開されると思います。
以下のページで確認してください。

* [PyCon US - YouTube](https://www.youtube.com/channel/UCMjMBMGt0WJQLeluw6qNJuA)

PyCon US 2023のあと、筆者はカリフォルニア州のサンディエゴに移動しました。
そして、カリフォルニアのいくつかのブルワリーでクラフトビールを飲みつつ、[LEGOLAND California](https://www.legoland.com/california/)と[Disneyland Park](https://disneyland.disney.go.com/)（主にスターウォーズ）に遊びに行きました。
San Diego→Carlsbad→Anaheim→Los Angelesと移動が激しくハードな旅でしたが、こちらもとても楽しい体験でした。
旅の様子はTogetterにもまとめたので、興味のある方は見てみてください。

* [LEGOLAND CaliforniaからのDisneyland Californiaエクストリームツアー - Togetter](https://togetter.com/li/2135239)

```{figure} images/with-trooper.jpg
:width: 400

First Order stormtrooperと記念撮影
```

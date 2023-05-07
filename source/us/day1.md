# Day 1

## 朝ご飯

* ブリトー

## Opening

* Conference Chairのマリエッタさんからのあいさつ
* 20年の過去を振り返る動画
* Thank you
  * 参加者、スタッフ、ボランティアへの感謝
  * スポンサーへの感謝
  * 発表者
  * 参加者は2,000名くらい
* First time here?
  * 2015にはじめて参加した。参加費のサポートがあった。自分も人生を変えた
  * 女性がたくさん発表していた
  * それから自分も発表できた
* Pythonのコアデベロッパーとなった
* キーノートスピーカーの紹介
* スペシャルゲスト(Council、Guido, D&I, Dev)
* Expo Hallの説明
* 89のトークはすべてライブストリームする
* Quiet room: PC作業もしちゃだめ
* 字幕がついている
* Hallway track: packman role
* PyLadies Auction
* Open Spaces
* Mobile App
* マスクは必須。つけてなかったら3回スキャンしたらアウトになる
* PyCon USの間にやってポイントを稼いでねって感じらしい

### Metaのスポンサートーク

* Pythonへの感謝を述べた

## Keynote: Ned Batchelder

* 2007が初参加。そのときのGuidoのトークはPython 3.0
* edXについて
* 人はterrible
* 標準がない、ドキュメントがない、予測できない
* 状態が隠れている
* 線形じゃない、明確じゃないエラーメッセージ
* 人はファンタスティック
* 人のAPIユーザーズガイド
  * 自分の経験に基づいている
* Information + Sentiment
* Defaulted sentiment
* 対策
  * Noって言わない?
  * 言葉が足りない
  
  
## Inside CPython 3.11's new specializing, adaptive interpreter.

* Brandt Bucher
* スライドの日付が間違っているのを指摘されて、その場で直すハプニング
* 6年前からPythonを使い始めた。今はMSのCPython Fasterチーム
* バイトコードがどう変わったか
  * `dis.sid()` で adaptive=Trueを付けると培地コードが変わる
  * `LOAD_ATTR_INSTANCE_VALUE` 前に読んだときと乾いてなければ速く動く
  * `BINARY_OP_ADD_FLOAT`
* `show_cashes=True` でキャッシュの状況が見れる
* `specialist --blue`
  * https://github.com/brandtbucher/specialist

```python
y = dy + self.py
cls = type(self)
```

* CPython 3.12でバイトコードが変わる
  * 3.12でスペしアライズされたバイトコードが増えた
  * キャッシュが減る
* [PEP 659 – Specializing Adaptive Interpreter | peps.python.org](https://peps.python.org/pep-0659/)

## Build Yourself a PyScript

* Nicholas H.Tollervey, Paul Everitt
* お互いを自己紹介
* pyscriptの基本的な書き方を説明
* pyscript.jsを見せながら、どうなっているかを説明
* MicroPythonでPyScriptを動かす?
* なんか字幕との掛け合いが始まる。おもしろい
* emscripten
 * https://pypercard.readthedocs.io/en/latest/

```{admonition} PyCon APACブース
このコラムは吉田([@koedoyoshida](https://twitter.com/koedoyoshida))がお届けします。

今回はPyCon APACブースをPyCon USで初出展しました。
PyCon APAC自体は2010年からAPAC地域で持ち回りで開催している
国際的なPyConイベントとなりますが、イベント自体は各国のPyConのオーガナイザーが
開催しているため、いままではあまり共同ではアピールはしてきませんでした。
今回ブース出展することも有り、共通ロゴやAPAC共通のWebサイト[PyCon APAC Organizers](https://pycon.asia/)を作成しました。

また、APACをアピールできる配布物や出展物を各自持ち寄りました。
PyCon JPからは日本らしく紅白の折り紙でAPACで開催される主要なPyConの紹介とwebサイトを紹介する折り紙など準備し持ち込みました。

この折り紙は鶴型に折ることが出来るようになっていて、APACの出展メンバーや
ブース訪問の参加者の方にAPACの紹介を兼ねてそのまま渡したり、英語での折り方ガイド
をみせつつ、一緒に鶴を折ってそれを持ち帰ってもらったり出来、非常に好評でした。

また、PyCon US開催に合わせて[PyCon APAC 2023 CFP(Call for proposal)サイト](https://pretalx.com/pyconapac2023/cfp)をオープン出来ましたので、そのアピール用の資料等も現地で作成、印刷し配布できました。
APAC地域やそれ以外の国の方含めブースに良く訪問があり、PyCon USに出展してアピールできた事は
とても良かったと思います。

![PyCon APACブースの様子](column-images-booth/boothimageall2.jpg "ブース出展の様子")

```

## Open Space

* [Python Bytes Podcast](https://pythonbytes.fm/)の公開収録を見学

## LT

* tox 4の更新情報
  * アウトプットがカラフルになった
  * Python 2.7 drop
* Sourcery
  * https://sourcery.ai/
* Zen of Pythonのはなし

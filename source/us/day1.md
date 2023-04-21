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

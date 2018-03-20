---
title: "obit"
date: 2018-03-18T16:00:00+09:00
---

プロセスが終わったことを標準出力に出力するツール。

<!--more-->

# 紹介

## ウィンドウやプロセスの終了を待つ

コマンドライン引数にウィンドウタイトルやプロセス名を指定することで、対象のプロセスが終了したことを標準出力に出力します。

既に立ち上がっているウィンドウ名を指定して、そのウィンドウを出しているアプリケーションの終了を待つ…ということができます。


## 終了時に標準出力にウィンドウやプロセスの情報を出力する

例えば、メモ帳が起動している状態で、以下のコマンドを実行します。

```
> obit メモ
(待機状態になる)
```

この状態で obit はメモ帳の終了を待機します。

メモ帳を終了すると、obit は標準出力に終了したウィンドウやプロセスの情報を出力します。

```
> obit
無題 - メモ帳(notepad.exe)
```

出力したものを通知アプリ等に渡せば、手元で終了がわかったり、ログに残したりすることができます。

監視対象がなくなれば obit も終了します。
ですので、obit の実行後になにか処理を書いておけば（バッチファイル等）、監視対象の終了直後の処理を後付けできることになります。


## 対象にポップアップウィンドウが出た際に情報を出力する

コマンドラインオプション ```--popup``` を指定すれば、そのウィンドウがなにか画面をポップアップさせた場合に通知を受け取れます。

例えば、処理の終了をメッセージボックスに表示するようなアプリケーションに対しては、この機能が使えます。
この場合、そのアプリケーションが終了しなくても obit は標準出力に出力します。

```
> obit --popup あるアプリタイトル
```

# 使い方

上でほとんど使い方は紹介してしまいました。

```--popup``` を指定する場合はウィンドウのタイトルを指定します。
それ以外の場合（プロセスの終了を待つ）は、ウィンドウのタイトルもしくはプロセス名を指定します。

詳細な使い方については、```obit help``` を参照してください。

# ダウンロード

Windows のみの配布です。

* [obit_windows_amd64_0.3.1.zip](https://github.com/ShuheiKubota/ShuheiKubota.github.io/releases/download/site/obit_windows_amd64_0.3.1.zip)
* [obit_windows_386_0.3.1.zip](https://github.com/ShuheiKubota/ShuheiKubota.github.io/releases/download/site/obit_windows_386_0.3.1.zip)

* [obit_windows_amd64.zip](https://github.com/ShuheiKubota/ShuheiKubota.github.io/releases/download/site/obit_windows_amd64.zip)
* [obit_windows_386.zip](https://github.com/ShuheiKubota/ShuheiKubota.github.io/releases/download/site/obit_windows_386.zip)

# 更新履歴

* 0.3.1 (2018-03-21)
    * 内部的な変更。複数の対象を並列で監視する仕組みを若干変更。
    * 現時点では、念の為に過去のバージョンも残しています。

* 0.3.0 (2018-03-18)
    * 公開～諸々
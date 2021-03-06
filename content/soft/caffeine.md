---
title: "caffeine"
date: 2019-10-19T23:00:39+09:00
---

起動中に Windows のスリープを抑止する。

<!--more-->

# 紹介

裏で実行しているプロセスがありスリープさせたくない場合、このアプリを起動しておくとスリープを抑止できます。

大抵の PC では、マウスやキーボードの操作がない場合にスリープする設定になっています。
このアプリを起動しておくと、いざ作業をする段になってスリープしているということを避けることができます。

* せっかくリモート接続したが、接続先に人がいないので、再接続ができない
* スリープするとネットワークも切断されるため、スリープしたくない
* 再度ログインするのが面倒
* ファイルをダウンロードしている間に Nintendo Switch で遊ぼう

# 使い方

## 実行

管理者として実行します。
これは、スリープ制御をするために必要です。

実行ファイル `caffeine.exe` を右クリックして「管理者として実行」を選択します。

実行するとコンソール画面が表示されますが、これはそのままにしておきます。
最小化しておくと良いしょう。

## 終了

終了時は、起動時に表示されたコンソール画面で `Ctrl+C` を押します。

## ショートカット作成機能

実行ファイルを `caffeine` の実行ファイルに D&D することで、
ショートカットファイルが作成されます。

このショートカット経由で起動したアプリが終了するまではスリープしません。

ただし、例によって、管理者として実行する必要があります。
ショートカットのプロパティで、詳細設定にある「管理者として実行」にチェックを入れると便利です。

# ダウンロード

[ダウンロード](https://github.com/shu-go/caffeine/releases)

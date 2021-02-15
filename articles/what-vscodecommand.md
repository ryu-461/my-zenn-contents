---
title: "VSCode使いなら使いたいCodeコマンド"
emoji: "🌊"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["vscode","windows","mac"]
published: false
---

# はじめに

ターミナルでファイルを操作するときにファイル VSCode で直接開きたい場面があります。
そこで VSCode を起動してフォルダを開くで開きますが、それだと少し手間がかかってしまいます。

VSCode が用意している `Code コマンド`を使うことでターミナルから直接 VSCode を開けるため紹介します。

# Codeコマンドとは

VSCode には code コマンドと呼ばれるコマンドが存在します。このコマンドを使うことでターミナルから直接 VSCode を起動したり、指定したファイル、ディレクトリを瞬間的に開けるようになります。

# Codeコマンドの準備【Windows】

VSCode をインストールすることで自動的にパスが通りコマンドプロンプトから使用可能になります。WSL2 を使うときに特に効果を発揮します。

# Code コマンドの準備【MacOS】

Mac の場合は少し手数を踏む必要があります。
VSCode を開き、`⌘ + ⇑ + p` でコマンドパレットを表示します。

コマンドパレットに `shell command` と打ち込むことで以下のような選択が表示されます。

![コマンドパレットを開いた様子](https://storage.googleapis.com/zenn-user-upload/g6g74ukk33yndvsz0siedopguxrm)
*シェルコマンド : PATH内にcodeコマンドをインストールしますを選択*

管理者特権でコマンドをインストールするのを許可する必要があるため OK を選択します。
![ダイアログが表示される様子](https://storage.googleapis.com/zenn-user-upload/kuoa8f1u9ok94qdg5hytbhhbyd3c)

コマンドのインストールが完了すると右下にメッセージが表示されます。これでパスが通って Code コマンドがターミナル上で使用可能になりました。

ターミナルを開いて code と打ってみましょう。VSCode が起動するはずです。

```shell
$ code
```
これで Code コマンドのインストール、使用準備は終了です。

Code コマンドは VSCode Stable 版、Insiders 版ともに使用可能です。2 つのビルドは共存できるため、コマンドも共存可能となります。

VSCode Insiders のコマンドは以下のようになります。
```shell
$ code-insiders
```
使うにはそれぞれのビルドでコマンドパレットからコマンドインストールの手順を踏む必要があります。
コマンドが独立していることで使いたい VSCode を選ぶことができるのは便利です。

# コマンド使用例

# よく使いそうなコマンド

code コマンドでできることをまとめる。以下 Stable 版で実行。

## VSCodeを起動

```shell
$ code
```

## VSCodeでディレクトリを開く

```shell
$ code .
```
開きたいディレクトリへ移動して以下のコマンドを実行します。

## VSCodeでファイルを開く

```shell
$ code hoge.txt
```

## VSCodeでファイルを比較する

```shell
$ code -d hoge1.txt hoge2.txt
```

## ヘルプを表示

```shell
$ code -h
```
使えるコマンドが一覧で表示されます。
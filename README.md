# vagrant-isucon/isucon7-final

## Overview

isucon7本戦とほぼ同じ環境を構築するためのVagrantfileです。

## Usage

- vagrant実行環境を用意する
- このリポジトリ内のVagrantfileを手元に用意する
  - 必要に応じてVagrantfileを編集する
- Vagrantfileがあるディレクトリで`vagrant up`を実行する
  - ベンチマーク用サーバ(bench)と参加者用サーバ(image) x3 が起動
- Ansibleによるプロビジョニングが完了したら`vagrant ssh`を実行する
  - vagrant ssh bench
  - vagrant ssh image-0
  - vagrant ssh image-1
  - vagrant ssh image-2
- ベンチマークを実行する
  - sudo -i -u isucon
  - cd cco/bench
  - ./bench -remotes (imageサーバのIPアドレス)

## 動作確認

macOS + VirtualBox 6.1.12 + Vagrant 2.2.9で動作確認済です。
VMWare Desktopでも動作するかもしれませんが未確認です。

# QA4you_lecture

## はじめに
これは東北大学の量子アニーリングワークショップ [**Quantum annealing for you**](https://altema.is.tohoku.ac.jp/QA4U/index.html#section2) の**非公式な**リポジトリです. ここでは, 講義に利用したコードを動くdocker環境を提供することを目的としています. 

## 準備

gitは使えるものとします. 

### 全OS共通
- [dockerの公式サイト](https://www.docker.com)に行って, PCに**Docker Desktop**をインストールする
  - **Docker Desktop**とは, 各々のOS上でDokcer環境を使えるよういい感じにやってくれるソフトです. 
  - WIndows以外の人は. インストールは各自のOSにしたがってよしなにやってください. **Windowsの人は, インストール前に次節を読んでください**
- スペックによっては少し時間がかかるので, 紅茶を飲みながらゆっくり待つ

### OS別の作業
Windowsユーザーの方だけ少しだけ分岐が生じます. 

#### Windowsの人
- インストール時に"Install required Windows components for WSL 2" と "Add shortcut to desktop
" にチェックを入れてインストールを行う. 
- インストール時に"WSL 2 installation is incomplete." というダイアログが出たら, 消さずに以下の手順を実行してください. 
  - Linux カーネル更新プログラム パッケージをダウンロードする必要があります. [ここ](https://docs.microsoft.com/ja-jp/windows/wsl/install-win10#step-4---download-the-linux-kernel-update-package)を参照して「x64 マシン用 WSL2 Linux カーネル更新プログラム パッケージ」をダウンロードし, 指示に従ってインストールを行う. 
- PowerShellを起動する

## 使い方

### コンテナを利用してjupyterを立ち上げる

#### コンテナの起動
- 起動コマンド ```docker-compose up -d```
  - ```docker-compose up --build -d``` のように ```--build``` オプションをつけるとイメージのビルドからやり直せる
    - Dockerfileを編集したあとはイメージのビルドを再度行わないと, 変更がコンテナに反映されない. 
    -  ビルドからやり直すので(初回ほどではないとはいえ)ちょっと時間がかかる
  - 設定に手を加えていない場合はを```http://localhost:8888から```ブラウザでjupyterLabが起動する
  - ここまで来たらあとは通常のjupyterの使い方と同じです. Enjoy!

#### コンテナの停止
- 停止コマンド ```docker-compose stop```
  - コンテナを停止する
- コンテナを破棄したい ```docker-compose down```
  - Dockerfileを編集した後などは一旦破棄するとよい

## 参照
- dockerに関する詳しい説明は[公式ドキュメント](https://docs.docker.com)を参照してください. 
  - 英語の苦手な人はがんばれ
  - 兎にも角にも, 英語が読めないとえらい苦労を強いられます. 「英語を学ぶ意味とは」と悩んでいる高校生の君へ. こういうときのために英語を学ぶのです. 

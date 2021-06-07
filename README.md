# QA4you_lecture

## はじめに
これは東北大学の量子アニーリングワークショップ [**Quantum annealing for you**](https://altema.is.tohoku.ac.jp/QA4U/index.html#section2) の**非公式な**リポジトリです. ここでは, 講義に利用したコードを動くdocker環境を提供することを目的としています. 

## 使い方

gitは使えるものとします. 

### 全OS共通
- [dockerの公式サイト](https://www.docker.com)に行って, PCにdockerをインストールする
  - 各自のOSにしたがってよしなにやってください. 
- スペックによっては少し時間がかかるので, 紅茶を飲みながらゆっくり待つ

#### コンテナの起動
- 起動コマンド ```docker-compose up -d```
  - ```docker-compose up --build -d``` のように ```--build``` オプションをつけるとイメージのビルドからやり直せる
    - Dockerfileを編集したあとはイメージのビルドを再度行わないと, 変更がコンテナに反映されない. 
    -  ビルドからやり直すので(初回ほどではないとはいえ)ちょっと時間がかかる
  - 設定に手を加えていない場合はを[http://localhost:8888]()からブラウザでjupyterLabが起動する
  - ここまで来たらあとは通常のjupyterの使い方と同じです. Enjoy!

#### コンテナの停止
- 停止コマンド ```docker-compose stop```
  - コンテナを停止する
- コンテナを破棄したい ```docker-compose down```
  - Dockerfileを編集した後などは一旦破棄するとよい

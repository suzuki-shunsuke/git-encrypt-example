# git-encrypt-example

gitで一部のファイルを暗号化してバージョン管理したい

## 参考

* http://qiita.com/ikeisuke/items/d7ee904d23745c758a7d
* https://gist.github.com/shadowhand/873637
* https://git-scm.com/book/ja/v2/Git-%E3%81%AE%E3%82%AB%E3%82%B9%E3%82%BF%E3%83%9E%E3%82%A4%E3%82%BA-Git-%E3%81%AE%E5%B1%9E%E6%80%A7
* https://github.com/AGWA/git-crypt -> GPG使って暗号化している。若干面倒な気もする

## 手順

1. .gitattributes作成
2. git config 設定
3. 3種類のスクリプト作成
4. パスフレーズを設定


## TODO: 自動化コマンドラインツール

イメージを書く

### Install

* コマンドの作成
* 場合によってはグローバル設定

### Usage

#### 初期設定

```
# git config 設定
# > パスフレーズを聞かれる
# パスフレーズの設定
$ git enc init
```

#### 暗号化されるファイルの追加

```
# .gitattributes設定
# initされていなかったらエラー
$ git enc <file-path>
```

#### 明示的に復号化

```
# configなどを設定する前にcheckoutしてきた暗号化されたままのファイルを復号化する
$ git enc
```

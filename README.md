# プロジェクト名(ここに直接記入)

write by kanno kennta
（誰が書いたか残しましょう）

※続けるためにあまりにも細かく書きすぎない
※他のツールなどで分かる情報はわざわざ書かないように

## 重要

**公開日まで見れないよう必ず時限設定を行ってください**

index.phpに以下を記述してプロジェクト直下に置いてください。

```php
<?php
date_default_timezone_set('Asia/Tokyo');

$date = strtotime(date('Y-m-d H:i'));

if (isset($_GET['dateck'])) {
    $date = strtotime($_GET['dateck']);
}

if ($date < strtotime('2023-1-13 10:00')){
    header('Location: https://hogehoge');
}

include_once('./index.html');
```


（案件特有の確認すべきことなどあれば記入してください、意図して一番上にしています）
想定される例
- ブランチルール
- 特殊な納品方法
- 

## test

https://hogehoge/

## node

v10.16.3
（ここに記入する以外に.node-versionファイルも作成、push推奨）


## php

v0.0.0

## 環境構築

（中途入社社員が大まかに把握できるくらいには書きましょう。）

npm インストール

```shell
yarn
```

.ymlファイルのあるディレクトリで実行してください

```shell
docker compose up -d
```

## ビルド方法

開発`src`下で行います、`sutatic`に置いたものはbuildされません。
buildしたものは`dist`下にはき出されます。

```shell
yarn dev
```
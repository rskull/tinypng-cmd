# tinypng ver 1.0

    PNG画像圧縮サービス[tinypng](https://tinypng.com/) さんの[API](https://tinypng.com/developers) をコマンドで直感的に叩けるようにしました！
    複数ファイルあるときはコレを使うと早いです。

## 事前準備

まず[ここから](https://tinypng.com/developers) デベロッパー登録し、API keyを取得する必要があります。
メールアドレスを入力するだけで簡単に登録できます！
なお無料版は月500リクエストまでだそうです。

## インストール

```shell
$ git clone https://github.com/rskull/tinypng-cmd.git

# tinypngを開き、取得したAPI keyを
# key='YOUR_API_KEY' の部分に入力してください。

$ sudo cp tinypng-cmd/tinypng /bin/
$ sudo chmod 755 /bin/tinypng # 実行権限を与えます
$ rm -rf tinypng # 不要なら削除します
```

## 使い方

```shell
$ tinypng [オプション(省略可)] [圧縮する画像] [出力先(省略可)]
```

色々な指定方法
```shell
$ tinypng target.png # 圧縮して上書き
$ tinypng target.png output.png # 名前をつけて保存
$ tinypng target.png outpt_dir/ # 保存先を指定
```

複数の画像をまとめて圧縮したいとき(-aオブション)
```shell
$ tinypng -a ./ # 指定フォルダにある全てのpngファイルを圧縮
```

圧縮対象の画像を一覧で確認(-cオブション)
```shell
$ tinypng -c ./
```

## オプション

| オプション     | 説明                                      |
|:---------------|:------------------------------------------|
| -a [--all]     | 指定先の全画像を圧縮                      |
| -c [--check]   | 対象画像を一覧で確認                      |



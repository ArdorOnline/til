# gitconfig

## ユーザ設定
```
$ git config --global user.name "My Name"
$ git config --global user.email myname@example.com
```


## 改行コード変換
```
$ git config --global core.autocrlf input
```

|設定|チェックアウト時|コミット時|
|:---|:---|:---|
|true|LF -> CRLF|CRLF -> LF|
|input|変換しない|CRLF -> LF|
|false|変換しない|変換しない|


## カラー出力の有効化
```
$ git config --global color.ui auto
```

## Github SSH設定
```
[url "github:"]
	InsteadOf = https://github.com/
	InsteadOf = git@github.com:
```

## 確認コマンド
確認は以下のコマンド
```
$ git config --global --list
```

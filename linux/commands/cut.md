# cut

テキストファイルから一部を選択表示する

## 書式

```
cut オプション [ファイル名...]
```

## オプション

|オプション|説明|
|:--|:--|
|-b 範囲<br> --byte=範囲|範囲に指定したバイト数だけ表示。タグとバックスペースは1バイトとして扱う|
|-c 範囲<br> --characters=範囲|範囲に指定した文字数だけ表示|
|-f 範囲<br> --fields=範囲|範囲に指定したフィールド数だけ表示。フィールドはデフォルトはタブで区切られている|
|-d 区切り文字<br> --delimiter=区切り文字|-f オプションを利用する時の区切り文字を指定。デフォルトはタブ|
|-s <br> --pnly-delimited|フィールドの区切りが無い行を無視|

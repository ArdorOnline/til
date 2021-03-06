# grep

指定したファイル、もしくは標準入力からの入力を読み込み、与えられたパターンにマッチした行を出力します。

## 書式

```
grep [オプション] [パターン][ファイル名...]
```

## オプション

|オプション|説明|
|:--|:--|
|-A<br>--after-context=行数|パターンにマッチした行の後ろ、指定行数分を出力|
|-e<br>--regexp=パターン|パターンを指定|
|-f<br>--file=ファイル名|指定したファイルからパターンを読み取る|
|-B<br>--before-context=行数|パターンにマッチした行の前、指定行数分を出力|
|-C<br>--context=行数|パターンにマッチした行の前後の指定行数分を出力。デフォルトは2行|
|-c<br>--count|マッチした行番号だけを出力|
|--color, --colour|出力に色を付ける(色は環境変数GREP_COLORに依存)|
|-i, --ignore-case|大文字と小文字を区別しない|
|-n, --line-number|出力行頭に入力ファイルでの行番号を表示|
|-m, --max-count=行数|指定した行数がマッチしたところで読み込みを止める|
|-R, -r<br> --recursive|ディレクトリの下も再帰的に読み込み|
|-v<br> --invert-match|マッチしなかった行を出力|
|-E<br> --extended-regrexp|拡張正規表現を利用|
|--exclude=パターン|指定したパターンにマッチするものは読み込まない|
|--exclude-file=ファイル名|ファイルに記述されたパターンにマッチするファイルは読み込まない|
|-F<br> --fixed-strings|パターンを改行で区切られた固定文字列リストとして扱い、マッチするか調べる|
|-Z|圧縮ファイルを検索前に一度解凍する|
|-P<br> 00perl-regexp|Perlの正規表現としてパターンを解析|

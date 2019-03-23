# vimrc

## 'encoding' 'enc'
```
set encoding=utf-8
```
'encoding' オプションに使用したいエンコーディングを設定します。  
これは、バッファ (編集中のファイル) のテキスト、レジスタ、Vim script ファイル、などに使われます。

## 'fileencodings' 'fencs'
```
set fileencodings=iso-2022-jp,uc-jp,sjis,cp932,utf-8
```
値は、既存のファイルの編集を開始するときに考慮される文字エンコーディングのリストである。  
ファイルが読み込まれると、Vimは指定されたうちの先頭の文字エンコーディングを使おうとする。  
そのときエラーが発見されると、値のリスト内で次に並んでいるエンコーディングが試される。  
あるエンコーディングでうまくいくとわかると、'fileencoding' がそれに設定される。  
すべてのエンコーディングが失敗すると 'fileencoding' は空文字列に設定され、'encoding' の値が使われることになる。  

## 'fileformats' 'ffs' 
```
set fileformats=unix,dos,mac
```
想定される改行 (<EOL>) の種類を指定する。  
これは新しいバッファの編集を始めたときと、ファイルを既存のバッファに読み込んだときに使われる。

## 'backup' 'bk' 'nobackup' 'nobk'
```
set nobackup
```
ファイルを上書きする前にバックアップを作る。

##  'writebackup' 'wb' 'nowritebackup' 'nowb'
```
set nowritebackup
```
ファイルの上書きの前にバックアップを作る。  
オプション 'backup' がオンでない限り、バックアップは上書きに成功した後削除される。


## 'swapfile' 'swf' 'noswapfile' 'noswf'
```
set noswapfile
```
バッファでスワップファイルを使用する。  
このオプションは、特定のバッファでスワップファイルを使いたくないときにはオフに設定できる。

## 'number' 'nu'
```
set number
```
毎行の前に行番号を表示する。  
オプション 'cpoptions' にフラグ 'n' が含まれていないときは、折り返された行の先頭は行番号の表示される桁に入り込まない。


## 'numberwidth' 'nuw'
```
set numberwidth=4
```
行番号を表示するのに使われる桁数の最小値。  
'number' か 'relativenumber'がオンのときか行番号付きで印刷するときのみ意味がある。  
常に番号とテキストの間にスペースが1つ置かれるので、番号そのものに割かれる桁数はこれより1文字少なくなる。

## 'backspace' 'bs'
```
set backspace=indent,eol,start
```
挿入モードで <BS> を使って削除できる文字を指定しています。  
コンマで区切られた三つの部分はそれぞれ次の文字の削除を許可しています。  


|オプション|説明|
|:-----------|:------------|
|indent|行頭の空白|
|eol|改行|
|start|挿入モード開始位置より手前の文字|

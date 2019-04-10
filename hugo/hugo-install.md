# Hugo install

## for windows

1. フォルダ作成（ex: C:/Hugo)
1. binフォルダ作成 （ex: C:/Hugo/bin)
1. Hugo をダウンロード [Releases · gohugoio/hugo · GitHub ](https://github.com/gohugoio/hugo/releases)
1. hugo_x.xx.x_Windows-64bit.zip を解凍し、/binへコピーする
1. パスを通す（ex: C:/Hugo/bin)

## サイト作成

### サイト作成コマンド
```
$ hugo new site quickstart
```
以下が出力される
```
Congratulations! Your new Hugo site is created in D:\Dropbox\Hugo\quickstart.

Just a few more steps and you're ready to go:

1. Download a theme into the same-named folder.
   Choose a theme from https://themes.gohugo.io/, or
   create your own with the "hugo new theme <THEMENAME>" command.
2. Perhaps you want to add some content. You can add single files
   with "hugo new <SECTIONNAME>\<FILENAME>.<FORMAT>".
3. Start the built-in live server via "hugo server".

Visit https://gohugo.io/ for quickstart guide and full documentation.
```

### テーマを取得
```
$ cd ./quickstart
$ git clone https://github.com/budparr/gohugo-theme-ananke.git themes/ananke
```

テーマ一覧は以下。  
https://themes.gohugo.io/


### 記事の作成
```
$ hugo new posts/my-first-post.md
```

### サーバー起動
```
$ hugo server -D
```
テーマを適用して起動
```
$ hugo server -t ananke -w -D
```

ブラウザから http://localhost:1313/ へアクセス

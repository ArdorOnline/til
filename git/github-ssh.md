# Github SSH設定

## 公開鍵・秘密鍵を作成
鍵を保存するディレクトリへ移動して、鍵を作成する。

```
$ cd ~/.ssh
$ ssh-keygen -t rsa

Generating public/private rsa key pair.
Enter file in which to save the key (/home/ardor/.ssh/id_rsa): id_github_rsa ☆ここでファイル名を入力
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
```

## 作成した公開鍵を設定
https://github.com/settings/keys

1. New SSH key をクリック
1. Title を入力
1. Key を入力
1. Add key をクリック

### 鍵のコピー方法
```
For Mac
$ pbcopy < ~/.ssh/id_github_rsa.pub
```

```
For Windows
$ clip < ~/.ssh/id_github_rsa.pub
```

## 接続の確認方法
```
$ ssh -T git@github.com

Hi (account name)! You've successfully authenticated, but GitHub does not provide shell access.
```

## ssh config 設定
```:~/.ssh/config
Host github github.com
    HostName github.com
    IdentityFile ~/.ssh/id_github_rsa
    User git
```

## gitconfig 設定
```:~/.gitconfig
[url "github:"]
	InsteadOf = https://github.com/
	InsteadOf = git@github.com:
```

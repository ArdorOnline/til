# Setup User

|コマンド|説明|
|:----|:---|
|useradd|ユーザーを追加|
|passwd|パスワード設定|
|usermod|ユーザーの変更|

## ユーザー追加
'useradd  new_user'  
ユーザーを追加する。

## ユーザーパスワード
'passwd new_user'  
ユーザーのパスワードを設定する。

## ユーザー権限
'usermod -G wheel new_user'

### グループ確認
'grouups new_user'  

'getent group wheel'  


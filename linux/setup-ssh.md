# Setup SSH

## Version 確認
```
ssh -V
```

## sshd_config について

|プロパティ|設定値|説明|
|:--|:--|:--|
|Port|22|ポート番号|
|PermitRootLogin|yes/no|rootでのログイン可否|
|PasswordAuthentication|yes/no|パスワード認証可否|
|PermitEmptyPasswords|yes/no|空パスワード可否|

### PermitRootLogin設定値
|設定値|説明|
|:--|:--|
|yes|rootでのログイン許可|
|no|rootでのログイン不可|
|without-password|rootのパスワード認証不可|
|forced-commands-only|rootユーザの直接ログインを拒否するが、root権限を使うコマンドのアクセスは許可|

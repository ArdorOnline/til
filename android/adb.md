# adb commands

## 端末の照会

`adb devices`

```
adb devices
List of devices attached
emulator-5554  device
emulator-5556  device
emulator-5558  device
```

## 特定の端末へのコマンドの送信

`adb -s serial_number command`

```
adb -s emulator-5556 install sample.apk
```

## 端末への / 端末からのファイルのコピー

`adb pull remote local`

`adb push local remote`



## adb コマンド リファレンス


|カテゴリ|コマンド|説明|
|:-----------|:------------|:------------|
|ターゲット端末|-d|接続されている USB 端末のみに adb コマンドを送信します。|
|ターゲット端末|-e|実行中のエミュレータ インスタンスのみに adb コマンドを送信します。|
|ターゲット端末|-s serial_number|adb によって割り当てられたシリアル番号（「emulator-5556」など）で参照される特定のエミュレータ / 端末インスタンスに adb コマンドを送信します。|
|全般|devices|接続されているすべてのエミュレータ / 端末インスタンスのリストを出力します。|
|全般|help|サポートされる adb コマンドのリストを出力します。|
|全般|version|adb のバージョン番号を出力します。|


### activity manager（am）の呼び出し

`adb shell am start -a android.intent.action.VIEW`

#### インテントの引数の仕様

|オプション|説明|
|:-----------|:------------|
|-a action|"android.intent.action.VIEW" などのインテント アクションを指定します。これは一度だけ宣言できます。|
|-d data_uri|"content://contacts/people/1" などのインテント データ URI を指定します。これは一度だけ宣言できます。|
|-t mime_type|"image/png" などのインテント MIME タイプを指定します。これは一度だけ宣言できます。|
|-c category|"android.intent.category.APP_CONTACTS" などのインテント カテゴリを指定します。|
|-n component|"com.example.app/.ExampleActivity" など、明示的なインテントを作成するためにパッケージ名の接頭辞が付いたコンポーネント名を指定します。|
|-f flags|setFlags() でサポートされているように、フラグをインテントに追加します。|
|--esn extra_key|null エクストラを追加します。URI インテントに対して、このオプションはサポートされていません。|
|-e｜--es extra_key extra_string_value|string 型データをキーと値のペアとして追加します。|
|--ez extra_key extra_boolean_value|boolean 型データをキーと値のペアとして追加します。|
|--ei extra_key extra_int_value|integer 型データをキーと値のペアとして追加します。|
|--el extra_key extra_long_value|long 型データをキーと値のペアとして追加します。|
|--ef extra_key extra_float_value|float 型データをキーと値のペアとして追加します。|
|--eu extra_key extra_uri_value|URI データをキーと値のペアとして追加します。|
|--ecn extra_key extra_component_name_value|変換されて ComponentName オブジェクトとして渡されるコンポーネント名を追加します。|
|--eia extra_key extra_int_value[,extra_int_value...]|integer 型データの配列を追加します。|
|--ela extra_key extra_long_value[,extra_long_value...]|long 型データの配列を追加します。|
|--efa extra_key extra_float_value[,extra_float_value...]|float 型データの配列を追加します。|



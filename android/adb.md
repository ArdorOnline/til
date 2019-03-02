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

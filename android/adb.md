# adb commands

# 端末の照会

`adb devices`

```
adb devices
List of devices attached
emulator-5554  device
emulator-5556  device
emulator-5558  device
```

# 特定の端末へのコマンドの送信

`adb -s serial_number command`

```
adb -s emulator-5556 install sample.apk
```

# Setup Network

## サービス

|コマンド|説明|
|:---|:---|
|service network start|ネットワークサービス起動|
|service network stop|ネットワークサービス停止|
|service network restart|ネットワークサービス再起動|
|service network status|ネットワークサービス確認|


## ネットワーク設定

/etc/sysconfig/network-scripts/ifcfg-eth0
|プロパティ|説明|設定例|
|:---|:---|:---|
|DEVICE|デバイス名|DEVICE=eth0|
|HWADDR|MACアドレス|HWADDR=00:00:00:00:00:00|
|TYPE|インタフェースのデバイスタイプ|TYPE=Ethernet|
|UUID|Universally Unique Identifier|UUID=XXXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX|
|ONBOOT|システム起動時に有効とするか|ONBOOT=yes|
|BOOTPROTO|IP取得方法 固定IP:static、DHCP:dhcp|BOOTPROTO=dhcp|
|IPADDR|IPアドレス|IPADDR=192.168.1.1|
|NETMASK|ネットマスク|NETMASK=255.255.255.0|
|GATEWAY|デフォルトゲートウェイ|GATEWAY=192.168.1.1|
|NETADDR|ネットワークアドレス。通常IPアドレスとネットマスクより自動判断|NETADDR=192.168.1.0|

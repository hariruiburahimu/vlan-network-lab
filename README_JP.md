# VLANネットワークラボ

🇬🇧 English version → [README.md](README.md)

## 概要

このラボでは、Cisco Packet Tracer を使用してレイヤー2スイッチでの基本的な VLAN 設定を実演します。

VLAN を使用してネットワークを分割し、異なるブロードキャストドメインを作成します。

同じ VLAN 内のデバイスは通信できますが、異なる VLAN 間ではルーティングがない限り通信できません。

## トポロジー

Cisco 2960 スイッチ ×1  
PC ×4  

PC0 と PC1 は VLAN 10 に割り当てられます。  
PC2 と PC3 は VLAN 20 に割り当てられます。

## ネットワーク設計

VLAN 10 – SALES  
ネットワーク: 192.168.10.0/24

VLAN 20 – IT  
ネットワーク: 192.168.20.0/24

## 使用機器

- Cisco 2960 スイッチ
- PC ×4

## PC設定

PC0  
IPアドレス: 192.168.10.10  
サブネットマスク: 255.255.255.0  

PC1  
IPアドレス: 192.168.10.11  
サブネットマスク: 255.255.255.0  

PC2  
IPアドレス: 192.168.20.10  
サブネットマスク: 255.255.255.0  

PC3  
IPアドレス: 192.168.20.11  
サブネットマスク: 255.255.255.0  

（このラボではデフォルトゲートウェイは必要ありません。）

## スイッチVLAN設定
enable
configure terminal

vlan 10
name SALES
exit

vlan 20
name IT
exit

interface range fastEthernet0/1-2
switchport mode access
switchport access vlan 10
exit

interface range fastEthernet0/3-4
switchport mode access
switchport access vlan 20
exit

## 動作確認

同じ VLAN の通信
ping 192.168.10.11
Reply from 192.168.10.11
異なる VLAN の通信
ping 192.168.20.10
Request timed out

## 結果

同じ VLAN 内では通信が可能です。

異なる VLAN 間では、ルーターなどのレイヤー3デバイスがない限り通信できません。

これは VLAN によるネットワーク分離を示しています。

## スクリーンショット

![Network Screenshot](topology_ping_test.png)

## ラボファイル

Packet Tracer ラボファイルのダウンロード:

[vlan-network-lab.pkt](vlan-network-lab.pkt)

Cisco Packet Tracer 8.x で動作確認済み

## ライセンス

Apache License 2.0

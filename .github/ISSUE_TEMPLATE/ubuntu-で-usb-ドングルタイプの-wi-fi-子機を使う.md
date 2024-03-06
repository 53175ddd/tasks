---
name: Ubuntu で USB ドングルタイプの Wi-Fi 子機を使う
about: ELECOM WDC-150SU2M
title: ''
labels: ''
assignees: ''

---

- [ ] 下記コマンド実行
```
sudo apt update && sudo apt upgrade -y
sudo apt install wireless-tools network-manager
```
- [ ] コンフィグを確認
```
iwconfig
```
以下のような出力が得られた場合，`wlx04ab18fd70b5` をメモっておく
```
lo        no wireless extensions.

wlo1      IEEE 802.11  ESSID:"Ruckus-Wireless-R500"  
          Mode:Managed  Frequency:5.58 GHz  Access Point: F0:3E:90:24:5A:3C   
          Bit Rate=433.3 Mb/s   Tx-Power=22 dBm   
          Retry short limit:7   RTS thr:off   Fragment thr:off
          Power Management:on
          Link Quality=53/70  Signal level=-57 dBm  
          Rx invalid nwid:0  Rx invalid crypt:0  Rx invalid frag:0
          Tx excessive retries:0  Invalid misc:157   Missed beacon:0

wlx04ab18fd70b5  IEEE 802.11  ESSID:off/any  
          Mode:Managed  Access Point: Not-Associated   Tx-Power=20 dBm   
          Retry short limit:7   RTS thr=2347 B   Fragment thr:off
          Power Management:off
```
- [ ] 構成ファイルを作成
```
sudo nano /etc/netplan/50-cloud-init.yaml
```
```
network:
    wifis:
        wlx04ab18fd70b5:
            addresses: []
            dhcp4: true
            optional: true
            access-points:
                {SSID}:
                    password: "{PASSWORD}"
   version: 2
    renderer: NetworkManager
```
- [ ] Netplan への反映
```
sudo netplan apply
```
- [ ] 確認
```
ifconfig
```

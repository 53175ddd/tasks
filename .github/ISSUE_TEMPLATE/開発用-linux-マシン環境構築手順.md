---
name: 開発用 Linux マシン環境構築手順
about: Linux ノートのセットアップ
title: ''
labels: ''
assignees: 53175ddd

---

- [ ] Chrome の導入
  - <https://uepon.hatenadiary.com/entry/2023/08/18/010431>
- [ ] Discord の導入
- [ ] Discord PTB の導入
  - <https://discord.com/download>
- [ ] Slack の導入
- [ ] VSCode の導入
- [ ] OBS の導入
  - <https://obsproject.com/ja/download>

```
sudo apt update && sudo apt upgrade -y
sudo snap install discord code slack -y
sudo apt install ffmpeg
sudo add-apt-repository ppa:obsproject/obs-studio 
sudo apt install obs-studio -y
```

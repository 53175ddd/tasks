---
name: RasPico with Rust on Ubuntu
about: Ubuntu 上で RasPico のプログラミングを Rust で行える環境をセットアップする手順
title: ''
labels: ''
assignees: 53175ddd

---

- [ ] おまじない
```
sudo apt udpate && sudo apt upgrade -y
```
- [ ] Rust のインストール
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source "$HOME/.cargo/env"
```
- [ ] クロスコンパイラのインストール
```
rustup target add thumbv6m-none-eabi
```
- [ ] 諸々のツールのインストール
```
sudo apt install gcc pkg-config libudev-dev -y
```
- [ ] 環境変数の設定
```
cd
sudo nano .bashrc
```
```
export ACLOCAL_PATH=/usr/local/share/aclocal/:$ACLOCAL_PATH
export PKG_CONFIG_PATH=/usr/lib/pkgconfig
```
- [ ] 再起動
- [ ] ユーティリティのインストール
```
cargo install flip-link elf2uf2-rs probe-run
cargo install probe-rs --feature cli
```
- [ ] OpenSSL のインストール
```
sudo apt install libssl-dev
```
- [ ] cargo-generate のインストール
```
cargo install cargo-generate
```

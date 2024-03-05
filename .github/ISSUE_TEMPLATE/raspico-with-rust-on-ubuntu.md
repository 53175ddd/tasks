---
name: RasPico with Rust on Ubuntu
about: Ubuntu 上で RasPico のプログラミングを Rust で行える環境をセットアップする手順
title: ''
labels: ''
assignees: ''

---

- [ ] Rust のインストール
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source "$HOME/.cargo/env"
```
- [ ] クロスコンパイラのインストール
```
rustup target add thumbv6m-none-eabi
```
- [ ] ユーティリティのインストール
```
cargo install flip-link elf2uf2-rs probe-run
```

---
name: Windows 11 導入後のタスク
about: 操作系を 10 に戻す・いつもの環境のセットアップ
title: ''
labels: ''
assignees: 53175ddd

---

# アプリケーション等のインストール

- [ ] Google 日本語入力の導入
  - <https://www.google.co.jp/ime/>
- [ ] Microsoft IME のリストラ
  - 「設定」 -> 「時刻と言語」 -> 「言語」 -> 「優先する言語」 -> 「日本語 [オプション]」 -> 「キーボード」
- [ ] Ctrl + Space を使うように設定
  - <https://kurobutasan.com/google-ime-ctrl-space/>
- [ ] winget の導入（オプション）
  - <https://aka.ms/getwinget>
  - Terminal で `Add-AppxPackage -Path .\Microsoft.DesktopAppInstaller_hogehoge.msixbundle`
  - `winget -v`
- [ ] Google Chrome の導入
  - `winget install --id Google.Chrome --force`
- [ ] デフォルトブラウザを Chrome に設定
  - 「設定」 -> 「アプリ」 -> 「規定のアプリ」 -> 「Web ブラウザー」
- [ ] Honeyview の導入
  - <https://honeyview.jp.download.it/download>
- [ ] VLC Media Player の導入
  - <https://www.videolan.org/vlc/download-windows.ja.html>
- [ ] ExplorerPatcher の導入
  - <https://github.com/valinet/ExplorerPatcher/releases>
- [ ] Tailscale インストール
  - [ ] ログイン
- [ ] Discord
- [ ] Synology Drive Client
- [ ] Clipboard Remote  // 要らんかもしれん

# 設定変更

- システム
  - 通知
    - [ ] 要らん通知を全部無効にする
    - [ ] 「追加の設定 / Windows を最大限に活用し、このデバイスの設定を完了する方法を提案する」を無効にする
    - [ ] 「Windows を使用する際のヒントや提案を入手する」を無効にする
  - 電源
    - [ ] 「電源モード」を適切なものに変更する
    - 画面、スリープ、休止状態のタイムアウト
      - [ ] 「後で画面をオフにする」を「なし」にする
      - [ ] 「次の時間の経過後にデバイスを休止状態にする」を「なし」に
    - 電源とスリープボタンコントロール
      - [ ] 「電源ボタンを押すと、PC が」>「何も行わない」
      - [ ] 「スリープボタンを押すと、PC が」>「何も行わない」
- 個人用設定
  - 背景
    - [ ] 「背景をカスタマイズ」を「画像」に
  - 色
    - [ ] 「モードを選ぶ」を「ダーク」に
    - [ ] 「透明効果」を「オフ」に
  - ロック画面
    - [ ] 「ロック画面を個人用に設定」を「画像」に
    - [ ] 「ロック画面にトリビアやヒントなどの情報を表示する」をオフに
    - [ ] 「ロック画面の状態」を「なし」に
  - タスクバー
    - タスクバー項目
      - [ ] 「検索」を「非表示」または「検索ボックス」に
      - [ ] 「タスクビュー」を無効に
      - [ ] 「ウィジェット」を無効に
      - [ ] 「再開」を無効に
    - タスクバーの動作
      - [ ] 「タスクバーの配置」を「左揃え」に
      - [ ] 「タスクバーを自動的に隠す」を無効に


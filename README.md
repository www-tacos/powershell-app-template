# Powershell App Template

PowerShellをバッチから実行するアプリのテンプレート


## 使い方

- 以下のような方法で処理を記述する
  - src配下のmain.ps1に処理を直接記述する
  - src配下に処理を記述したシェルスクリプトを配置し、main.ps1から呼び出す

- アイコンファイル（.ico）をimg配下に配置し、main.lnkに設定する

- lib配下にスクリプトモジュールを配置し、main.ps1やその他スクリプトから読み込む

## 実行方法

main.lnk をダブルクリックで実行する


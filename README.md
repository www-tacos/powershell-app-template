# Powershell App Template

## 概要
- PowerShellをバッチから実行するアプリのテンプレート

- ディレクトリごとコピーしてmain.ps1を適当に編集する


## 構成
- main.lnk
  - src/main.batへのショートカット
  - 実行ファイルに任意のアイコンを設定するためだけのショートカット

- src/main.bat
  - src/main.ps1を呼び出すためのバッチファイル
  - ps1実行時のカレントディレクトリを設定する役割もある

- src/main.ps1
  - 処理の本体

- src/debug.bat
  - src/main.ps1をテスト用に呼び出すためのバッチファイル
  - コンソールを表示して、スクリプト終了後もコンソールを閉じない


## Tips
- main.batで `-WindowStyle Hidden` オプションを付けてmain.ps1を実行しているためコンソールは表示されない
  - `Write-Host` や `Read-Host` など標準入出力を使いたい場合はオプションを外す

- main.lnkへのアイコン設定は絶対パスでの指定なので参照先アイコンの移動時やアプリ配布時にアイコンが無効になってしまう点に注意
  - Windows標準のアイコンを使う方が無難（[参考](https://4thsight.xyz/13325)）
  - 例） `%SystemRoot%\System32\imageres.dll`



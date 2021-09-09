# Powershell App Template

- PowerShellをバッチから実行するアプリのテンプレート

- main.lnkをクリックで実行するとsrc配下のmain.ps1が実行されるのでmain.ps1に処理を記述する

- main.batに`-WindowStyle Hidden`オプションを付けているためコンソールは表示されない。コンソール上の入出力を使いたい場合（Write-Host, Read-Host, Write-Progress等を用いたい場合）はオプションを外す。

- main.lnkにアイコンを設定することもできるが絶対パスなので、参照先アイコンの移動時やアプリ配布時にアイコンが無効になってしまう点に注意



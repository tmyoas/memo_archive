WSL調べたことメモ
---
# 背景
* Win10で直接ubuntuが叩けるようになった = virtualboxとかいらない
* ファイルの更新にはWinの高機能なエディタ使いたい
* そのためにubuntu on WSLとwinのディレクトリ対応関係が知りたい = 調べてみた

# 結果
`/` = `C:\Users\<UserName>\AppData\Local\Packages\CanonicalGroupLimited.UbuntuonWindows_79rhkp1fndgsc\LocalState\rootfs\`
解読してみると
`/` = `C:\Users\<UserName>\AppData\Local\Packages\CanonicalGroupLimited.UbuntuonWindows_<ランダム英数字13桁>\LocalState\rootfs\`

# 疑問
* linux側とWin側で権限の不一致とか起きない?
  * 試してみる
  * 簡単なテストでは大丈夫そう
* ランダム英数字の意味は?
  * 実は複数台建てられる可能性?
* win側で作ったファイルの権限はどう見える?
  * 000になった

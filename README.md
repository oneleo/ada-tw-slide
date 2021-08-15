# Welcome to [ada.tw](https://www.facebook.com/groups/ada.tw)
Cardano ADA 臺灣研究社

## A Cardano Group in Taiwan
本社團以創建 Cardano ADA Ouroboros PoS 臺灣礦池為目標，歡迎大家來討論！

- Cardano ADA 臺灣研究社臉書社團：[https://www.facebook.com/groups/ada.tw](https://www.facebook.com/groups/ada.tw)
- 什麼是 Cardano？Cardano 介紹影片：[https://youtu.be/cn3WxIFmO14](https://youtu.be/cn3WxIFmO14)
- 影片內的介紹簡報在此：[https://go-talks.appspot.com/github.com/oneleo/CardanoPresent/CardanoIntroduction-20180809.slide](https://go-talks.appspot.com/github.com/oneleo/CardanoPresent/CardanoIntroduction-20180809.slide)

## 建置 Cardano 礦池相關原創文章

1. [2018/08/09 Cardano 區塊鏈的基本介紹](https://go-talks.appspot.com/github.com/oneleo/ada-tw-slide/s20180809-intro.slide)

## 要如何保存並在本機瀏覽這裡的簡報？
- 這裡的簡報均是用 Go 語言的 [present](https://pkg.go.dev/golang.org/x/tools/present) 專案製作，以下在 Windows 作業系統中編譯
	1. 在「Windows 符號」上按下【滑鼠右鍵】→【Windows PowerShell（系統管理員）（A）】，執行以下指令
	2. 安裝 Windows APP 管理工具 [chocolatey](https://chocolatey.org/)
		```powershell
		Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
		```
	3. 安裝 chocolateygui 圖形介面、golang 語言環境、git.install 版本控管工具
		```powershell
		"$Env:ProgramData\chocolatey\bin\choco.exe" install -y chocolateygui golang git.install --params "/NoShellIntegration"
		```
	4. 下載並編譯 present
		```powershell
		"$Env:ProgramFiles\Git\cmd\git.exe" clone "https://github.com/oneleo/ada-tw-slide.git" "$Env:USERPROFILE\go\src\github.com\oneleo\ada-tw-slide"
		"$Env:ProgramFiles\Git\cmd\git.exe" clone "https://github.com/golang/tools.git" "$Env:USERPROFILE\go\src\golang.org\x\tools"
		"$Env:ProgramFiles\Go\bin\go.exe" get -u "golang.org/x/tools/cmd/present"
		cd /d "$Env:USERPROFILE\go\src\github.com\oneleo\ada-tw-slide"
		"$Env:USERPROFILE\go\bin\present.exe" -base "$Env:USERPROFILE\go\src\golang.org\x\tools\cmd\present" -notes
		```

	5. 使用瀏覽器開啟 [http://127.0.0.1:3999](http://127.0.0.1:3999) 連結以觀看簡報

## LICENSE
- [Apache License 2.0](https://github.com/oneleo/ada.tw/blob/main/LICENSE)
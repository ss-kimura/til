# エディタの設定変更
**Ctrl + Shift + p**で窓を出して設定キーワードを検索し、選択すれば設定できる  
例えば、窓に\>breadcrumsと打つと、View: Toggle Breadcrumbsなどが表示されるので、選択すればよい

# Cheatsheet
- **! + Tab** or **! + Enter**でHTML5のテンプレート文が表示される(**html:5 + Enter**でもいい)
- **div#app + Enter**で<div id="app"></div>

# WSL(Windows Subsystem for Linux)をいれる  
1. 管理者モードでPowerShellを起動し以下のコマンドを実行 
```C:\Windows\System32> Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux```  

2. 再起動後、ストアからWSLをいれる

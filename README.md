# 知行账本安装包

这个仓库只发布 Windows x64 安装包和更新清单 `latest.json`。这里没有程序源码，也没有任何人的账本。

源码不在这个仓库。安装包里是已经构建好的程序，装到电脑后可以看到程序文件；这只表示没有把源码仓库和账本公开。

GitHub 自动附带的 Source code 压缩包只包含本仓库里的说明，不是程序源码。

## 下载

安装包文件名是 `zhixing-ledger-setup-<版本>-win-x64.exe`。GitHub 会去掉附件名里的中文，所以不用中文文件名。

最新的公开版本：

https://github.com/ychyc07/zhixing-ledger-releases/releases/latest

应用内更新读取：

https://github.com/ychyc07/zhixing-ledger-releases/releases/latest/download/latest.json

清单里的 `sha256` 是安装包的校验和。请在安装前核对。

## 安装

- 安装包没有代码签名。Windows SmartScreen 可能提示未知发布者。不要为了安装去关闭系统的安全提示。
- 1.2.0 和更早的已安装版本不会自动知道这个地址，需要手动安装一次 1.2.1。之后的安装版在「软件更新」里检查、下载并核对，只有输入确认文字后才会安装。
- 安装前程序会把账本复制到 `%APPDATA%\知行账本\backups`。账本仍留在 `%APPDATA%\知行账本`。卸载不删除这份数据。
- 本仓库不使用 GitHub Actions、Git LFS 或 GitHub Packages，也没有绑定付款方式。

## 发布顺序

每个正式版本有两个附件：安装包 exe，然后是 `latest.json`。两个文件都上传之后，才把 Release 从草稿改为公开，避免清单先指向一个还不存在的安装包。

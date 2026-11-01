# SK 浏览器

基于 Chromium 的定制浏览器，自带 Flash 支持，可连接自建服务器同步书签、密码和扩展。

**两个平台**：Windows x64、Linux x86_64（Deepin / Debian 系）。

## 下载

到 [Releases](../../releases) 页面下载最新版。两个平台用同一个版本号，看文件名区分：

| 文件 | 说明 |
| --- | --- |
| `SK-Browser-<版本>-Setup.exe` | Windows 安装版，双击安装，可选安装位置 |
| `SK-Browser-<版本>-Portable.zip` | Windows 免安装版，解压即用 |
| `SK-Browser-<版本>-linux-amd64-deepin.deb` | Linux 安装包（Deepin / Debian 系 x86_64） |
| `sk-server-<版本>-x64.fpk` | 自建同步服务端（飞牛 fnOS 应用包） |

## Linux 安装

```bash
sudo dpkg -i SK-Browser-1.20261101.102-linux-amd64-deepin.deb
sudo apt -f install     # 若提示缺依赖
sudo dpkg -r sk-browser # 卸载
```

## 简单说明

- 内核 Chromium 156，两个平台同一版本
- Windows 与 Linux 共用一条版本号，Linux 只多 `-linux-amd64-<发行版>` 后缀
- Windows 的 Flash 由内置的独立宿主进程提供，不需要另外装老插件
- Linux 的 Flash 由内置 Ruffle 提供，默认启用；AS1/AS2 基本正常，AS3 部分可用，DRM 与本地文件读写不支持
- Linux 版安装、卸载前会先结束正在运行的旧版本，避免装完点图标看到的还是旧界面
- 安装包没有做代码签名，Windows 首次运行系统可能拦一下，选「仍要运行」即可
- 自建服务端跑在 NAS 或任意常开的机器上，用来代替厂商服务器存账号和同步数据
- GitHub 不接受中文文件名（会被替换成点号），所以 release 里用的是英文名，下载后改回中文名不影响使用

## 其它

- 官网：本地站点，暂未上线
- 服务端部署与升级：见 release 说明

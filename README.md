# 叛逆汉堡大王-桌面宠物

叛逆汉堡大王是一个基于 Electron 的桌面电子宠物。它内置粉色零食主题 chibi 宠物精灵图，不依赖 Codex App，下载后即可运行。当前提供 Windows x64 便携 EXE、macOS universal 未签名测试包和 Linux/UOS/Deepin deb 安装包。

![叛逆汉堡大王动画预览](media/rebellious-burger-king-animation-preview.gif)

## 下载 Windows EXE

普通用户请到 GitHub Releases 下载最新版本：

- [最新版本 Releases](https://github.com/SakuraTearDuDu/rebellious-burger-king-desktop-pet/releases/latest)
- 直接运行版：`RebelliousBurgerKing-DesktopPet.exe`
- 中文文件名压缩包：`RebelliousBurgerKing-DesktopPet-v2.0-win-x64.zip`

Windows 版程序未做代码签名，首次运行时 Windows SmartScreen 可能提示风险，这是未签名个人项目的常见提示。

说明：GitHub Release 对中文附件文件名的下载链接兼容性不好，所以直接下载的 EXE 使用英文文件名。它和本地的 `叛逆汉堡大王-桌面宠物.exe` 是同一个程序；如果希望得到中文文件名，请下载 ZIP，解压后里面就是 `叛逆汉堡大王-桌面宠物.exe`。

## macOS 测试包

macOS 版用于小范围测试。普通用户请到 GitHub Releases 下载：

- DMG 安装包：`RebelliousBurgerKing-DesktopPet-v2.0-mac-universal.dmg`
- `.app` 压缩包：`RebelliousBurgerKing-DesktopPet-v2.0-mac-universal.zip`

说明：macOS 的 `.app` 本质上是一个目录包，GitHub Release 不能像普通单文件那样直接上传裸 `.app`。如果需要 `.app`，请下载 ZIP，解压后里面就是可点击运行的 `叛逆汉堡大王-桌面宠物.app`。

macOS 测试包未做 Apple Developer ID 签名和公证。首次打开时，如果系统提示无法验证开发者，可以右键点击 `.app` 选择“打开”，或到“系统设置 > 隐私与安全性”里允许打开。

## Linux / UOS / Deepin

普通用户请到 GitHub Releases 下载对应架构的 deb 安装包：

- x64：`RebelliousBurgerKing-DesktopPet-v2.0-linux-amd64.deb`
- ARM64：`RebelliousBurgerKing-DesktopPet-v2.0-linux-arm64.deb`

## 第一次运行

1. 下载 `RebelliousBurgerKing-DesktopPet.exe`，或下载 ZIP 后解压出 `叛逆汉堡大王-桌面宠物.exe`。
2. 双击 EXE 运行。
3. 如果 Windows 出现“Windows 已保护你的电脑”：
   - 点击“更多信息”。
   - 点击“仍要运行”。
4. 运行后桌面上会出现叛逆汉堡大王，任务栏里不会出现普通窗口，主要通过桌面宠物本体和系统托盘控制。

程序是便携版，不需要安装，也不会要求用户手动复制 `pet.json` 或 `spritesheet.webp`。

macOS 测试版可打开 DMG 后运行或拖入 Applications；ZIP 版解压后运行 `.app` 即可。

## 基本操作

- 单击叛逆汉堡大王：挥手。
- 双击或连续三击叛逆汉堡大王：跳跃。
- 按住叛逆汉堡大王拖动：移动位置，移动时会播放跑步动作。
- 5 分钟没有鼠标互动后，叛逆汉堡大王会进入难过动画；再次鼠标互动会恢复。
- 右键叛逆汉堡大王：打开快捷菜单。
- 点击系统托盘图标：显示或隐藏叛逆汉堡大王。
- 右键系统托盘图标：打开完整菜单。

## 右键和托盘菜单

菜单包含：

- 显示/隐藏叛逆汉堡大王
- 始终置顶
- 缩放：`75%`、`100%`、`125%`、`150%`、`200%`，也可自定义 `50%` 到 `300%`
- 难过时间：可选择常用分钟数，也可自定义 `1` 到 `120` 分钟
- 重置位置
- 退出叛逆汉堡大王-桌面宠物

如果叛逆汉堡大王拖到屏幕边缘找不到了，可以在系统托盘菜单里选择“重置位置”。

## 设置保存

叛逆汉堡大王会自动记住：

- 上次位置
- 缩放比例
- 难过等待时间
- 是否始终置顶
- 是否隐藏

Windows 版配置通常保存在：

```text
%APPDATA%\叛逆汉堡大王-桌面宠物\settings.json
```

macOS 版配置通常保存在：

```text
~/Library/Application Support/叛逆汉堡大王-桌面宠物/settings.json
```

如果想恢复默认状态，可以退出程序后删除这个 `settings.json`，再重新运行 EXE。

## 退出和卸载

退出：

1. 右键叛逆汉堡大王或托盘图标。
2. 选择“退出叛逆汉堡大王-桌面宠物”。

卸载：

- 本项目是便携版，没有安装向导。
- Windows：删除下载的 EXE 或解压出的 `叛逆汉堡大王-桌面宠物.exe` 即可。
- macOS：删除 `.app`、`.dmg` 或解压目录即可。
- 如需清除用户设置，再删除 `%APPDATA%\叛逆汉堡大王-桌面宠物\settings.json`。

## 常见问题

### 为什么 Windows 提示风险？

因为当前版本没有购买代码签名证书。源码和构建脚本都在本仓库公开，用户可以自行检查或从源码构建。

### 为什么任务栏里看不到窗口？

叛逆汉堡大王是桌面宠物，默认使用透明无边框窗口，并隐藏普通任务栏入口。请使用桌面上的叛逆汉堡大王本体或系统托盘图标控制它。

### 叛逆汉堡大王不见了怎么办？

检查系统托盘图标，点击托盘图标可以显示/隐藏。也可以右键托盘图标，选择“重置位置”。

### 能在 macOS 或 Linux 运行吗？

当前 Release 提供 Windows x64 便携 EXE、macOS universal 未签名测试包，以及 Linux/UOS/Deepin deb 安装包。

## 开发

环境要求：

- Node.js 20 或更高版本
- npm
- Python 3 和 Pillow/OpenCV/imageio 用于生成预览 GIF/MP4

安装依赖：

```bash
npm install
```

启动开发版：

```bash
npm start
```

校验内置宠物资源：

```bash
npm run check:assets
```

打包 Windows 便携版：

```bash
npm run package:win
```

打包 macOS 测试版需要在 macOS 环境执行：

```bash
npm run package:mac
```

打包产物会生成到：

```text
dist/叛逆汉堡大王-桌面宠物.exe
```

导出动画预览 GIF 和 MP4：

```bash
npm run export:preview
```

预览文件会生成到：

```text
media/rebellious-burger-king-animation-preview.gif
media/rebellious-burger-king-animation-preview.mp4
```

## 项目结构

- `src/main.js`：Electron 主进程，负责透明窗口、托盘、拖拽、配置持久化。
- `src/renderer/`：Canvas 渲染和宠物动画控制。
- `assets/`：内置叛逆汉堡大王配置、精灵图和托盘图标。
- `media/`：动画预览 GIF/MP4。
- `scripts/check-assets.js`：资源尺寸和配置校验。
- `scripts/export-preview-media.py`：导出展示所有动作的短视频和 GIF。

## 许可证

本项目代码和随仓库发布的叛逆汉堡大王宠物资源使用 MIT License 开源。转载、修改或二次分发时请保留许可证声明。

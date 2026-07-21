一款用于制作服务端警笛音效的 FiveM 工具

## 致谢
感谢 @Dexyfex 开发的 [CodeWalker](https://github.com/dexyfex/CodeWalker)
由@asdvb38汉化

## 快速上手
前往 [发布页](https://github.com/BJDubb/SirenSharp/releases/latest) 下载最新版本安装包。
- **推荐方案**：运行安装程序 `.exe`。会自动安装软件，并在后台静默更新，新版本无需重新下载。
- **便携版**：解压便携压缩包 `.zip`，直接运行 `SirenSharp.exe`。无自动更新功能，升级需重新下载完整安装包。

## 交流社群
遇到任何问题，可加入 [Discord 社群](https://discord.gg/GCMRtBNCXR)，或私信作者 BJDubb#0001。

## 使用教程
前往 [官方文档](https://docs.sirensharp.dev/overview/what-is-sirensharp) 学习 SirenSharp 使用方法
B站/YouTube 视频教程点这里：[点击查看](https://youtu.be/oTv3mVHZAK0)

## 赞助支持
捐赠赞助，助力 SirenSharp 持续开发更新
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/T6T0L425H)

---

## 二、SirenSharp.exe 软件本体汉化步骤（单EXE .NET程序）
### 工具准备
dnSpy（专门编辑C#编译exe，汉化.NET程序专用）
### 操作流程
1. **备份原文件**
复制一份 `SirenSharp.exe` 改名 `原版备份.exe`，避免改错报废。
2. 打开 dnSpy，直接拖拽 `SirenSharp.exe` 进软件窗口加载
3. 两种提取文字方式
#### 方式1：全局一键搜所有界面文字（最快）
顶部菜单栏 → **搜索 → 搜索字符串**
输入关键词：`Create`/`Save`/`Export`/`Siren`/`Sound` 等，批量定位所有英文按钮、弹窗、提示文本。
#### 方式2：资源文件精准汉化（界面菜单文字）
左侧展开目录：`SirenSharp → Resources`
里面所有 `.resx`、`.resources` 文件储存窗口标题、按钮、选项文字
右键资源文件 → **编辑资源**，逐条替换中文：
例：
Create New Siren → 新建警笛
Export Siren File → 导出警笛文件
Save Project → 保存工程
Delete → 删除
Preview → 预览
注意：`{0}` `{1}` 这类占位符号**不许删除、修改**，只翻译前后文字。
4. 解决中文方框乱码
找到窗口窗体代码，将界面默认字体替换为：微软雅黑 / 宋体，保存后中文正常显示。
5. 保存汉化成品
顶部菜单「文件 → 保存模块」，生成全新汉化版 exe。

## 三、常见问题
1. 改完打开依旧英文
确认你修改的是 Resources 资源文件，不是代码内硬编码字符串；全部字符串都要替换。
2. 按钮文字截断显示不全
汉化翻译用词尽量简洁，不要过长；若界面固定，只能缩减中文字数。
3. 杀毒报毒
dnSpy修改.NET程序会被安全软件判定篡改程序，汉化完成后加入白名单，仅个人FiveM开服自用。

## 四、法律提醒
仅可个人学习、私服自用；未经作者BJDubb授权，禁止上传、分发、发布汉化版 SirenSharp。

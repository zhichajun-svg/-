[README.md](https://github.com/user-attachments/files/34232463/README.md)
# 盏茶待办

一款轻量的 Windows 桌面日历待办小工具：月 / 周 / 日三种视图、日程与待办分栏、自动月报、备忘录导出。单文件 exe，无需安装、无需联网，数据保存在本地 JSON。

## 功能

- **三种视图**：月视图（日历 + 日程栏 + 待办栏）、周视图（一周日程 + 底部操作行 + 待办浮窗）、日视图（单日聚焦，右侧贴边摆放）
- **日程**：时间、分类、颜色、子任务、完成状态；支持回撤为待办、复制、顺延到下一个工作日、上移 / 下移、删除
- **待办**：分类颜色、安排到日历（支持跨天与重复）、批量操作
- **卡片选中与多选**：所有视图的日程 / 待办卡片可点选，按住 `Ctrl` 多选，多选后「改 / 删 / 顺延 / 回撤 / 复制 / 安排」批量生效；子任务可单独选中
- **事项分类**：内置分类 + 自定义分类；双击分类可重命名、改颜色、删除；分类颜色会同步到卡片与日历色块
- **自动月报**：每月自动生成（也可手动立即生成）`月度总结-yyyy-MM.txt`，列出已完成与未完成事项；生成后可选择一键回撤、一键顺延或保持不变
- **备忘录**：标题 + 正文富文本（字体、字号、加粗、倾斜、下划线、高亮、格式刷），首行缩进与公文式排版；导出 PNG（公文 A4 / 手机长图两种模板）、Word、PDF，可直接打印
- **外观**：背景色 / 强调色（自定义取色会留存历史色块）、分隔线样式、整体透明度、最多 3 套「我的皮肤」
- **窗口**：无边框圆角、可拖动与四角缩放、对齐 20px 网格、日视图自动贴靠月视图右侧、位置与尺寸自动记忆
- **菜单栏**：置顶、紧凑模式、托盘常驻

## 运行

1. 下载 `dist/盏茶待办-Release.zip` 并解压，或直接下载 `DesktopCalendarTodo.exe`
2. 双击 `DesktopCalendarTodo.exe` 即可运行
3. 数据保存在程序目录的 `planner-data.json`（首次运行自动创建）

> 需要 .NET Framework 4.0 及以上（Windows 7 及以上系统自带）。

## 从源码构建

源码为 C# / WPF（.NET Framework 4.0），不依赖 NuGet，直接用系统自带的 `csc.exe` 编译：

```powershell
powershell -ExecutionPolicy Bypass -File src\DesktopCalendarTodo\build.ps1 -OutDir build_out
```

编译产物：`build_out\DesktopCalendarTodo.exe`。

## 目录结构

仓库里除说明文件外，源码与发布产物也提供压缩包（便于网页上传 / 直接下载）：

```
盏茶待办-完整包.zip    源码 + 发布产物 + 说明（解压即用）
src.zip                仅源码（解压后为 src/DesktopCalendarTodo/*.cs）
dist.zip               仅发布产物（exe、使用说明、更新说明、开机启动脚本、Release zip）
docs.zip               仅文档（使用说明、更新说明）

src/DesktopCalendarTodo/    C# 源码（MainWindow / Panels / Notes / Export / Models / DataStore / UiKit）
dist/                       发布包（exe + 说明 + 启动脚本）
docs/                       使用说明、更新说明
```

## 使用说明

见 [docs/使用说明.txt](docs/使用说明.txt)、[docs/更新说明.txt](docs/更新说明.txt)。

## 许可

MIT License，见 [LICENSE](LICENSE)。

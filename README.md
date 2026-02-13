# Foreground-Display-Keep-Alive （特定程序前台防暗屏）

仅在指定程序处于前台时阻止显示器息屏。


## 注意 Notes
目前界面主要为中文版本，欢迎扩展为多语言版本或改进本地化支持。

Currently the user interface is primarily available in Chinese. Contributions to extend it into a multi-language version are very welcome.

以下提供一个简要的界面标注说明，方便阅读。

A brief annotated reference is provided below for easier understanding of the interface.

<img width="1174" height="805" alt="image" src="https://github.com/user-attachments/assets/24aac567-3b9d-4084-948e-08050a55d072" />



## 项目简介

Foreground-Display-Keep-Alive 仅在指定程序处于前台活动状态时阻止显示器息屏。

当目标程序退到后台后，系统将立即恢复默认的息屏行为。

本工具不会修改系统电源计划，也不会永久阻止休眠，仅在需要时临时保持显示器常亮。


## 适用场景

* 远程控制 / 远程桌面
* 实时监控面板
* 演示展示
* 媒体播放软件
* 仅在特定程序前台时需要保持屏幕常亮的工作流程


## 主要功能

* 仅在目标程序前台时防暗屏
* 目标程序失去焦点后立即恢复系统默认行为
* 托盘常驻运行
* 单实例保护
* 可调整刷新间隔
* 一键设为当前前台程序
* 可选开机启动支持

## 工作原理（简述）

程序监测当前前台窗口，当检测到目标程序处于前台时调用：

```
SetThreadExecutionState(ES_DISPLAY_REQUIRED)
```

否则恢复为：

```
ES_CONTINUOUS
```

## 构建方式

需要 .NET 8 SDK。

下载地址：

[https://dotnet.microsoft.com/en-us/download/dotnet/8.0](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)
选择 “SDK 8.x.xxx” 版本。

构建命令：

```bash
dotnet publish -c Release -r win-x64 --self-contained true /p:PublishSingleFile=true
```

## 说明

* 仅支持 Windows
* 不联网
* 不收集数据
* 不修改系统电源计划


## 关于本项目

这是一个个人小工具项目，在 ChatGPT 的帮助下完成开发与测试。
作者并非专业软件开发人员，但程序已在实际使用中验证可用。

欢迎使用，也欢迎提出建议或改进意见。


## 开源协议

MIT License


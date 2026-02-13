# Foreground Display Keep Alive （特定程序前台防暗屏）
Prevent display sleep only when a specific application is in the foreground.

[中文说明 → README.zh-CN.md](README.zh-CN.md)




## Overview

ForegroundDisplayKeepAlive keeps your screen awake **only while a specified application is actively in the foreground**.  
Once the target program moves to the background, normal system sleep behavior is immediately restored.

This tool does **not** modify power plans or permanently block sleep.  
It simply applies display keep-alive conditionally.


## Use Cases

- Remote desktop / remote control sessions  
- Monitoring dashboards  
- Presentation software  
- Media playback tools  
- Any workflow requiring screen-on only during active use  


## Key Features

- Foreground-only display keep-alive  
- Immediate restore when target loses focus  
- Tray-based lightweight execution  
- Single-instance protection  
- Adjustable refresh interval  
- One-click “Set to current foreground app”  
- Optional startup support  


## How It Works (Brief)

It monitors the current foreground window and calls:

```

SetThreadExecutionState(ES_DISPLAY_REQUIRED)

````

only when the target application is active.


## Build

Requires .NET 8 SDK.

https://dotnet.microsoft.com/en-us/download/dotnet/8.0 and choose "SDK 8.x.xxx"

```bash
dotnet publish -c Release -r win-x64 --self-contained true /p:PublishSingleFile=true
````


## Notes

* Windows only
* No telemetry
* No network activity
* No modification of system power plans


## About This Project

This is a small personal utility created with the help of ChatGPT.
The author is not a professional software developer, but the tool is functional and tested in practical use.

Feedback, suggestions, and improvements are welcome!


## License

MIT License


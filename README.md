# Foreground Display Keep Alive （特定程序前台防暗屏）
Prevent display sleep only when a specific application is in the foreground.

[中文说明 → README.zh-CN.md](README.zh-CN.md)

---

## Overview

ForegroundDisplayKeepAlive keeps your screen awake **only while a specified application is actively in the foreground**.  
Once the target program moves to the background, normal system sleep behavior is immediately restored.

This tool does **not** modify power plans or permanently block sleep.  
It simply applies display keep-alive conditionally.

---

## Use Cases

- Remote desktop / remote control sessions  
- Monitoring dashboards  
- Presentation software  
- Media playback tools  
- Any workflow requiring screen-on only during active use  

---

## Key Features

- Foreground-only display keep-alive  
- Immediate restore when target loses focus  
- Tray-based lightweight execution  
- Single-instance protection  
- Adjustable refresh interval  
- One-click “Set to current foreground app”  
- Optional startup support  

---

## How It Works (Brief)

It monitors the current foreground window and calls:


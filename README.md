# EmuBox Web

EmuBox 项目的静态展示站点与资源获取页。主项目为 Android 应用 [mihsian77/Emubox](https://github.com/mihsian77/Emubox)（正式签名发布）。

- **在线访问**：https://mihsian77.github.io/EmuHub/
- **站点定位**：提供 EmuBox 的项目介绍、功能说明与常用资源获取入口；Android 应用不可用时，可经本站获取最新 APK 与常用驱动/组件。
- **下载加速**：下载链接经 [MirrorHub](https://github.com/mihsian77/MirrorHub)（MIT）加速节点自动转发，选取延迟最低节点；节点不可用时回退 GitHub 直连。
- **技术栈**：静态 HTML + 原生 JavaScript，无后端依赖，可部署于任意静态托管。

## 功能

- 项目介绍与已发布功能说明
- 最新 APK 获取（自动选择最快加速节点）
- 备用资源下载：常用驱动（Turnip / PanVK）与转译组件（DXVK / Box64 / VKD3D-Proton 等）最新版本入口

## 项目结构

```
├── index.html     # 站点主页面
├── README.md      # 本说明
└── .github/workflows/   # 部署与检查工作流
```

## 来源声明

- 界面与资源目录整理基于 [NotZeetaa/EmuHub](https://github.com/NotZeetaa/EmuHub) 与 [Rodrig02005/EmuHub-APP](https://github.com/Rodrig02005/EmuHub-APP)（均为 MIT 协议），本项目已独立更名并持续维护。
- 加速节点数据由 [MirrorHub](https://github.com/mihsian77/MirrorHub)（MIT）提供。
- 所有驱动与组件版权归各自作者所有，本站仅提供获取入口。

## 协议

MIT License。

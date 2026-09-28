# 🎮 EmuHub 网页版（备选）

> 📱 **推荐使用 Android App：[EmuHub 国内版](https://github.com/mihsian77/EmuHub-CN)**
>
> 本仓库为 EmuHub 国内版的**网页备选方案**，已归档（只读），不再更新。
> 当 GitHub 下载 APK 限速、或不想安装 App 时，可通过本网页直接下载驱动与组件。

基于 [NotZeetaa/EmuHub](https://github.com/NotZeetaa/EmuHub) 静态网页修改，添加中文界面、国内下载加速与 i18n 自动化校验。

---

## 🌐 在线访问

**https://mihsian77.github.io/EmuHub/**

---

## ✨ 功能

| 功能 | 说明 |
|------|------|
| 🌐 中文界面 | 完整简体中文汉化，可在设置中切换中/英文 |
| 🚀 国内下载加速 | 内置 5 个 GitHub 加速节点，自动测速选延迟最低，可手动切换 |
| ⚙️ 设置面板 | 语言切换 + 加速节点管理 + 实时延迟显示 |
| 📦 驱动信息 | 自动获取最新 Turnip 驱动版本与下载链接 |

---

## ⚡ 加速节点

内置节点（均为公益反代，如失效请在设置中切换）：

- `gh-proxy.org` — 官方主力
- `ghfast.top` — 多线 CDN
- `mirror.ghproxy.com` — 老牌
- `github.moeyy.xyz`
- `gh.llkk.cc`

---

## 📁 项目结构

```
├── index.html                  # 主页面
├── locales/
│   ├── en.json                 # 英文基准词条
│   └── zh-CN.json              # 简体中文翻译
├── scripts/
│   ├── extract-i18n.mjs        # 从 HTML 提取可翻译字符
│   └── check-i18n.mjs          # 翻译完整性校验
├── latest-release.json         # 最新驱动信息（Actions 自动更新）
└── .github/workflows/          # CI/CD（同步上游 / i18n检查 / 部署Pages）
```

---

## 🧩 资源归属

所有驱动与软件版权归原作者所有。本网页仅为社区资源导航，与任何项目均无隶属关系。

| 工具 | 仓库 |
|------|------|
| Turnip Drivers | https://github.com/StevenMXZ/Adreno-Tools-Drivers |
| DXVK | https://github.com/doitsujin/dxvk |
| VKD3D | https://github.com/HansKristian-Work/vkd3d-proton |
| Box64 | https://github.com/ptitSeb/box64 |
| Wine | https://www.winehq.org |

---

## 📜 协议

MIT License。原作者 NotZeetaa，网页版修改 moon279。

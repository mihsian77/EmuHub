# 🎮 EmuHub 汉化版 — Android 模拟资源中心

> 上游仓库：[NotZeetaa/EmuHub](https://github.com/NotZeetaa/EmuHub)
> 本仓库为社区汉化分支，添加中文界面、国内下载加速与 i18n 自动化校验。

**一站式获取 GPU 驱动、Winlator 修改版、游戏补丁，以及在安卓设备上运行 PC 游戏所需的全部工具。**

---

## ✨ 本分支新增功能

| 功能 | 说明 |
|------|------|
| 🌐 中文界面 | 完整简体中文汉化，专业国内用语，可在设置中切换中/英文 |
| 🚀 国内下载加速 | 内置 5 个 GitHub 加速节点，自动测速选延迟最低，可手动切换 |
| ⚙️ 设置面板 | 右上角齿轮打开，语言切换 + 加速节点管理 + 实时延迟显示 |
| 🔄 上游自动同步 | GitHub Actions 每天自动合并上游更新，冲突时开 PR 人工处理 |
| 🔍 i18n 编译检查 | CI 自动检查漏译、多译、空译、占位符丢失，阻断有问题的合并 |
| 📦 最新驱动静态化 | 每天自动获取最新 Gen8 驱动信息，前端无需直连 GitHub API |

---

## 🚀 访问

部署在 GitHub Pages：`https://<你的用户名>.github.io/EmuHub/`

首次部署需在仓库 **Settings → Pages → Source** 选择 **GitHub Actions**。

---

## 🛠 本地开发

```bash
git clone <你的仓库地址>
cd EmuHub
# 直接用浏览器打开 index.html 即可（中文需通过 HTTP 服务器访问以加载 locales/*.json）
# 推荐：python3 -m http.server 8080
```

### i18n 脚本

```bash
# 检查 HTML/JS 中的 key 是否都在 en.json 中
node scripts/extract-i18n.mjs

# 检查翻译完整性（漏译/多译/空译/占位符）
node scripts/check-i18n.mjs

# 自动补全 en.json 中缺失的 key
node scripts/extract-i18n.mjs --fix
```

---

## 📁 项目结构

```
├── index.html                  # 主页面（i18n + 设置 + 加速）
├── locales/
│   ├── en.json                 # 英文基准词条
│   └── zh-CN.json              # 简体中文翻译
├── scripts/
│   ├── extract-i18n.mjs         # 从 HTML 提取可翻译字符
│   └── check-i18n.mjs          # 翻译完整性校验
├── latest-release.json         # 最新 Gen8 驱动信息（Actions 自动更新）
└── .github/workflows/
    ├── sync-upstream.yml       # 每天同步上游
    ├── i18n-check.yml          # i18n 编译检查
    ├── update-latest-release.yml  # 最新驱动信息静态化
    └── deploy-pages.yml        # GitHub Pages 部署
```

---

## ⚡ 加速节点

内置节点（均为公益反代，如失效请在设置中切换）：

- `gh-proxy.org` — 官方主力，支持 Release / Raw / API
- `ghfast.top` — 多线 CDN
- `mirror.ghproxy.com` — 老牌
- `github.moeyy.xyz`
- `gh.llkk.cc`

加速仅对 GitHub 下载链接生效，GameHub 官网等国内源保持直连。

---

## 🧩 资源归属

所有驱动与软件版权归原作者所有。本站仅为社区资源导航，与任何项目均无隶属关系。

| 工具 | 仓库 |
|------|------|
| Turnip Drivers | https://github.com/StevenMXZ/Adreno-Tools-Drivers |
| Winlator | https://github.com/brunodev85/winlator |
| DXVK | https://github.com/doitsujin/dxvk |
| VKD3D | https://github.com/HansKristian-Work/vkd3d-proton |
| Box64 | https://github.com/ptitSeb/box64 |

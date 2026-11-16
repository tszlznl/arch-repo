# tszlznl's Personal Arch Linux Pacman Repository

Personal Arch Linux / CachyOS software repository for desktop tools and agents.

## 📦 包含的软件包 (Packages)

| 软件 (Package) | 简介 (Description) | 上游 (Upstream) |
| :--- | :--- | :--- |
| **`videodown`** | 哔哩哔哩、抖音、YouTube 原生高性能下载器 | [tszlznl/videodown](https://github.com/tszlznl/videodown) |
| **`cindy-bin`** | 开源开箱即用 AI Agent 桌面客户端 (Global 版) | [makecindy/cindy](https://github.com/makecindy/cindy) |
| **`quiet-md-bin`** | 又快又安静的本地 Markdown 笔记 (Rust + GPUI) | [s1dashu/quiet-md](https://github.com/s1dashu/quiet-md) |
| **`spotish-bin`** | 基于 NSH 构建的原生 Spotify 客户端 | [huacnlee/spotish](https://github.com/huacnlee/spotish) |
| **`cicada-bin`** | 知了 Cicada · 实时会议字幕、同声传译与 AI 纪要 | [wquguru/cicada](https://github.com/wquguru/cicada) |
| **`denova-bin`** | 开源 AI 小说写作与角色扮演工作台 | [alfredxw/denova](https://github.com/alfredxw/denova) |
| **`crommacode-bin`** | 专为 AI Coding Agent 设计的可视化桌面工作台 | [cromma.ai/code](https://cromma.ai/code) |

---

## 🚀 如何使用 (Usage)

在你的系统配置文件 `/etc/pacman.conf` 中追加以下内容：

```ini
[tszlznl]
SigLevel = Optional TrustAll
Server = https://tszlznl.github.io/arch-repo/$arch
```

同步仓库并安装软件：

```bash
sudo pacman -Syu
sudo pacman -S videodown cindy-bin quiet-md-bin spotish-bin cicada-bin denova-bin crommacode-bin
```

---

## ⚙️ 自动更新机制 (Automation)

- 本仓库由 **GitHub Actions** 容器环境每天定时自动从上游 Release 构建最新的 `.pkg.tar.zst`。
- 构建完成后自动生成仓库索引数据库 (`tszlznl.db.tar.gz`) 并发布到 GitHub Pages。

# MediaHub

<p align="center">
  <strong>面向 Emby、115 云盘与飞牛 NAS 生态的一站式媒体管理面板</strong><br/>
  把媒体库整理、任务自动化、Webhook 与消息通知集中到一个更顺手的控制台里。
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Nuxt-3-00DC82?style=flat-square&logo=nuxtdotjs&logoColor=white" alt="Nuxt 3" />
  <img src="https://img.shields.io/badge/Vue-3-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white" alt="Vue 3" />
  <img src="https://img.shields.io/badge/TypeScript-5-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/SQLite-better--sqlite3-003B57?style=flat-square" alt="SQLite" />
  <img src="https://img.shields.io/badge/Node--Cron-Scheduler-6C43E0?style=flat-square" alt="node-cron" />
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=flat-square" alt="MIT License" />
  <img src="https://img.shields.io/badge/FnOS-FPK_Supported-4F46E5?style=flat-square" alt="FnOS FPK" />
</p>

<p align="center">
  <sub>支持独立部署，也支持按飞牛 NAS 应用。</sub>
</p>

---

## 功能亮点

- **媒体库总览**：集中查看 Emby 媒体库统计、最近入库、最近播放与封面内容
- **115 智能整理**：自动识别影视信息，结合 TMDB 生成目标路径并执行整理
- **Emby 工具集**：缺失剧集检测、重复内容分析、封面生成、Webhook 日志
- **任务自动化**：签到、清理、自动整理统一管理，支持定时执行与手动触发
- **通知联动**：支持 Telegram、微信与 Webhook 推送

## 为什么是 MediaHub

MediaHub 不是单点工具集合，而是一个围绕家庭影音库场景构建的前后端一体面板。你可以在同一套界面里完成媒体库查看、115 文件整理、任务调度、Webhook 联动与通知配置，减少在多个脚本、容器和页面之间来回切换的成本。

## 界面预览

<table>
  <tr>
    <td align="center" width="50%"><strong>Dashboard</strong><br/><img src="./docs/screenshots/dashboard.png" alt="Dashboard" width="100%" /></td>
    <td align="center" width="50%"><strong>Organize</strong><br/><img src="./docs/screenshots/organize.png" alt="Organize" width="100%" /></td>
  </tr>
  <tr>
    <td align="center" width="50%"><strong>Emby Tools</strong><br/><img src="./docs/screenshots/emby-tools.png" alt="Emby Tools" width="100%" /></td>
    <td align="center" width="50%"><strong>Tasks</strong><br/><img src="./docs/screenshots/tasks.png" alt="Tasks" width="100%" /></td>
  </tr>
  <tr>
    <td align="center" colspan="2"><strong>Settings</strong><br/><img src="./docs/screenshots/settings.png" alt="Settings" width="100%" /></td>
  </tr>
</table>

## 适用场景

- 家庭影音库 / NAS / Homelab 的统一控制台
- 115 下载目录的自动归档、重命名与整理
- Emby 媒体库的日常维护、巡检与排障
- 需要签到、清理、通知联动的个人媒体自动化流程

## 技术栈

- **Frontend:** Nuxt 3, Vue 3, TypeScript
- **UI:** @nuxt/ui
- **Server:** Nitro / h3
- **Database:** better-sqlite3
- **Scheduler:** node-cron
- **Third-party:** Emby API, 115 云盘, TMDB, Telegram, 微信 iLink Bot

## License

本项目采用 **MIT License**。

你可以在 [LICENSE](./LICENSE) 查看完整授权内容。

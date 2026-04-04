# MediaHub

<p align="center">
  <strong>为你的 Emby 与 115 云盘打造的一站式媒体管理面板</strong>
</p>

<p align="center">
  一个围绕家庭影音库、媒体自动化整理与消息通知打造的可视化控制台。
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Nuxt-3-00DC82?style=flat-square&logo=nuxtdotjs&logoColor=white" alt="Nuxt 3" />
  <img src="https://img.shields.io/badge/Vue-3-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white" alt="Vue 3" />
  <img src="https://img.shields.io/badge/TypeScript-5-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/SQLite-better--sqlite3-003B57?style=flat-square" alt="SQLite" />
  <img src="https://img.shields.io/badge/Node--Cron-Scheduler-6C43E0?style=flat-square" alt="node-cron" />
</p>

---

## 产品简介

MediaHub 是一个前后端一体的媒体管理面板，用来把你分散在不同服务里的媒体维护工作整合起来。

它把以下能力放进一个统一界面中：

- **Emby 仪表盘**
- **115 云盘整理**
- **定时任务自动化**
- **Telegram / 微信通知**
- **Webhook 与日志查看**

它的目标不是做一个通用 CMS，而是围绕 **家庭影音库**、**NAS / Homelab**、**媒体自动化维护** 这些真实使用场景，提供一套真正能每天用起来的工具。

## 为什么选择 MediaHub

当媒体系统逐渐变复杂后，常见问题往往会一起出现：

- Emby 里最近新增了什么，不够直观
- 云盘下载后的文件命名混乱，整理起来费时费力
- 手动签到、清理回收站、整理目录，重复又琐碎
- Webhook 事件、整理结果、任务执行状态缺少统一通知入口

MediaHub 想解决的，就是这些“每天都会遇到，但没有统一入口”的问题。

## 功能亮点

### Emby 仪表盘

通过首页快速掌握媒体库状态：

- 媒体库统计总览
- 最近入库内容
- 最近播放内容
- 媒体库封面展示
- Emby 配置状态检查

适合日常巡检，也适合作为你的家庭媒体系统首页。

### Emby 工具集

围绕 Emby 日常维护，提供多种实用能力：

- **缺失剧集检测**：对比 Emby 与 TMDB 数据，发现缺失集数
- **剧集查重分析**：识别重复剧集并支持导出报告
- **封面生成**：生成并上传封面到 Emby
- **Webhook 集成**：接收 Emby 事件并展示处理日志

### 115 云盘整理

这是 MediaHub 最核心的业务能力之一。

你可以直接在界面中浏览 115 保存目录，并完成从“识别”到“整理”的整条流程：

- 浏览云盘目录
- 自动识别影视文件信息
- 结合 TMDB 进行匹配
- 自动生成规范化目标路径
- 支持移动 / 复制整理
- 支持文件夹批量整理
- 支持字幕处理与空目录清理
- 支持整理记录追踪与自动整理

如果你长期依赖 115 云盘作为下载与缓存入口，这一能力可以明显减少手工整理时间。

### 定时任务自动化

MediaHub 提供内置任务调度能力，把重复劳动交给系统：

- 115 自动签到
- 115 回收站清理
- 飞牛论坛签到
- GlaDOS 签到
- 影巢签到
- 自动整理任务

所有任务都可以在界面中集中查看、配置与手动触发。

### 消息通知

关键结果不必等你手动打开页面查看。

MediaHub 支持：

- Telegram 通知
- Telegram 机器人命令能力
- 微信通知
- 整理结果推送
- Webhook 事件推送
- 定时任务结果推送

这样你可以把“媒体系统状态”接入自己常用的消息渠道。

## 截图预览

> 你可以把下面占位内容替换成真实截图。

### 仪表盘

```md
![Dashboard](./docs/screenshots/dashboard.png)
```

### 云盘整理

```md
![Organize](./docs/screenshots/organize.png)
```

### Emby 工具集

```md
![Emby Tools](./docs/screenshots/emby-tools.png)
```

### 参数配置

```md
![Settings](./docs/screenshots/settings.png)
```

### 推荐截图目录结构

```text
docs/
└─ screenshots/
   ├─ dashboard.png
   ├─ organize.png
   ├─ emby-tools.png
   ├─ settings.png
   └─ mobile-dashboard.png   # 可选：移动端展示
```

### 推荐命名规范

建议统一使用 **小写英文 + 连字符** 或简洁页面名，方便长期维护：

- `dashboard.png`：仪表盘首页
- `organize.png`：云盘整理页
- `emby-tools.png`：Emby 工具集页
- `settings.png`：参数配置页
- `tasks.png`：定时任务页
- `mobile-dashboard.png`：移动端首页

如果后续截图变多，也可以按模块拆分：

- `emby-missing.png`
- `emby-webhook.png`
- `organize-recognize.png`
- `organize-result.png`

### 截图建议

为了让 GitHub 首页展示更整洁，建议：

- 优先使用 16:9 或接近比例的桌面截图
- 保持相同主题风格（统一浅色或统一深色）
- 截图前隐藏敏感信息，例如 Cookie、Token、手机号、路径隐私信息
- 首页只放 3-4 张最能体现核心能力的截图

## 适用场景

MediaHub 适合这些用户：

- 家庭影音库管理者
- Emby 媒体库维护者
- 使用 115 云盘作为下载或缓存入口的用户
- 希望减少重复手工整理的人
- Homelab / NAS 场景下需要轻量控制台的用户

它不是一个通用型内容管理系统，而是一套更偏向 **个人媒体运营面板** 的工具集合。

## 技术架构

MediaHub 采用前后端一体的单仓结构：

- **Frontend:** Nuxt 3, Vue 3, TypeScript
- **UI:** @nuxt/ui
- **Server:** Nitro / h3
- **Database:** better-sqlite3
- **Scheduler:** node-cron
- **Third-party:** Emby API, 115 云盘, TMDB, Telegram, 微信 iLink Bot

这种结构让它既有可视化界面，也具备稳定的后端任务与本地持久化能力。

## FAQ

### 1. MediaHub 是只做前端面板吗？

不是。它是一个前后端一体的 Nuxt 项目，既有可视化页面，也有服务端 API、SQLite 持久化和定时任务能力。

### 2. 必须配置所有第三方服务才能使用吗？

不需要。你可以只启用自己需要的模块，例如只使用 Emby 仪表盘，或只使用 115 云盘整理。

### 3. 115 云盘整理会直接影响我的媒体目录吗？

会。它支持移动 / 复制等整理操作，因此建议你先在测试目录验证命名模板、分类策略与识别效果。

### 4. 是否适合部署在 NAS / Homelab 环境中？

适合。这个项目本身就很贴近家庭媒体与自部署场景，适合作为个人媒体控制台使用。

### 5. 是否支持自动化运行？

支持。项目内置基于 `node-cron` 的调度器，可配置多种定时任务与自动整理流程。

## 注意事项

- 项目依赖多个第三方服务，请确保相关配置正确可用
- 115 / Telegram / 微信能力依赖有效凭证或登录状态
- 建议先在测试目录验证整理规则与命名模板，再用于正式媒体库
- 某些功能依赖外部网络访问质量，如 Emby、TMDB、消息推送服务

## License

如需开源发布，请根据你的实际意图补充许可证，例如 MIT / Apache-2.0 / GPL-3.0。

当前仓库未检测到明确的 License 文件，因此本 README 不对授权方式做默认声明。

<div align="center">

<br/>

# 🖥️ One Server

**面向飞牛 NAS 的 MacOS 风格 SSH 终端管理工具**

<br/>

一个同时适配 **桌面端 · 手机端 · fnOS iframe** 的轻量 SSH 管理与终端应用

聚焦 **好看 · 好用 · 好维护** 的 NAS 端 SSH 体验

<br/>

<p>
  <img src="https://img.shields.io/badge/license-MIT-059669?style=flat-square&labelColor=0f172a" alt="License" />
  <img src="https://img.shields.io/badge/platform-fnOS-0ea5e9?style=flat-square&labelColor=0f172a" alt="Platform" />
  <img src="https://img.shields.io/badge/node-%3E%3D24-16a34a?style=flat-square&labelColor=0f172a" alt="Node" />
  <img src="https://img.shields.io/badge/React-19-0891b2?style=flat-square&labelColor=0f172a" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-5.x-2563eb?style=flat-square&labelColor=0f172a" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Express-5-000000?style=flat-square&labelColor=0f172a" alt="Express" />
</p>

<p>
  <strong>React 19</strong> &middot;
  <strong>TypeScript</strong> &middot;
  <strong>Express 5</strong> &middot;
  <strong>xterm.js</strong> &middot;
  <strong>ssh2</strong> &middot;
  <strong>fnOS</strong>
</p>

<p>
  <a href="#功能总览">功能总览</a> &middot;
  <a href="#api-接口文档">API 接口</a> &middot;
  <a href="#安全设计">安全设计</a> &middot;
  <a href="#项目结构">项目结构</a>
</p>

<br/>

</div>

---

## 功能总览

<table>
<tr>
<td width="25%" align="center"><strong>🔐 安全存储</strong></td>
<td width="25%" align="center"><strong>📡 SSH 终端</strong></td>
<td width="25%" align="center"><strong>📊 资源监控</strong></td>
<td width="25%" align="center"><strong>🔔 实时告警</strong></td>
</tr>
<tr>
<td align="center">主密码保护<br/>敏感字段加密落盘<br/>密钥库自动锁定</td>
<td align="center">多标签会话<br/>自动重连<br/>键盘快捷键</td>
<td align="center">CPU / 内存 / 磁盘<br/>CPU 温度 · 开机时间<br/>国旗自动识别</td>
<td align="center">阈值自定义<br/>超限高亮提示<br/>轻量监控替代方案</td>
</tr>
</table>

---

## 核心功能

### 🔐 安全存储

| 功能 | 说明 |
|------|------|
| 主密码保护 | 首次使用必须设置主密码，密码不明文存储 |
| 加密落盘 | 主机密码、私钥、私钥口令加密后写入磁盘 |
| 密钥库锁定 | 支持手动锁定，解锁状态默认 30 分钟自动失效 |
| 主密码修改 | 已解锁状态下可更换主密码，自动用新密钥重新加密所有敏感字段 |
| 密钥库导入/导出 | 支持导出加密备份文件，换设备或重装后一键恢复 |

### 📡 SSH 与终端

| 功能 | 说明 |
|------|------|
| 主机管理 | 新增、编辑、删除、列表管理，拖拽排序 |
| 多种认证 | 支持密码登录与私钥登录 |
| 多标签终端 | 基于 xterm.js，多标签页会话切换 |
| 终端尺寸同步 | 窗口大小变化实时同步到远端 PTY |
| 会话复用 | 已连接主机支持复用已有会话，避免重复建连 |
| 会话保活 / 自动重连 | 网络波动后自动尝试恢复 SSH 会话（最多 5 次，指数退避） |
| SSH 主机密钥验证 | 首次连接记录公钥指纹，后续自动校验，防止中间人攻击 |
| 键盘快捷键 | `Alt+N` 新建连接 · `Alt+W` 关闭标签 · `Alt+←/→` 切换会话 |

### 📊 资源监控

| 功能 | 说明 |
|------|------|
| CPU 监控 | 实时使用率、核心数、温度（不支持温度的设备自动隐藏） |
| 内存监控 | 使用率、SWAP 使用率，一键切换显示 |
| 磁盘监控 | 使用率与挂载点信息 |
| 开机时间 | 系统运行天数统计 |
| 地理识别 | 主机地理位置与国旗自动识别 |

### 🔔 实时告警

| 功能 | 说明 |
|------|------|
| 阈值监控 | CPU / 内存 / 磁盘超过阈值时侧边栏高亮提示 |
| 自定义阈值 | 支持通过 API 自定义告警阈值 |
| 脉冲动画 | 超限指标带脉冲动画与颜色编码，直观醒目 |

### 🎨 外观与显示

| 功能 | 说明 |
|------|------|
| 亮色 / 暗色模式 | 全局主题切换 |
| 终端主题 | 午夜蓝 / 曜石黑 / 日光白 |
| 终端字体 | Courier / Menlo / Monaco / JetBrains Mono / SF Mono / Fira Code |
| 终端字号 | 支持自定义调节 |
| MacOS 风格 | 偏液态玻璃的视觉方向，窗口化标题栏 |

### 📱 移动端适配

| 功能 | 说明 |
|------|------|
| 响应式布局 | 自动适配桌面端与手机端 |
| 单页切换 | 手机端"列表 / 终端"单页式切换 |
| 会话保持 | 返回列表后保留已连接会话，再次进入复用原会话 |

### 🛡️ 稳定性与安全

| 功能 | 说明 |
|------|------|
| API 速率限制 | 安全接口 15min/10次，写操作 1min/30次 |
| WebSocket 认证 | 首条消息握手认证，5 秒超时断开 |
| CSP 安全响应头 | 7 项安全响应头，防 XSS / 点击劫持 / MIME 嗅探 |
| 并发写入保护 | 文件锁 + 原子写入，防止数据损坏 |
| 数据防护 | 未解锁状态下禁止修改磁盘数据 |
| Error Boundary | 全局错误边界，避免渲染异常导致白屏 |
| 优雅停机 | SIGINT / SIGTERM 信号处理，先关监听再释放会话 |

---

## API 接口文档

> 所有 REST API 均以 `/api/v1` 为前缀。WebSocket 通道无版本前缀。

### 认证机制

| 项目 | 说明 |
|------|------|
| 客户端标识 | 请求需携带 `clientId` 查询参数 |
| 认证令牌 | 密钥库解锁后返回 `Authorization: Bearer <token>`，后续请求需携带 |
| 401 | 认证失效 |
| 423 | 密钥库已锁定 |

### 健康检查

| 方法 | 路径 | 说明 | 认证 |
|------|------|------|:----:|
| `GET` | `/api/v1/health` | 健康检查 | ❌ |
| `GET` | `/api/v1/app/info` | 获取运行信息（平台、架构） | ❌ |

### 密钥库接口

| 方法 | 路径 | 说明 | 认证 | 速率限制 |
|------|------|------|:----:|:--------:|
| `GET` | `/api/v1/security/state` | 获取密钥库状态（configured / unlocked / authenticated） | ❌ | — |
| `POST` | `/api/v1/security/setup` | 初始化主密码（首次使用） | ❌ | 15min/10次 |
| `POST` | `/api/v1/security/unlock` | 解锁密钥库 | ❌ | 15min/10次 |
| `POST` | `/api/v1/security/lock` | 锁定密钥库 | ✅ | — |
| `POST` | `/api/v1/security/change-password` | 修改主密码 | ✅ | 15min/10次 |

### 主机管理接口

| 方法 | 路径 | 说明 | 认证 | 速率限制 |
|------|------|------|:----:|:--------:|
| `GET` | `/api/v1/hosts` | 获取主机列表 | ✅ | — |
| `POST` | `/api/v1/hosts` | 新增主机 | ✅ | 1min/30次 |
| `PUT` | `/api/v1/hosts/:id` | 更新主机 | ✅ | 1min/30次 |
| `DELETE` | `/api/v1/hosts/:id` | 删除主机 | ✅ | 1min/30次 |
| `PUT` | `/api/v1/hosts/reorder` | 调整主机排序 | ✅ | 1min/30次 |
| `POST` | `/api/v1/hosts/export` | 导出主机配置（加密备份） | ✅ | 1min/30次 |
| `POST` | `/api/v1/hosts/import` | 导入主机配置（加密备份） | ✅ | 1min/30次 |

### 资源统计接口

| 方法 | 路径 | 说明 | 认证 |
|------|------|------|:----:|
| `GET` | `/api/v1/hosts/stats` | 批量获取所有主机资源使用情况 | ✅ |
| `GET` | `/api/v1/hosts/:id/stats` | 获取单个主机资源使用情况 | ✅ |

### 告警接口

| 方法 | 路径 | 说明 | 认证 |
|------|------|------|:----:|
| `GET` | `/api/v1/alerts/thresholds` | 获取当前告警阈值 | ✅ |
| `PUT` | `/api/v1/alerts/thresholds` | 更新告警阈值 | ✅ |
| `POST` | `/api/v1/alerts/check` | 检查资源指标是否超过阈值 | ✅ |

### WebSocket 终端通道

| 路径 | 说明 |
|------|------|
| `WS /ws/terminal?clientId=xxx` | 终端消息通道 |

**握手流程：**

1. 客户端连接 WebSocket，携带 `clientId` 查询参数
2. 发送 `auth` 消息完成认证（5 秒超时）
3. 认证成功后可发送 `connect` / `input` / `resize` / `reconnect` / `disconnect` 消息
4. 服务端推送 `output` / `status` / `error` / `exit` 消息

**客户端 → 服务端：**

| 类型 | 说明 |
|------|------|
| `auth` | 认证 `{ clientId, authToken }` |
| `connect` | 建立 SSH 连接 `{ sessionId, host, port, username, authMethod, ... }` |
| `input` | 发送终端输入 `{ sessionId, data }` |
| `resize` | 调整终端尺寸 `{ sessionId, cols, rows }` |
| `reconnect` | 重连已有会话 `{ sessionId, cols, rows }` |
| `disconnect` | 断开会话 `{ sessionId }` |

**服务端 → 客户端：**

| 类型 | 说明 |
|------|------|
| `auth_ok` | 认证成功 |
| `auth_error` | 认证失败 |
| `output` | 终端输出 `{ sessionId, data }` |
| `status` | 会话状态变更 `{ sessionId, status }` |
| `error` | 连接错误 `{ sessionId, message }` |
| `exit` | 会话退出 `{ sessionId }` |

---

## 安全设计

### 数据安全

```
┌─────────────────────────────────────────────────────────┐
│                      用户输入主密码                        │
└───────────────────────┬─────────────────────────────────┘
                        ▼
┌─────────────────────────────────────────────────────────┐
│  PBKDF2 + scrypt 双重哈希                                │
│  主密码 → 密码哈希 → 存储到 vault.json                     │
│  主密码 → 解密密钥 → 仅保留在运行时内存                      │
└───────────────────────┬─────────────────────────────────┘
                        ▼
┌─────────────────────────────────────────────────────────┐
│  AES-256-GCM 加密                                       │
│  主机密码 / 私钥 / 私钥口令 → 加密后写入 hosts.json         │
└─────────────────────────────────────────────────────────┘
```

### 防护机制

| 机制 | 说明 |
|------|------|
| 速率限制 | 安全接口 15min/10次，写操作 1min/30次，429 返回 `Retry-After` |
| WebSocket 认证 | 首条消息握手，5 秒超时断开，令牌不暴露在 URL 中 |
| CSP 安全头 | Content-Security-Policy / X-Content-Type-Options / Referrer-Policy 等 7 项 |
| 数据防护 | 未解锁状态下禁止修改磁盘数据，防止数据损坏 |
| 并发写入保护 | 文件锁 + 原子写入（临时文件 + rename），防止并发写入导致数据损坏 |
| 自动锁定 | 解锁状态默认 30 分钟失效，按设备独立维护 |
| 主机密钥验证 | 首次连接记录公钥指纹，后续自动校验，防止中间人攻击 |
| 导出加密 | 配置导出使用 AES-256-GCM 加密，需设置独立加密密码 |

---

## 技术栈

<table>
<tr>
<th>前端</th>
<th>后端</th>
<th>打包部署</th>
</tr>
<tr>
<td>

- React 19
- TypeScript
- Vite
- xterm.js
- @xterm/addon-fit

</td>
<td>

- Node.js 24
- Express 5
- ws (WebSocket)
- ssh2
- TypeScript

</td>
<td>

- npm workspaces
- GitHub Actions
- fnpack
- fnOS 应用打包

</td>
</tr>
</table>

---

## 项目结构

```
OneServer/
├── apps/
│   ├── server/                  # Express + WebSocket + SSH 后端
│   │   ├── src/
│   │   │   ├── routes/          # API 路由（hosts / security / alerts）
│   │   │   ├── ssh/             # SSH 会话管理与主机密钥验证
│   │   │   ├── ws/              # WebSocket 终端网关
│   │   │   ├── storage/         # 数据存储（主机仓库 / 密钥库）
│   │   │   └── lib/             # 工具库（加密 / 文件操作 / 安全头）
│   │   └── dist/                # 编译产物
│   └── www/                     # React + Vite 前端
│       ├── src/
│       │   ├── components/      # UI 组件（终端 / 安全 / 侧边栏）
│       │   ├── hooks/           # 自定义 Hooks（useVault / useHosts / useApi）
│       │   ├── pages/           # 页面组件（DesktopShell）
│       │   └── lib/             # 工具库（外观 / 客户端ID）
│       └── dist/                # 构建产物
├── shared/                      # 前后端共享类型
├── App.Native.OneServer/        # fnOS 打包壳
├── .github/workflows/           # GitHub Actions CI/CD
├── test.mjs                     # 自动化测试脚本（100 用例）
└── package.json                 # workspace 根配置
```

### 数据存储

后端运行时在数据目录中保存以下文件：

| 文件 | 说明 |
|------|------|
| `vault.json` | 主密码元数据（密码哈希、盐值） |
| `hosts.json` | 已加密的主机配置 |
| `known_hosts.json` | SSH 主机公钥指纹记录 |

数据目录解析优先级：`TRIM_PKGVAR` → `TRIM_PKGDIR/var` → 本地 `data/`

---

## 键盘快捷键

| 快捷键 | 功能 |
|--------|------|
| `Alt + N` | 新建连接 |
| `Alt + W` | 关闭当前标签 |
| `Alt + →` | 切换到下一个会话（循环） |
| `Alt + ←` | 切换到上一个会话（循环） |

> 使用 `Alt` 修饰键而非 `Ctrl`，避免与浏览器原生快捷键冲突。

---

## 适用场景

- 🏠 在飞牛 NAS 上集中管理多台 Linux 主机
- 📱 在浏览器或手机上快速进入 SSH 终端
- 🔧 家庭实验室、轻量运维、局域网设备管理
- 📦 作为 fnOS 原生应用部署，无需额外维护 Docker

---

## License

[MIT License](LICENSE)

---

<div align="center">

**One Server**

让飞牛 NAS 上的 SSH 终端，更像一个真正可长期使用的应用。

</div>


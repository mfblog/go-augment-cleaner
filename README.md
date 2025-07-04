# Augment 插件清理工具 

<div align="center">


**一款功能强大的 Augment 插件数据清理和 API 优化工具**

[![Go Version](https://img.shields.io/badge/Go-1.23+-blue.svg)](https://golang.org)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-green.svg)](#系统兼容性)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

</div>

## 📖 项目简介

Augment 插件清理工具是一款专业的多功能工具，集成了 **Augment 插件数据清理** 和 **API 域名优化** 两大核心功能。通过智能化的交互式菜单和丰富的命令行参数，为用户提供灵活、安全、高效的使用体验。

### 🎯 核心功能

- 🧹 **彻底清理** Augment 插件的所有跟踪数据
- 🚀 **API 域名测速** 和 hosts 文件优化
- 🌐 **代理支持** (Clash、V2Ray、自定义代理)
- 🎛️ **交互式主菜单** 和命令行双模式
- 🔒 **安全模式** 和干运行预览
- 📊 **详细报告** 和进度显示
- 🌍 **跨平台兼容** (Windows、macOS、Linux)

---

## ⚠️ 重要注意事项

### 🔴 使用前必读

| ⚠️ 警告类型 | 说明 |
|------------|------|
| **数据安全** | 清理操作不可逆，强烈建议创建备份 |
| **功能影响** | 插件需要重新初始化，可能需要重新登录 |
| **权限要求** | hosts 文件修改需要管理员权限 |
| **IDE 状态** | 清理前必须关闭所有 JetBrains IDE |

### 🖥️ 系统兼容性

| 操作系统 | 最低版本 | 支持状态 |
|----------|----------|----------|
| Windows | Windows 10+ | ✅ 完全支持 |
| macOS | macOS 10.14+ | ✅ 完全支持 |
| Linux | 主流发行版 | ✅ 完全支持 |

---

## � 快速开始

### 📦 安装和编译

#### 方式一：下载预编译版本

**Windows 系统：**
```cmd
# 下载 augment-cleaner-windows-amd64.exe
# 直接双击运行或在命令行中执行
.\augment-cleaner-windows-amd64.exe
```

**Linux 系统：**
```bash
# 下载 augment-cleaner-linux-amd64
# 添加执行权限（重要！）
chmod +x augment-cleaner-linux-amd64

# 运行程序
./augment-cleaner-linux-amd64
```

**macOS 系统：**
```bash
# 下载 augment-cleaner-darwin-amd64
# 添加执行权限（重要！）
chmod +x augment-cleaner-darwin-amd64

# 运行程序
./augment-cleaner-darwin-amd64
```

> ⚠️ **重要提示**: Linux 和 macOS 系统下载后必须先添加执行权限才能运行！



**Windows 系统：**
```cmd
# 直接运行
.\augment-cleaner.exe

# 或者使用 go run
go run .
```

**Linux/macOS 系统：**
```bash
# 添加执行权限（重要！）
chmod +x augment-cleaner

# 运行程序
./augment-cleaner

# 或者使用 go run
go run .
```

---

### 🎛️ 使用模式

本工具提供两种使用模式：

#### 1️⃣ 交互式主菜单模式（推荐）

直接运行程序，无需任何参数：

```bash
# Windows
.\augment-cleaner.exe

# Linux/macOS
./augment-cleaner
```

程序将显示美观的主菜单：

```
🎯 请选择要执行的操作：
┌─────────────────────────────────────────────────────────────┐
│                        主菜单                              │
├─────────────────────────────────────────────────────────────┤
│ 1. 🚀 只执行 API 测速和 hosts 优化                         │
│ 2. 🧹 只执行 Augment 插件清理                              │
│ 3. 🔄 执行完整流程（清理 + API 优化）                      │
│ 4. 🚪 退出程序                                             │
└─────────────────────────────────────────────────────────────┘
```

![Augment Logo](https://github.com/user-attachments/assets/fd697b25-649e-4ce8-988a-2ee5ccf02fb4)

#### 2️⃣ 命令行参数模式

适合自动化脚本和高级用户：

```bash
# 查看帮助
./augment-cleaner --help

# 只执行 API 优化
./augment-cleaner --api-only

# 只执行清理
./augment-cleaner --skip-api

# 干运行模式
./augment-cleaner --dry-run
```

---

## 📋 功能特性详解

### 🧹 Augment 插件清理功能

#### 支持的 IDE
| IDE | 支持状态 | 版本要求 |
|-----|----------|----------|
| IntelliJ IDEA | ✅ 完全支持 | 所有版本 |
| PyCharm | ✅ 完全支持 | 所有版本 |
| WebStorm | ✅ 完全支持 | 所有版本 |
| PhpStorm | ✅ 完全支持 | 所有版本 |
| RubyMine | ✅ 完全支持 | 所有版本 |
| CLion | ✅ 完全支持 | 所有版本 |
| DataGrip | ✅ 完全支持 | 所有版本 |
| GoLand | ✅ 完全支持 | 所有版本 |
| Rider | ✅ 完全支持 | 所有版本 |
| Android Studio | ✅ 完全支持 | 所有版本 |

#### 清理范围
- ✅ **配置文件**: options 目录中的 Augment 相关配置
- ✅ **插件数据**: 插件目录中的缓存和数据文件
- ✅ **项目数据**: .idea 目录中的 Augment 文件
- ✅ **缓存文件**: 各种临时和缓存文件
- ✅ **注册表项**: Windows 注册表中的相关项（仅 Windows）
- ✅ **用户数据**: .jetbrains 和 .augmentcode 目录

### 🚀 API 域名优化功能

#### 测速范围
- 🌐 测试 `d1.api.augmentcode.com` ~ `d20.api.augmentcode.com`
- ⚡ 并发测试，每个域名测试 3 次取平均值
- 📊 智能排序，显示最快的域名列表
- 🏆 自动选择前 5 个最快域名优化 hosts

#### 代理支持
| 代理类型 | 配置方式 | 说明 |
|----------|----------|------|
| Clash | `--proxy=clash` | 127.0.0.1:7890 |
| V2Ray | `--proxy=v2ray` | 127.0.0.1:1080 |
| 自定义 | `--proxy=custom:host:port` | 用户指定地址 |
| 无代理 | 默认或 `--proxy=none` | 直连模式 |

## �️ 命令行参数详解

### 清理相关参数

| 参数 | 说明 | 示例 |
|------|------|------|
| `-h, --help` | 显示帮助信息 | `./augment-cleaner --help` |
| `-v, --verbose` | 详细输出模式 | `./augment-cleaner -v` |
| `-d, --dry-run` | 干运行模式（预览操作） | `./augment-cleaner --dry-run` |
| `-s, --silent` | 静默模式（无交互） | `./augment-cleaner --silent` |
| `--unsafe` | 非安全模式（更彻底清理） | `./augment-cleaner --unsafe` |
| `--ide=NAME` | 只清理指定IDE | `./augment-cleaner --ide=PyCharm` |
| `--chat-only` | 只清理聊天记录 | `./augment-cleaner --chat-only` |
| `--keep-settings` | 保留用户设置 | `./augment-cleaner --keep-settings` |

### API 优化相关参数

| 参数 | 说明 | 示例 |
|------|------|------|
| `--api-only` | 只执行API测速和hosts优化 | `./augment-cleaner --api-only` |
| `--skip-api` | 跳过API优化步骤 | `./augment-cleaner --skip-api` |
| `--proxy=TYPE:ADDR` | 指定代理配置 | `./augment-cleaner --proxy=clash` |

### 代理配置格式

```bash
# Clash 代理
--proxy=clash

# V2Ray 代理
--proxy=v2ray

# 自定义代理
--proxy=custom:127.0.0.1:1080

# 不使用代理
--proxy=none
```

---

## 💡 使用示例

> 📝 **注意**: 以下示例中的 `./augment-cleaner` 在 Linux/macOS 系统下需要先执行 `chmod +x augment-cleaner` 添加执行权限

### 基础使用

```bash
# 1. 交互式主菜单（推荐新手）
./augment-cleaner

# 2. 查看帮助信息
./augment-cleaner --help

# 3. 干运行模式（安全预览）
./augment-cleaner --dry-run
```

### 清理功能示例

```bash
# 完整清理（推荐）
./augment-cleaner

# 只清理指定IDE
./augment-cleaner --ide=IntelliJIdea

# 只清理聊天记录
./augment-cleaner --chat-only

# 详细输出模式
./augment-cleaner --verbose

# 静默模式（适合脚本）
./augment-cleaner --silent --dry-run
```

### API 优化示例

```bash
# 只执行API优化
./augment-cleaner --api-only

# 使用Clash代理进行API优化
./augment-cleaner --api-only --proxy=clash

# 使用自定义代理
./augment-cleaner --api-only --proxy=custom:127.0.0.1:1080

# 干运行模式查看优化效果
./augment-cleaner --api-only --dry-run
```

### 组合使用示例

```bash
# 清理但跳过API优化
./augment-cleaner --skip-api

# 详细模式 + 干运行
./augment-cleaner --verbose --dry-run

# 只清理PyCharm + 详细输出
./augment-cleaner --ide=PyCharm --verbose

# 完整流程 + Clash代理（推荐）
./augment-cleaner  # 选择菜单选项3，然后选择Clash代理
```

## 📊 功能验证和效果检查

### � 清理效果验证

#### 自动验证
程序内置验证功能，会自动检查：
- ✅ 残留文件扫描
- ✅ 配置重置确认
- ✅ 清理统计报告
- ✅ 操作完整性检查

#### 手动验证方法

**Windows 系统：**
```cmd
# 检查配置目录
dir "%APPDATA%\JetBrains" /s | findstr augment

# 检查本地数据
dir "%LOCALAPPDATA%\JetBrains" /s | findstr augment

# 检查用户目录
dir "%USERPROFILE%\.augmentcode"
```

**Linux/macOS 系统：**
```bash
# 检查配置目录
find ~/.config/JetBrains -name "*augment*" 2>/dev/null

# 检查缓存目录
find ~/.cache/JetBrains -name "*augment*" 2>/dev/null

# 检查用户目录
ls -la ~/.augmentcode 2>/dev/null
```

### 🚀 API 优化效果验证

#### 测速结果示例
```
🏆 最快的域名排行榜 (前10名):
┌────┬─────────────────────────────────────┬──────────┬─────────────────┐
│排名│              域名                   │   延迟   │       IP        │
├────┼─────────────────────────────────────┼──────────┼─────────────────┤
│  1 │ d13.api.augmentcode.com             │ 298ms    │ 34.36.152.253   │
│  2 │ d14.api.augmentcode.com             │ 299ms    │ 35.190.75.54    │
│  3 │ d9.api.augmentcode.com              │ 300ms    │ 34.8.117.179    │
└────┴─────────────────────────────────────┴──────────┴─────────────────┘
```

#### hosts 文件检查
```bash
# Windows
type C:\Windows\System32\drivers\etc\hosts | findstr Augment

# Linux/macOS
cat /etc/hosts | grep Augment
```

---

## � 故障排除

### 常见问题及解决方案

#### 🚨 IDE 运行检测错误
```
❌ 问题：检测到 JetBrains IDE 正在运行
✅ 解决方案：
1. 完全关闭所有 JetBrains IDE
2. 检查任务管理器/活动监视器中的相关进程
3. 如有必要，重启计算机
```

#### 🔒 权限相关错误

**执行权限问题（Linux/macOS）：**
```
❌ 问题：Permission denied 或无法执行程序
✅ 解决方案：
chmod +x augment-cleaner        # 添加执行权限
./augment-cleaner               # 然后运行
```

**管理员权限问题：**
```
❌ 问题：无法修改 hosts 文件或删除某些文件
✅ 解决方案：
• Windows: 右键"以管理员身份运行"
• Linux/macOS: 使用 sudo 运行
  sudo ./augment-cleaner
• 检查文件是否被其他程序占用
```

#### 🌐 网络连接问题
```
❌ 问题：API 测速失败或连接超时
✅ 解决方案：
1. 检查网络连接
2. 尝试使用代理模式
3. 确认防火墙设置
4. 检查 DNS 设置
```

#### 📁 清理不完整
```
❌ 问题：仍有残留文件
✅ 解决方案：
1. 使用 --verbose 模式查看详细信息
2. 尝试 --unsafe 模式进行更彻底清理
3. 手动检查和删除残留文件
4. 重新运行清理程序
```

### 🆘 获取帮助

如果遇到其他问题：
1. 📖 查看 `--help` 获取详细参数说明
2. 🔍 使用 `--verbose` 模式获取详细日志
3. 🧪 使用 `--dry-run` 模式安全预览操作
4. 📝 查看生成的清理报告文件

---

## 📈 版本信息

### 当前版本：v3.4

#### 🆕 新增功能
- ✨ **交互式主菜单**: 用户友好的菜单驱动界面
- 🚀 **API 域名优化**: 集成域名测速和 hosts 优化
- 🌐 **代理支持**: 支持 Clash、V2Ray 和自定义代理
- 🎛️ **模块化设计**: 独立的 API 优化器模块
- 📊 **美化界面**: 丰富的图标和表格显示

#### 🔧 改进功能
- 🎯 **智能参数检测**: 自动识别命令行参数
- 📝 **详细进度提示**: 分步骤显示执行进度
- 🛡️ **增强错误处理**: 更好的错误提示和恢复
- 🎨 **界面优化**: 更美观的输出格式

#### 🐛 修复问题
- 修复跨平台兼容性问题
- 优化内存使用和性能
- 改进网络连接稳定性

---

## 📞 联系方式

### 公众号：煎饼果子卷AI





![PixPin_2025-07-04_15-21-54](https://github.com/user-attachments/assets/f90594a7-9624-49f3-846c-441b1f784c94)

<div align="center">
<table>
<tr>
<td align="center">
<b>个人微信</b><br>
<img src="https://github.com/user-attachments/assets/028ca832-7ae6-491f-8802-b2a4689260fd" width="250" alt="作者微信"><br>
<b>微信：JavaRookie666</b>
</td>
<td align="center">
<b>微信交流群</b><br>
<img src="img/qun-14.jpg" width="500" alt="WeChat"><br>
<small>二维码7天内(6月18日前)有效，过期请加微信</small>
</td>
<td align="center">
<b>微信赞赏</b><br>
<img src="https://github.com/user-attachments/assets/45674478-1ac8-4d4e-8ab0-a5c7fd4175d3" width="500" alt="微信赞赏码"><br>
<small>要到饭咧？啊咧？啊咧？不给也没事~ 请随意打赏</small>
</td>
<td align="center">
<b>支付宝赞赏</b><br>
<img src="https://github.com/user-attachments/assets/8e14d294-a549-43d7-b96d-d602de4939b4" width="500" alt="支付宝赞赏码"><br>
<small>如果觉得有帮助,来包辣条犒劳一下吧~</small>
</td>
</tr>
</table>
</div>

### 项目信息
- 🏠 **项目主页**: [GitHub Repository](https://github.com/yuaotian/go-augment-cleaner)
- 📄 **许可证**: MIT License
- 🏷️ **当前版本**: v3.4
- 🛠️ **Go 版本要求**: 1.23+

---

<div align="center">

**感谢使用 Augment 插件清理工具！**

如果这个工具对您有帮助，请考虑给项目一个 ⭐ Star

</div>

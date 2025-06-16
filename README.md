# go-augment-cleaner
清理Augment缓存和生成设备SessionId

Augment插件清理工具是一套专门设计的工具集，用于彻底清理Augment插件的所有跟踪数据，让插件以为运行在全新的环境中。工具包含多个版本以适应不同的使用场景和技术水平。

## 公众号：煎饼果子卷AI 


## ⚠️ 重要注意事项

### 使用前必读

1. **数据安全**
   - 清理操作不可逆
   - 强烈建议创建备份
   - 重要项目请额外备份

2. **功能影响**
   - 插件需要重新初始化
   - 可能需要重新登录
   - 个性化设置会丢失

3. **系统兼容性**
   - 支持Windows 10+
   - 支持macOS 10.14+
   - 支持主流Linux发行版

---


## 📖 详细使用说明

### 使用前准备

1. **关闭IntelliJ IDEA**
   ```
   确保所有IntelliJ IDEA进程都已关闭
   工具会自动检测并提示
   ```

2. **备份重要数据**（可选但推荐）
   ```
   工具提供自动备份功能
   备份文件保存在用户目录下
   ```

3. **确认清理范围**
   ```
   工具会显示将要清理的文件列表
   用户可以选择性确认
   ```

### Go程序详细使用

#### 基本用法
```bash
# 默认模式：安全清理 + 自动备份
./augment-cleaner-linux-amd64

# 查看帮助
./augment-cleaner-linux-amd64 -h
```
#### Windows
```cmd
augment-cleaner-windows-amd64.exe
```

#### Linux
```bash
./augment-cleaner-linux-amd64
```

#### macOS
```bash
./augment-cleaner-darwin-amd64
```
![PixPin_2025-06-16_15-56-51](https://github.com/user-attachments/assets/e2006cd0-4c05-4a88-a790-f6e481bf7139)


#### 高级选项
```bash
# 干运行模式（只显示将要清理的文件，不实际删除）
./augment-cleaner-linux-amd64 -dry-run

# 禁用备份（不推荐）
./augment-cleaner-linux-amd64 -no-backup

# 非安全模式（清理更彻底，但风险更高）
./augment-cleaner-linux-amd64 -unsafe

# 静默模式（无交互）
./augment-cleaner-linux-amd64 -silent
```

#### 组合使用
```bash
# 先查看将要清理什么
./augment-cleaner-linux-amd64 -dry-run

# 确认后执行实际清理
./augment-cleaner-linux-amd64
```
---

## 📋 清理范围

### 完全清理的数据类型

✅ **设备标识数据**
- PermanentInstallationID相关配置
- SessionID和会话数据
- 用户代理字符串缓存

✅ **配置文件**
- PropertiesComponent中的Augment设置
- IDE选项文件中的相关配置
- 插件状态和偏好设置

✅ **缓存和临时文件**
- 本地索引缓存
- Blob状态文件
- 临时处理文件

✅ **日志和跟踪数据**
- 操作日志文件
- 错误和异常记录
- Sentry监控数据

✅ **项目级数据**
- .idea目录中的Augment文件
- 项目特定的配置和缓存
- 记忆和上下文数据


---

## 📊 清理效果验证

### 验证方法

1. **自动验证**
   ```
   工具内置验证功能
   检查残留文件
   验证配置重置
   ```

2. **手动验证**
   ```bash
   # 检查配置目录
   ls -la ~/.config/JetBrains/IntelliJIdea*/options/
   
   # 搜索残留文件
   find ~ -name "*augment*" 2>/dev/null
   
   # 检查进程
   ps aux | grep augment
   ```

3. **IDE验证**
   ```
   重启IntelliJ IDEA
   检查插件状态
   验证是否需要重新登录
   确认功能正常
   ```

### 成功标志

✅ **完全清理成功**
- 无残留配置文件
- 插件状态重置
- 需要重新初始化
- 生成新的SessionID

✅ **部分清理成功**
- 主要数据已清理
- 少量无关紧要的残留
- 插件功能正常
- 达到预期效果

❌ **清理失败**
- 大量文件未清理
- 插件状态未改变
- 仍使用旧的SessionID
- 需要重新清理

---

---

## 🔍 故障排除

### 常见问题

#### 1. "IDE正在运行"错误
```
问题：工具检测到IntelliJ IDEA正在运行
解决：
1. 完全关闭IntelliJ IDEA
2. 检查任务管理器中的相关进程
3. 重启计算机（如果进程无法关闭）
```

#### 2. 权限不足错误
```
问题：无法删除某些文件
解决：
1. 以管理员身份运行（Windows）
2. 使用sudo运行（Linux/macOS）
3. 检查文件是否被其他程序占用
```

#### 3. 备份失败
```
问题：无法创建备份
解决：
1. 检查磁盘空间
2. 确认备份目录权限
3. 手动创建备份目录
```

#### 4. 清理不完整
```
问题：仍有残留文件
解决：
1. 运行验证功能
2. 手动检查残留文件
3. 使用非安全模式重新清理
```

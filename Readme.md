# mac常用

通过 `Brewfile` 快速恢复或同步 macOS，一键安装所有依赖工具。

---

## 📦 用途

- ​**快速恢复环境**：在新设备或系统重装后，快速安装所有工具。
- ​**版本化管理**：跟踪工具版本变化，方便回滚和审计。

---

## 🛠️ 安装方法

### 前置条件
- ​**系统要求**：macOS 10.13+
- ​**Homebrew**：确保已安装 [Homebrew](https://brew.sh)

### 一键安装
```bash
# 克隆本仓库
git clone https://github.com/shinwu/homebrew-config
cd homebrew-config

# 使用 Homebrew Bundle 安装所有依赖
brew bundle install
```

---

## 🔄 更新方法

更新本地 Brewfile
若你修改了环境配置（如新增/删除软件），运行以下命令更新 Brewfile：
```bash
# 强制覆盖当前 Brewfile
brew bundle dump --force
```

同步远程仓库
```bash
git add Brewfile
git commit -m "更新开发环境依赖"
git push origin main
```

---

## ⚠️ 注意事项

### 1. ​权限问题：
* 安装过程中可能需要输入密码（如 sudo 权限）。
### 2. 网络要求：
* 国内用户建议配置 Homebrew 镜像源 加速下载。

---

## 🧩 扩展用法

### 选择性安装
仅安装指定类别的工具（需提前拆分 Brewfile）：

```bash
# 示例：仅安装编程语言工具
brew bundle --file Brewfile-languages
```

### 清理旧版本
安装完成后清理过时版本：
```bash
brew cleanup
```

---

## 📜 开源协议

本项目采用 MIT License，可自由修改和分发。

---

## 🤝 贡献指南

欢迎通过 Issue 或 Pull Request 提交改进建议！

---

*_✨ 提示：使用前请仔细阅读 Brewfile 内容，确认需要安装的工具列表。_*

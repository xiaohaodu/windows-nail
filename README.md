# Windows Nail - Windows 窗口置顶工具

一个简单易用的 Windows 窗口置顶工具，帮助您快速将任意窗口置顶显示。

## ✨ 特性

- 🖥️ **窗口置顶** - 快速将任意窗口设置为置顶状态
- 🎯 **精准选择** - 支持通过窗口标题或鼠标位置选择窗口
- 📋 **窗口列表** - 显示所有可操作的窗口列表
- 🚀 **原生性能** - 使用 C++ Node.js 扩展实现高性能操作
- 💡 **Electron 包装** - 友好的图形用户界面

## 🛠️ 技术栈

- **C++ Node.js 扩展** - 核心窗口操作功能
- **Node-API (N-API)** - Node.js 原生模块接口
- **Electron** - 跨平台桌面应用框架
- **Electron Forge** - 应用构建和打包工具

## 📦 安装

### 环境要求

- Windows 操作系统
- Node.js (建议 v16 或更高版本)
- Python 3.x (用于 node-gyp 编译)
- Visual Studio Build Tools (用于 C++ 编译)

### 克隆项目

```bash
git clone https://github.com/xiaohaodu/windows-nail.git
cd windows-nail
```

### 安装依赖

```bash
npm install
```

安装过程会自动编译 C++ 扩展。

## 🚀 使用

### 开发模式

```bash
npm start
```

### 打包应用

```bash
npm run package
```

### 构建安装包

```bash
npm run make
```

### 发布到 GitHub

```bash
# 发布正式版
npm run publish-production

# 发布测试版
npm run publish-beta
```

## 📖 API 功能

### 核心功能

- `switchWindowTopmostByTitle(title, isTopmost)` - 通过窗口标题设置置顶
- `switchWindowTopmostByHWND(hwnd, isTopmost)` - 通过窗口句柄设置置顶
- `getAllWindowsInfo()` - 获取所有窗口信息
- `getForegroundWindowAtPosition(x, y)` - 获取指定位置的窗口

## 📁 项目结构

```
windows-nail/
├── node/                    # C++ 扩展源代码
│   ├── window_nail.cc      # 主扩展实现
│   ├── index.js            # Node.js 入口
│   ├── CMakeLists.txt      # CMake 构建配置
│   ├── test/               # 测试代码
│   └── third_party/        # 第三方库
│       ├── LOG/            # 日志模块
│       └── WINDOWINFO/     # 窗口信息模块
├── src/                     # Electron 应用源代码
├── package.json             # 项目配置
├── forge.config.js          # Electron Forge 配置
├── binding.gyp              # node-gyp 构建配置
└── README.md               # 项目文档
```

## 🤝 贡献

欢迎提出 Issue 和 Pull Request！

如有新需求，可联系微信：18713908616（请注明来意）

## 📄 许可证

ISC License

## 👤 作者

Du-XiaoHao

# RoboMaster 视觉算法组培训项目

这个仓库用于记录视觉算法组培训中的练习。目前包含一个最小的 C++/CMake 示例，后续练习建议按主题分目录，并为每个程序添加独立的 CMake target。

## 环境要求

- CMake 3.16 或更高版本
- 支持 C++17 的 C++ 编译器
- （可选）使用 VS Code 调试时需要安装 C/C++ 扩展和 GDB

## 构建和运行

在仓库根目录执行：

```bash
cmake -S . -B build
cmake --build build
./build/cmake_1st
```

程序会输出 `HELLO CMAKE`。`build/` 是本机生成目录，不需要提交到 Git。

## 项目结构

```text
.
├── .github/workflows/   # GitHub Actions 构建检查
├── .vscode/             # 可共享的 VS Code 编辑与调试配置
├── cmake_1st.cpp        # 第一个 C++ 示例
├── CMakeLists.txt       # CMake 项目和构建目标
└── CONTRIBUTING.md      # 分支、提交和代码约定
```

## 参与练习

开始新练习前，先阅读 [CONTRIBUTING.md](CONTRIBUTING.md)，并从 `main` 创建自己的主题分支。提交前至少完成一次本地构建；对 `main` 的修改通过 GitHub Pull Request 合并。

## 许可

仓库目前没有附带开源许可证。公开仓库前，请确认是否要添加许可证，以及是否允许他人使用和再分发代码。

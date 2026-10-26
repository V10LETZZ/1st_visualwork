# 贡献与 Git 约定

## 分支与合并

- `main` 保持可构建；不要直接在 `main` 上开发。
- 每项练习使用单独分支，例如 `feature/camera-calibration` 或 `learning/first-cmake`。
- 完成后推送分支，并通过 Pull Request 合并到 `main`。PR 描述要说明改动内容和验证方式。

```bash
git switch main
git pull --ff-only
git switch -c feature/your-topic
# 修改并验证代码
git add <files>
git commit -m "feat: add your topic"
git push -u origin feature/your-topic
```

## 提交信息

提交标题使用简短的 `type: description` 格式。常用类型：

- `feat`: 新练习或新功能
- `fix`: 修复错误
- `docs`: 文档修改
- `build`: 构建系统或依赖修改
- `refactor`: 不改变行为的代码整理

示例：`build: fix CMake executable target`。

## C++ 与构建

- 使用 C++17；缩进为 4 个空格，文本文件使用 UTF-8 和 LF 换行。
- 保持编译器警告开启，并修复本次改动引入的警告。
- 新增源文件时，将它明确添加到对应的 CMake target；不要提交 `build/` 等构建产物。
- 提交前在仓库根目录运行：

  ```bash
  cmake -S . -B build
  cmake --build build
  ```

GitHub Actions 会在推送到 `main` 和针对 `main` 的 Pull Request 上运行构建检查。

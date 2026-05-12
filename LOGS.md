# 阶段一：环境攻坚实录

### 1. 跨平台尝试
我最初在 **Windows** 上进行调试，遇到的第一个下马威是 `pip` 权限问题。
- **报错：** 'pip' is not recognized as an internal or external command.
- **解决：** 我深入研究了系统环境变量，手动将 Python 的 Scripts 目录添加到了 Path 中。

### 2. Ubuntu 迁移
为了让程序 24 小时运行，我转向了 **Ubuntu**。
- 在 Linux 环境下，我学会了如何使用 `git clone` 获取源码，并处理了 Linux 下的权限问题（chmod）。
- 重点研究了 `requirements.txt` 的安装顺序，确保每一个依赖库都精准匹配。

### 3. JSON 配置的“像素级”排查
这是最考验耐心的一步。我反复修改了 `config.json`：
- **挑战：** 只要少一个双引号，程序就会报 `JSONDecodeError`。
- **研究：** 我学会了使用代码编辑器的 JSON 插件来辅助检查语法，并最终理顺了 OpenAI 和 Telegram 的鉴权逻辑。

# 📦 TMUX 配置文件（适用于 Ubuntu + oh-my-zsh）

A modern and practical `tmux` configuration tailored for **Ubuntu + oh-my-zsh** users, with support for:

- Mouse scrolling
- Clipboard integration via `xclip`
- Vim-style navigation in copy mode
- A clean and informative status bar
- Auto zsh shell and pane switching

---

## 🧩 功能 Features

### ✅ 中文说明

- 使用 `Ctrl + a` 作为 tmux 前缀，更符合直觉
- 启用鼠标支持：滚动、点击 pane、选择窗口
- 支持 vi 键风格复制：`v` 选中，`y` 复制到系统剪贴板
- 增强状态栏：显示 session 名、时间、颜色更清晰
- 分屏控制快捷键（`Ctrl + ↑↓←→`）
- 使用 zsh 作为默认 shell（适配 oh-my-zsh）
- 支持自动启动 tmux 会话（需搭配 `.zshrc`）

### ✅ English Summary

- Uses `Ctrl + a` as tmux prefix (more intuitive)
- Mouse support: scroll, pane click, window select
- Vi-style copy mode with clipboard sync via `xclip`
- Enhanced status bar with session name & time
- Easy pane navigation (`Ctrl + arrows`)
- zsh as the default shell (perfect for oh-my-zsh users)
- Optional: auto-start tmux on terminal login

---

## ⚙️ 安装 Installation

### 1. 安装依赖 Install Dependencies

```bash
sudo apt update
sudo apt install tmux xclip zsh

## 🖥️ 可选配置：自动进入 tmux（推荐）
在你的 ~/.zshrc 文件末尾添加以下内容：

```
if command -v tmux &> /dev/null && [ -z "$TMUX" ]; then
  tmux attach -t default || tmux new -s default
fi
```
每次打开终端时会自动进入上次的 tmux 会话，或新建一个名为 default 的会话。

🧪 使用 Usage Tips
- 复制模式：Ctrl + a 然后 [ 进入，使用 v 开始选择，y 复制（自动复制到系统剪贴板）

- 分屏操作：

- 垂直分屏：Ctrl + a 然后 %

- 水平分屏：Ctrl + a 然后 "

- pane 切换：按住 Ctrl + 方向键

- 退出 tmux：

- 输入 exit 或按 Ctrl + d，关闭当前 pane

- 或执行：tmux kill-session -t session_name

## 📄 License
MIT License. Free to use and customize.

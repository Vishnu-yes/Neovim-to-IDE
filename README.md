---

SunVim (Your Pocket IDE)

🚀 A clean, IDE-style Neovim configuration built on top of lazy.nvim.
Designed for developers who want a polished coding experience without bloat.
Especially friendly for arm64 users by avoiding mason.nvim and supporting manual LSP installs.


---
This Whole SunVim.zip is divided into three Child Folders of lua
You have full controls over plugins. 
This wont break until you did something wrong with init.lua or any User/ , simply user folder files.
Make sure to Scroll a little down to learn how to Clone and How to Clone efficiently without breaking anything!
```Bash
❯ tree ~/.config/nvim
/data/data/com.termux/files/home/.config/nvim
├── init.lua
├── lazy-lock.json
└── lua
    └── user
        ├── Basics
        │   ├── autoreload.lua
        │   ├── env.lua
        │   ├── mappings.lua
        │   ├── options.lua
        │   ├── plugins.lua
        │   └── utilities.lua
        ├── UI
        │   ├── DAP_UI.lua
        │   ├── IBL.lua
        │   ├── bufferline.lua
        │   ├── dashboard.lua
        │   ├── diagonasticsigns.lua
        │   ├── gitsigns.lua
        │   ├── statusline.lua
        │   └── ui.lua
        └── config
            ├── autopairs.lua
            ├── cmp.lua
            ├── custom
            │   ├── harpoon.lua
            │   ├── refactoring.lua
            │   ├── sessions.lua
            │   ├── todo.lua
            │   └── trouble.lua
            ├── formattor.lua
            ├── lsp.lua
            ├── notify.lua
            ├── nvimtree.lua
            ├── sessions.lua
            ├── telescope.lua
            ├── toggleterm.lua
            └── workspace.lua
```
---

📖 SunVim Installation Guide

Welcome to SunVim — a lightweight, single-file Neovim IDE config (400+ lines, as of September 2025).
This guide will help you install safely without breaking your existing setup.


---

⚠️ Before You Begin

Backup is mandatory – never skip this step.

You can test SunVim without overwriting your current config using NVIM_APPNAME.

Works best with Neovim 0.11.4 (future versions may require adjustments).



---

📦 Step 1 – Backup Your Current Config

# Backup your Neovim config
cp -r ~/.config/nvim ~/nvim-backup-$(date +%Y%m%d)

# (Optional) also backup plugin data
cp -r ~/.local/share/nvim ~/nvim-data-backup-$(date +%Y%m%d)


---

🧹 Step 2 – Clean Old Config (Optional)

⚠️ Do this only if you want to fully replace your config.
If you just want to test SunVim safely, skip this and see “Safe Install” below.

rm -rf ~/.config/nvim
rm -rf ~/.local/state/nvim
rm -rf ~/.local/share/nvim


---

📥 Step 3 – Download & Install SunVim

Option A: Safe Install (Recommended)

Run Neovim with a custom config name so your old setup stays intact:

# Create a SunVim folder
mkdir -p ~/.config/sunvim

# Download SunVim.zip
curl -L -o ~/SunVim.zip https://github.com/Vishnu-yes/Neovim-to-IDE/raw/main/SunVim.zip

# Extract into the SunVim config folder
unzip ~/SunVim.zip -d ~/.config/sunvim

# Launch Neovim with SunVim
NVIM_APPNAME=sunvim nvim

Option B: Full Replace

# Download SunVim.zip
curl -L -o ~/SunVim.zip https://github.com/Vishnu-yes/Neovim-to-IDE/raw/main/SunVim.zip

# Extract into Neovim config folder
unzip ~/SunVim.zip -d ~/.config/nvim

# Launch Neovim
nvim


---

▶️ Step 4 – Plugin Setup

Start Neovim and wait for lazy.nvim to install plugins automatically.


---

🔧 Step 5 – Install LSP Servers (Manually)

Mason is not included. Install language servers yourself:

# JavaScript / TypeScript
npm i -g typescript typescript-language-server

# Python
pipx install pyright-langserver  # or
npm i -g pyright

# C / C++
sudo apt install clangd

👉 After installation, configure LSP paths in IDE.lua.


---

🎨 Themes

Switch themes easily:

:colorscheme <Tab>

Use arrow keys to cycle, then press Enter.


---

⚠️ Notes

Deprecated API warnings may appear — they don’t break Neovim.

SunVim is designed for Neovim 0.11.4.

The config is easy to edit since it’s just one file.



---

✅ Uninstall / Revert

To restore your old setup:

rm -rf ~/.config/nvim
cp -r ~/nvim-backup-YYYYMMDD ~/.config/nvim

---

Features --------->

✨ Highlights

⚙️ Plugin Management

lazy.nvim – modern, fast plugin manager.
→ Ensures smooth lazy-loading and minimal startup time.

Full Control of Plugins/UI/Basics


🎨 UI & Themes

Multiple top-notch color schemes: Gruvbox, Catppuccin, Tokyonight, OneDark, Kanagawa, Nord, VSCode theme and more.

Bufferline.nvim – tab-like buffers for quick navigation.

Lualine.nvim – beautiful statusline with devicons.

Indent Blankline – clean indentation guides.

Better gutter icons for diagnostics & Git.


📂 File & Project Management

Nvim-tree – file explorer with devicons.

Workspaces.nvim – manage multiple project roots.

Auto-session – automatically save & restore sessions.


🔍 Navigation & Search

Telescope.nvim – fuzzy finder for files, buffers, help, grep, and file browser.

Quick project-wide search with live grep.


💻 Coding Assistance

Treesitter – advanced syntax highlighting & parsing.

Native LSP – manual setup (no Mason), supports pyright, clangd, tsserver, lua-language-server, etc.

nvim-cmp – autocompletion engine with snippets (LuaSnip), buffer, path, and LSP sources.

nvim-autopairs – automatic closing of brackets, quotes, etc.

Conform.nvim – automatic code formatting.


🐛 Debugging

nvim-dap – Debug Adapter Protocol client.

nvim-dap-ui – debugging UI with REPL, breakpoints, and step controls.



---

⌨️ Command Cheat Sheet

🔍 Telescope

Keymap	Action

<leader>ff	Find Files
<leader>fg	Live Grep
<leader>fb	Find Buffers
<leader>fh	Help Tags
<leader>fe	File Browser


📂 File Explorer

Keymap	Action

<leader>e	Toggle File Explorer


⚡ LSP

Keymap	Action

gd	Go to Definition
K	Hover Docs
gr	References
<leader>rn	Rename
<leader>ca	Code Action


🐛 Debugging (DAP)

Keymap	Action

<F5>	Start/Continue Debugging
<F10>	Step Over
<F11>	Step Into
<F12>	Step Out
<leader>db	Toggle Breakpoint
<leader>dr	Open REPL


📦 Sessions & Workspaces

Keymap	Action

<leader>pw	Open Workspaces
<leader>ps	Save Session
<leader>pr	Restore Session



---

🌟 Why This Config?

No Mason → ARM64 friendly & portable (manual LSP setup).

Fast → Uses lazy.nvim with lazy-loading.

IDE Features → Git, debugging, formatting, autocompletion, and themes in one place.

Customizable → Edit the plugin tables in IDE.lua to add/remove plugins easily.


~Config Generated with months of efforts done by Chatgpt/Claude.
Onece this cobfig was more than 900+ lines but Chatgpt made it small with many unique features.
~This config was created to get the experience of IDE for Termux/Arm64/Aarch64 terminals.
~Some themes may feel broken as most of them are desgined for simplicity, use the modern themes for better modern Support. 
#Jay Jagannath Ji!
---

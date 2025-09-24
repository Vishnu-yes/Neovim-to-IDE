---

Neovim IDE Config (IDE.lua)

🚀 A clean, IDE-style Neovim configuration built on top of lazy.nvim.
Designed for developers who want a polished coding experience without bloat.
Especially friendly for arm64 users by avoiding mason.nvim and supporting manual LSP installs.


---

✨ Highlights

⚙️ Plugin Management

lazy.nvim – modern, fast plugin manager.
→ Ensures smooth lazy-loading and minimal startup time.


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

📦 Installation
! Backup your current configs via 
``` bash
cp ~/.configs/nvim/init.lua ~/YourBacupFolder/
```
! Make sure to run these command one by one 
Only for Linux/MacOs (⚠️ If Not then Don't Try this!)
``` bash
rm -rf ~/.config/nvim
rm -rf ~/.local/state/nvim
rm -rf ~/.local/share/nvim
```
1. Clone this repo into your Neovim config folder:

```bash
git clone https://github.com/Vishnu-yes/Nvim-to-IDE ~/.config/nvim
```

2. Start Neovim and let lazy.nvim install plugins.


3. Install LSP servers manually (no Mason):
``` bash
npm i -g pyright typescript typescript-language-server
sudo apt install clangd
pipx install pyright-langserver
```
Then configure server paths inside IDE.lua.




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



---

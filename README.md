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
1. Download this IDE.lua file into your Neovim config folder:
Remember I created this for Nvim 0.11.4 for further versions I will work.
```bash
#make sure you have curl!
curl -o ~/.config/nvim/init.lua https://raw.githubusercontent.com/Vishnu-yes/Neovim-to-IDE/main/IDE.lua

#wget
wget -O ~/.config/nvim/init.lua https://raw.githubusercontent.com/Vishnu-yes/Neovim-to-IDE/main/IDE.lua
```

⚠️ You may see some warnings of Deprecated things don't worry they are normal won't break your nvim. 
Use Ai or Professionals to get rid of the problem. But as of now even Claude and Chatgpt are using same type of deprecated things that's why You have to wait some months even years to get rid of those errors. 

⚠️ Don't worry you are free to manipulate this config as it is just a single file and only 400+ lines of code (September, 2025 )

⚠️ You can easily change themes via esc + : + colorscheme + tab key  + Left/Right keys for toggling up and down + Enter 
2. Start Neovim and let lazy.nvim install plugins.


3. Install LSP servers manually (no Mason):
``` bash
npm i -g pyright typescript typescript-language-server
sudo apt install clangd
pipx install pyright-langserver
```
Then configure server paths inside IDE.lua.
Yeah you have to configure according to your Version 
1st Download the Lsps etc and paste them in Lsp sections.
You must Use Ai for any edit. 




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


~Config Generated with months of efforts done by Chatgpt/Claude. Onecd this cobfig was more than 900+ lines but Chatgpt made it small with many unique features.
~This config was created to get the experience of IDE for Termux/Arm64/Aarch64 terminals.
~Some themes may feel broken as theybare desgined for simplicity, use the modern themes for better modern Support. 
#Jay Jagannath Ji!
---

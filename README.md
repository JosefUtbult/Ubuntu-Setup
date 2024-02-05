# Ubuntu Setup

## Settings

Open settings.

Change `Appearance` to dark, and keep the orange color.

Under the `Dock` section, select `Auto-hide Dock`

Under `Keyboard Shortcuts` change the following

- `Launch Teminal` - `Super+Return`
- `Launch web browser` - `Shift+Super+Return`
- `Move to workspace on the left` - `Ctrl+Super+Left`
- `Move to workspace on the right` - `Ctrl+Super+Right`
- `Move window one workspace to the left` - `Shift+Ctrl+Super+Left`
- `Move window one workspace to the right` - `Shift+Ctrl+Super+Right`
- `Close window` - `Shift+Super+Q`
- `Maximize window` - `Shift+Super+Space`

Under `Accessibility` disable animations

## Gnome Tweaks

Install `gnome-tweaks`

```bash
sudo apt install -y gnome-tweaks
```

Open `Tweaks`. Under `Keyboard & Mouse > Additional Layout Options > Caps Lock behaviour` set it to `Make Caps Lock an additional Esc but Shift + Caps Lock is the regular Caps Lock`

## NeoVim

Follow [this guide](https://github.com/JosefUtbult/neovim-config)

## ZSH

Follow [this guide](https://github.com/JosefUtbult/Zsh-Setup)

## TMUX

Follow [this guide](https://github.com/JosefUtbult/tmux-config)

## LazyGit

Install [LazyGit](https://github.com/jesseduffield/lazygit#ubuntu) using the following command

```bash
LAZYGIT_VERSION=$(curl -s "https://api.github.com/repos/jesseduffield/lazygit/releases/latest" | grep -Po '"tag_name": "v\K[^"]*')
cd ~/Downloads
curl -Lo lazygit.tar.gz "https://github.com/jesseduffield/lazygit/releases/latest/download/lazygit_${LAZYGIT_VERSION}_Linux_x86_64.tar.gz"
tar xf lazygit.tar.gz lazygit
sudo install lazygit /usr/local/bin
```

Then, add an alias to your `.zshrc` config

```bash
# Alias LazyGit
alias g=lazygit
```

## QuteBrowser

Install the browser

```bash
sudo apt install -y qutebrowser
```

Copy the config file to `.config/qutebrowser`

```bash
cp qutebrowser/config.py ~/.config/qutebrowser
```

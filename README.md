# 🚀 macOS Development Environment Setup

A comprehensive guide to setting up a modern, productive development environment on macOS with a beautiful terminal, powerful tools, and essential applications.

## 📋 Table of Contents

- [Quick Start](#-quick-start)
- [Prerequisites](#-prerequisites)
- [Core Tools](#-core-tools)
- [Terminal Enhancement](#-terminal-enhancement)
- [Development Applications](#-development-applications)
- [Additional Resources](#-additional-resources)

## 🏁 Quick Start

1. **Clone this repository:**
   ```bash
   git clone https://github.com/salesawagner/configs.git ~/.config
   ```

2. **Open the workspace(need vscode):**
   ```bash
   open ~/.config/config.code-workspace
   ```

## 🔧 Prerequisites

### Essential Package Manager
Install [Homebrew](https://brew.sh) - The missing package manager for macOS:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

**Batch Installation with Brewfile:**
This repository includes a `Brewfile` that allows you to install multiple packages at once:
```bash
brew bundle --file=~/.config/Brewfile
```

### Development Environment
- **Xcode**: [Download from official site](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://apps.apple.com/br/app/xcode)
- **Visual Studio Code**: [Download from official site](https://code.visualstudio.com/download)
- **Ruby**: Required for various CLI tools
  ```bash
  brew install ruby
  ```
  > **Note:** If you used `brew bundle` above, Ruby is already installed and you can skip this step.

## 🛠 Core Tools

### SSH Configuration
Set up SSH keys for secure GitHub access:
- Follow the [official GitHub guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) for generating SSH keys

### iOS Development
Install [CocoaPods](https://cocoapods.org) for iOS dependency management:
```bash
brew install cocoapods
```
> **Note:** If you used `brew bundle` above, CocoaPods is already installed and you can skip this step.

## 🎨 Terminal Enhancement

### 1. Oh My Zsh Framework
Install [Oh My Zsh](https://ohmyz.sh) for an enhanced shell experience:
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### 2. Spaceship Prompt Theme
Install the beautiful [Spaceship](https://spaceship-prompt.sh) theme:

**Installation:**
```bash
git clone https://github.com/spaceship-prompt/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
```

**Create symlink:**
```bash
ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
```

**Activation:**
Set `ZSH_THEME="spaceship"` in your `.zshrc` file.

**Configuration:**
Add this line at the end of your `~/.zshrc` file to load custom configurations:
```bash
source "$HOME/.config/.myzsh.zsh"
```

### 3. Essential Zsh Plugins

#### Auto-suggestions
[zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions) - Fish-like autosuggestions:
```bash
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

#### Syntax Highlighting
[zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting) - Real-time syntax highlighting:
```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```

#### Fast Syntax Highlighting
[fast-syntax-highlighting](https://github.com/zdharma-continuum/fast-syntax-highlighting) - Enhanced syntax highlighting:
```bash
git clone https://github.com/zdharma-continuum/fast-syntax-highlighting.git $ZSH_CUSTOM/plugins/fast-syntax-highlighting
```

#### Auto-complete
[zsh-autocomplete](https://github.com/marlonrichert/zsh-autocomplete) - Real-time type-ahead autocompletion:
```bash
git clone https://github.com/marlonrichert/zsh-autocomplete.git $ZSH_CUSTOM/plugins/zsh-autocomplete
```

### 4. Dracula Theme
Install the elegant [Dracula theme](https://draculatheme.com/terminal) for Terminal:

**Installation:**
```bash
git clone https://github.com/dracula/terminal-app.git ~/.config/dracula-theme
```

**Setup Instructions:**
1. Open **Terminal** → **Settings**
2. Navigate to **Profiles** tab
3. Click the **"..."** button under the themes list
4. Select **Import...**
5. Choose `~/.config/dracula-theme/Dracula.terminal`
6. Set as **Default**

### 5. Nerd Fonts
Install [Hack Nerd Font](https://www.nerdfonts.com/font-downloads) for icon support:

**Installation:**
```bash
brew install --cask font-hack-nerd-font
```
> **Note:** If you used `brew bundle` above, Hack Nerd Font is already installed and you can skip this step.

**Terminal Configuration:**
Navigate to **Settings** → **Profiles** → **Text** → Select **Hack Nerd Font Retina**

Install [Fira Code Nerd Font](https://www.nerdfonts.com/font-downloads) for icon support:

**Installation:**
```bash
brew install --cask font-fira-code-nerd-font
```
> **Note:** If you used `brew bundle` above, Hack Nerd Font is already installed and you can skip this step.

### 6. Colorls
Enhanced `ls` command with colors and icons using [colorls](https://github.com/athityakumar/colorls):

**Installation:**
```bash
sudo gem install colorls
```

**Dracula Theme for Colorls:**
```bash
git clone git@github.com:dracula/colorls.git ~/.config/colorls
```

**Useful Aliases:**
Add these to your `.aliases.zsh`:
```bash
alias ls='colorls --sort-dirs -1'
alias lc='colorls -lA --sd'
```

## 🎨 IDEs Enhancement
- **[Dracula for Xcode](https://draculatheme.com/xcode)**
   ```bash
   brew tap dracula/install
   brew install --cask dracula-xcode
   ```
   > **Note:** If you used `brew bundle` above, Hack Nerd Font is already installed and you can skip this step.

   ### Activating theme
   1. Xcode > Preferences > Themes;
   2. Select the Dracula Theme;
   3. Select Fira code font

- **[Dracula for VSCode](https://draculatheme.com/visual-studio-code)**
   ### Install using Command Palette
   1. Go to `View -> Command Palette` or press `Ctrl+Shift+P`
   2. Then enter `Install Extension`
   3. Write `Dracula Official`
   4. Select it or press Enter to install
   5. Install Fira Code Font: [link](https://github.com/tonsky/FiraCode/wiki/VS-Code-Instructions)

## 💻 Development Applications

### Essential Tools
- **[GitKraken](https://www.gitkraken.com)** - Git GUI client
- **[Proxyman](https://proxyman.com)** - HTTP debugging proxy
- **[Postman](https://www.postman.com/downloads/)** - API development platform

### System Utilities
- **[Dell Display and Peripheral Manager](https://www.dell.com/support/product-details/pt-br/product/dell-display-peripheral-manager/drivers)** - Display management
- **[DisplayLink Manager](https://www-synaptics-com.translate.goog/products/displaylink-graphics/downloads/macoshttps://www.synaptics.com/products/displaylink-graphics/downloads/macos)** - Multi-monitor support
- **[MacDown](https://macdown.uranusjr.com)** - Markdown editor
- **[The Unarchiver](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://apps.apple.com/br/app/the-unarchiver)** - Archive utility

### Development Environments
- **[Python](https://packaging.python.org/en/latest/tutorials/installing-packages/)** - Programming language

## 📚 Additional Resources

### Helpful Guides
- [Terminal customization guide](https://gist.github.com/n1snt/454b879b8f0b7995740ae04c5fb5b7df)
- [RocketSeat terminal setup (PT-BR)](https://www.rocketseat.com.br/blog/artigos/post/terminal-com-oh-my-zsh-spaceship-dracula-e-mais)
- [macOS terminal improvements](https://manuelrdsg.github.io/2018/10/improving-the-look-of-your-macos-terminal/)
- [Oh My Zsh productivity tips (PT-BR)](https://www.alura.com.br/artigos/oh-my-zsh-melhorando-produtividade-terminal)

---

**Note:** This setup creates a beautiful, functional development environment optimized for productivity and aesthetics. Each tool has been carefully selected to enhance the development workflow.
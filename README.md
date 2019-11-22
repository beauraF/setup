## setup MacOS workstation

### [Homebrew](https://brew.sh/index_fr)

```sh
  /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

```sh
  brew tap heroku/brew && \
    brew tap homebrew/cask && \
    brew tap homebrew/cask-fonts && \
    brew tap homebrew/cask-versions && \
    brew tap homebrew/services
```

```sh
  brew install \
    asdf \
    git \
    heroku \
    htop \
    nginx \
    nodenv \
    postgresql \
    rbenv \
    sqlite \
    thefuck \
    zsh \
    zsh-autosuggestions \
    zsh-completions
```

```sh
  brew cask install \
    docker \
    firefox \
    font-fira-code \
    google-chrome \
    gpg-suite-no-mail \
    iterm2 \
    spotify \
    tunnelblick \
    visual-studio-code \
    1password
```

### [Oh-My-Zsh](https://ohmyz.sh/)

```sh
  sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

### [spaceship-prompt](https://github.com/denysdovhan/spaceship-prompt)

```sh
  git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" && \
    ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
```

### [zsh-completions](https://github.com/zsh-users/zsh-completions)

```sh
  rm -f ~/.zcompdump; compinit && \
    chmod go-w '/usr/local/share'  
```

### NGinx

```sh
  sudo brew services start nginx
```

### [SSH Key](https://help.github.com/en/enterprise/2.16/user/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

```sh
  ssh-keygen -t rsa -b 4096 -C 'beaurain.florent@gmail.com' && \
    eval "$(ssh-agent -s)" && \
    ssh-add -K ~/.ssh/id_rsa
```

### [GPG Key](https://help.github.com/en/articles/generating-a-new-gpg-key)

```sh
  gpg --full-generate-key
```

### .dotfiles

```sh
  bin/setup
```

### iTerm2

```
iTerm2 ▶ Preferences ▶ General ▶ Preferences ▶ Load preferences from a custom folder or URL
~/.iterm2
```

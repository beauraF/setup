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
    atom \
    docker \
    dashlane \
    firefox-developer-edition \
    firefox-nightly \
    font-fira-code \
    google-backup-and-sync \
    google-chrome \
    google-chrome-canary \
    gpg-suite-no-mail \
    iterm2 \
    jetbrains-toolbox \
    slack \
    spotify \
    steam \
    tunnelblick
```

### [Oh-My-Zsh](https://ohmyz.sh/)

```sh
  sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

### [zsh-completions](https://github.com/zsh-users/zsh-completions)

```sh
  rm -f ~/.zcompdump; compinit
  chmod go-w '/usr/local/share'  
```

### .dotfiles

```sh
  bin/setup
```

### [asdf](https://asdf-vm.com/)

```sh
  asdf plugin-add ruby https://github.com/asdf-vm/asdf-ruby.git
  asdf plugin-add nodejs https://github.com/asdf-vm/asdf-nodejs.git
  asdf plugin-add python https://github.com/danhper/asdf-python.git
  sh ~/.asdf/plugins/nodejs/bin/import-release-team-keyring
  asdf install
```

### NGinx

```sh
  sudo brew services start nginx
```

### [SSH Key](https://help.github.com/en/enterprise/2.16/user/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

```sh
  ssh-keygen -t rsa -b 4096 -C 'beaurain.florent@gmail.com'
  eval "$(ssh-agent -s)"
  ssh-add -K ~/.ssh/id_rsa
```

### [GPG Key](https://help.github.com/en/articles/generating-a-new-gpg-key)

```sh
  gpg --full-generate-key
```

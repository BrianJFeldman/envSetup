Brian's Mac Dev Setup

# From Scratch

- set up gestures
- clean up dock
- open terminal
- install homebrew (`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`)
  - enter to continue with installations
- install Google Chrome (`brew install google-chrome`)
  - open application folder & add Chrome to dock
  - open Chrome and begin setup with personal and work sign-ins
- install Slack (`brew cask install slack`)
  - login to slack
- install iterm2 (`brew cask install iterm2`)
  - close terminal and open iterm
  - setup git config
    - `git config --global user.name "Firstname Lastname"`
    - `git config --global user.email "username@myEmail.com"`
- install zsh (`brew install zsh`)
- install om-my-zsh (`sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`)
  - cd Downloads
    - downloads the MD color scheme(`curl -O https://raw.githubusercontent.com/MartinSeeler/iterm2-material-design/master/material-design-colors.itermcolors`)
    - complete the powerline font installation (`cd && cd Desktop/envSetup && git clone https://github.com/powerline/fonts.git --depth=1 && cd fonts && ./install.sh && cd. . && rm -rf fonts`)
    - clone the envSetup repo (`git clone https://github.com/BrianJFeldman/envSetup.git`)
      - copy the .zshrc to root from the repo (`cp ./envSetup/.zshrc ~/.zshrc`)
- install vscode (`brew cask install visual-studio-code`)
- install python (`brew install python`)
- install xcode from the appstore

- install nvm via cURL(`curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash`)

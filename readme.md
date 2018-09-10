Brian's Mac Dev Setup

# From Scratch
- set up gestures
- clean up dock
- install homebrew (```/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"```)
  - enter to continue with installations
- install Google Chrome (```brew install google-chrome```)
  - open application folder & add Chrome to dock
  - open Chrome and begin setup with personal and work sign-ins
- install Slack (```brew cask install slack```)
  - login to slack
- install iterm2 (```brew cask install iterm2```)
  - close terminal and open iterm
- install zsh (```brew install zsh```)
- install om-my-zsh (```sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"```)
  - cd Downloads
    - downloads the MD color scheme(```curl -O https://raw.githubusercontent.com/MartinSeeler/iterm2-material-design/master/material-design-colors.itermcolors```)
    - complete the powerline font installation (```cd && cd Desktop/envSetup && git clone https://github.com/powerline/fonts.git --depth=1 && cd fonts && ./install.sh && cd. . && rm -rf fonts```)
- install python (```brew install python```)
- install xcode from the appstore

- install nvm via cURL(```curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash```)

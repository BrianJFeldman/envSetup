Brian's Mac Dev Setup

# From Scratch

###Brian's Setup

- set up gestures
- clean up dock
- update dock settings
  - hidden app setting (`defaults write com.apple.dock showhidden -bool TRUE; killall Dock`)
- open terminal
- for M1 Systems: install rosetta (Apple's solution for running Intel software on new chip) (`softwareupdate --install-rosetta`)
- install homebrew (`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`)
  - enter to continue with installations
- install dockutil(`brew install dockutil`)
- install Google Chrome (`brew install google-chrome`)
  - add chrome to dock (`dockutil --add /Applications/Google\ Chrome.app`)
  - open Chrome and begin setup with personal and work sign-ins (`open -a Google\ Chrome`)
- install Slack & add to dock(`brew install slack && dockutil --add /Applications/Slack.app`)
  - login to slack (`open -a Slack`)
- install iterm2 & add to dock (`brew install iterm2 && dockutil --add /Applications/iTerm.app`)
  - close terminal and open iterm (`osascript -e 'quit app "terminal"'(?) && open -a iTerm`)
  - setup git config
    - `git config --global user.name "Firstname Lastname"`
    - `git config --global user.email "username@myEmail.com"`
- install zsh (`brew install zsh`)
- install om-my-zsh (`sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`)
  - cd Downloads
    - downloads the MD color scheme(`curl -O https://raw.githubusercontent.com/MartinSeeler/iterm2-material-design/master/material-design-colors.itermcolors`)
    - clone the envSetup repo (``cd && cd Desktop && git clone https://github.com/BrianJFeldman/envSetup.git`)
      - copy the .zshrc to root from the repo (`cp ./envSetup/.zshrc ~/.zshrc`)
    - complete the powerline font installation (`cd && cd Desktop/envSetup && git clone https://github.com/powerline/fonts.git --depth=1 && cd fonts && ./install.sh && cd . && rm -rf fonts`)
- install vscode & add to dock(`brew install visual-studio-code && dockutil --add /Applications/Visual\ Studio\ Code.app`)
  - open VSCode and install the `settings sync` extension
    - download settings using the gist API (I store mine in my email) and the gist ID that follows the username in the URL to the gist
    - set VSCode as your default git editor (`git config --global core.editor "code --wait"`)
      - You may have to install 'code' for your shell manually. To do so, in VSCode open the commany palette (⇧⌘P) & search for 'Shell Command: Install 'code' command in PATH', and then run.
- install xcode from the appstore(possibly not needed?)
- install python (`brew install python`)
- install golang (`brew install golang && mkdir -p $GOPATH $GOPATH/src $GOPATH/pkg $GOPATH/bin`)
- install nvm via cURL(`brew install nvm && mkdir ~/.nvm && "export NVM_DIR="${XDG_CONFIG_HOME/:-$HOME/.}nvm" [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm" >> ~/.zshrc`)
  - install node(`nvm install node && nvm use node`)
- install common packages global (`npm install -g yarn typescript express gulp grunt webpack`)
- install spectacle (`brew install spectacle`)
- install kubectl (`brew install kubernetes-ctl`)
  - install helm (kubernetes package manager)(`brew install kubernetes-helm`)
- install Postman & add to dock (`brew install postman && dockutil --add /Applications/Postman.app`)
- install postico & add to dock (`brew install postico && dockutil --add /Applications/Postico.app`)
- install spotify & add to dock (`brew install spotify && dockutil --add /Applications/Spotify.app`)
- Setup github ssh (https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)
  - check for existing keys (`ls -al ~/.ssh`)
  - if no keys exist generate a new one (`ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`)
    - start an ssh agent in the background(`eval"$(ssh-agent -s)"`)
    - add a config file (`touch ~/.ssh/config`)
      - add the config settings (`echo "Host *" >> ~/.ssh/config && echo "AddKeysToAgent yes" >> ~/.ssh/config && echo "UseKeychain yes" >> ~/.ssh/config && echo "IdentityFile ~/.ssh/id_rsa" >> ~/.ssh/config`)
    - and add the key to the ssh agent (`ssh-add -K ~/.ssh/id_rsa`)
  - copy the public key to your clipboard (`pbcopy < ~/.ssh/id_rsa.pub`)
    - add the ssh key to your github account (https://github.com/settings/keys)

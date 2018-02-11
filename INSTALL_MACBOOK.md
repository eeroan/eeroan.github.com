# Tasks for fresh install

### Homebrew

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install git fish wget ack jsonpp node yarn postgresql 
brew tap caskroom/cask
brew cask install intellij-idea sizeup launchbar google-chrome virtualbox textmate sketch spotify viscosity vlc flowdock dropbox
```
### Configure fish and nvm
```
sudo bash -c "echo /usr/local/bin/fish>>/etc/shells"
chsh -s /usr/local/bin/fish
curl -Lo ~/.config/fish/functions/fisher.fish --create-dirs https://git.io/fisher
fisher edc/bass
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh | bash
.config/function/nvm.fish:
echo "function nvm
  bass source ~/.nvm/nvm.sh --no-use ';' nvm $argv
end">>.config/function/nvm.fish
```

### OSX tweaks

- iCloud login
- Add statusbar to finder
- Add homedir to finder sidebar
- Move focus to next window shortcut
- Set plain text to textedit `defaults write com.apple.TextEdit RichText -int 0`
- Clean dock `defaults write com.apple.dock persistent-apps -array`
- Configure activity monitor history
- Configure Dock magnification	
- Disable autocorrect `defaults write -g NSAutomaticSpellingCorrectionEnabled -bool false`
- Install hasklig https://github.com/i-tu/Hasklig	`mv ~/Downloads/Hasklig-1/* /Library/Fonts`
- Install apps from app store
- Configure Launcbar: allow accessibility, clipboard history to 100
- Configure sizeUp: allow access, start on login, hide visual action, corner key shortcuts


### Copy stuff from old computer and dropbox:
```
ln -s Dropbox/drop 
ln -s drop/.vimrc 
ln -s drop/.npmrc
ln -s drop/settings/.gitconfig 
copy .locaL/share/fish/fish_history
copy .config/fish/fish.config
copy .config/fish/functions/*
```

### Project stuff
- Register viscosity and copy settings
```
copy .npmrc to project top
nvm install 6.11.1
vm install 8
brew services start postgresql
gem install rhc
```

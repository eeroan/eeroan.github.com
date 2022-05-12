# Tasks for fresh install

### Homebrew

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install git fish wget ack node yarn postgresql 
brew tap homebrew/cask
brew install --cask intellij-idea sizeup launchbar google-chrome virtualbox textmate sketch spotify viscosity vlc dropbox firefox
```
### Configure fish and nvm
```
sudo bash -c "echo /opt/homebrew/bin/fish>>/etc/shells"
chsh -s /opt/homebrew/bin/fish
curl -Lo ~/.config/fish/functions/fisher.fish --create-dirs https://git.io/fisher
fisher install edc/bass
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
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
- Open blank document by default `defaults write -g NSShowAppCentricOpenPanelInsteadOfUntitledFile -bool false`
- Clean dock `defaults write com.apple.dock persistent-apps -array`
- Configure activity monitor history
- Configure Dock magnification	
- Disable autocorrect `defaults write -g NSAutomaticSpellingCorrectionEnabled -bool false`
- Install hasklig https://github.com/i-tu/Hasklig	`mv ~/Downloads/Hasklig-1/* /Library/Fonts`
- Install apps from app store
- Configure Launcbar: allow accessibility, clipboard history to 100
- Configure sizeUp: allow access, start on login, hide visual action, corner key shortcuts
- Make finder open to new windows instead of tabs

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
nvm install <version>
brew services start postgresql
```

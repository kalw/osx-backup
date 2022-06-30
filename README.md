# osx-backup

On First install

```
# Install rosetta if M1
if [[ $(uname -m) == 'arm64' ]]; then
  softwareupdate --install-rosetta --agree-to-license
fi
# Install Homebrew 
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
# get the bundle
curl -Lso ~/Brewfile https://raw.githubusercontent.com/kalw/osx-backup/master/Brewfile
# get minimal tmux config
curl -Lso ~/.tmux.conf https://raw.githubusercontent.com/kalw/osx-backup/master/.tmux.conf
# Install necessary material
brew bundle install --file=~/Brewfile
# Configure VSCode
code-insiders --install-extension Shan.code-settings-sync
# Setup Chrome as default
open -a "Google Chrome" --args --make-default-browser
# custom config
user=$(stat -f %Su /dev/console); 
# Enable AppExpose 4 fingers 
sudo -u $user defaults write com.apple.trackpad.TrackpadFourFingerVertSwipeGesture -int 2
# Enable tap to click
sudo -u $user defaults write defaults write com.apple.AppleMultitouchTrackpad Clicking -bool true
sudo -u $user defaults write com.apple.driver.AppleBluetoothMultitouch.trackpad Clicking -bool true
# Disable the sound effects on boot
sudo nvram SystemAudioVolume=" "
# Disable transparency in the menu bar and elsewhere on Yosemite
sudo -u $user defaults write com.apple.universalaccess reduceTransparency -bool true
# show dotfiles
sudo -u $user defaults write com.apple.Finder AppleShowAllFiles true ; killall Finder
# show batteriy percentage
sudo -u $user defaults write com.apple.menuextra.battery -ShowPercent YES
sudo -u $user killall SystemUIServer
```

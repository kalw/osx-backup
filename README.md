# osx-backup

On First install

```
# Install Homebrew 
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
# Install Dashlane
brew cask install dashlane 
# Clone install material
git clone https://github.com/kalw/osx-backup.git
# Install necessary material
brew bundle install -file=osx-backup/Brewfile
# Configure VSCode
code-insiders --install-extension Shan.code-settings-sync
# Setup Chrome as default
open -a "Google Chrome" --args --make-default-browser
# Enable AppExpose 4 fingers 
defaults write com.apple.trackpad.TrackpadFourFingerVertSwipeGesture -int 2
# Enable tap to click
defaults write com.apple.driver.AppleBluetoothMultitouch.trackpad Clicking -bool true
# Disable the sound effects on boot
sudo nvram SystemAudioVolume=" "
# Disable transparency in the menu bar and elsewhere on Yosemite
defaults write com.apple.universalaccess reduceTransparency -bool true
```

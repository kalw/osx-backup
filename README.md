# osx-backup

On First install

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install dashlane 
git clone https://github.com/kalw/osx-backup.git
brew bundle install -file=osx-backup/Brewfile
code-insiders --install-extension Shan.code-settings-sync
open -a "Google Chrome" --args --make-default-browser
defaults write com.apple.trackpad.TrackpadFourFingerVertSwipeGesture -int 2
defaults write com.apple.driver.AppleBluetoothMultitouch.trackpad Clicking -bool true
```

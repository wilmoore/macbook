# Developer System Setup for Mac OS X

> Prepares a Mac running OS X Mountain Lion (or higher) for polyglot software development. Run as many times as you like...no harm will be done (idempotency).

## Install

NOTE: On Mavericks (or higher), you can optionally skip steps #1 and #2; as the Xcode command-line tools are already installed. That being said, I personally like to install full XCode.

### 1. Get/Install XCode

[![Xcode - Apple](http://r.mzstatic.com/images/web/linkmaker/badge_macappstore-lrg.gif)](https://itunes.apple.com/us/app/xcode/id497799835?mt=12&uo=4)

### 2. Download "Command Line Tools"

Open Xcode

    % open -a Xcode
    
Navigate to "Downloads" with the following steps:

- Press `command + ,` to open "Preferences" pane.
- Click the "Downloads" tab (second to last tab).
- Select "Command Line Tools" and confirm to install.

### 3. Agree to the Xcode/iOS license

If you have skipped #2, you'll need to agree to the license:

    % sudo xcodebuild -license

### 4. Run Setup

    % bash < <(curl -s https://raw.githubusercontent.com/wilmoore/system/master/setup)

## What's in here?

- [dotfiles]
- [homebrew]
- pip (python)
- Mac OSX system updates

## Inspiration

- [2011 Rubyist’s guide to a Mac OS X development environment](http://robots.thoughtbot.com/post/8700977975/2011-rubyists-guide-to-a-mac-os-x-development)
- [boxen](https://github.com/boxen/our-boxen)

## LICENSE

  MIT

[dotfiles]: https://github.com/wilmoore/dotfiles
[homebrew]: https://github.com/wilmoore/homebrew-home

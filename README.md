# Developer System Setup for Mac OS X

> A list of steps that I go through to get a new machine with OS X Mountain Lion (or higher) bootstrapped for polyglot software development. Until there is a blessed way to automate Xcode install, the first couple steps will continue to be manual.

## Install

NOTE: On Mavericks (or higher), you can optionally skip steps #1 and #2; as the Xcode command-line tools are pre-loaded and just need to be installed. Open the `Terminal` app, then type `make` which will cause a prompt to be invoked which asks if you'd like to install the full Xcode or just the command line tools (i.e. just select **Install** if you do not need Xcode).

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
    % sudo xcode-select --install

### 4. Install Homebrew

    % bash < <(curl -s https://raw.github.com/wilmoore/homebrew-home/master/go)
    % brew install python
    
NOTE: Homebrew's python will make your life easier.

### 5. Install Dotfiles

    % git clone https://github.com/wilmoore/dotfiles /tmp/dotfiles
    % bash /tmp/dotfiles/setup

## What's in here?

- [dotfiles]
- [homebrew]
- Mac OSX system updates

## Inspiration

- [2011 Rubyist’s guide to a Mac OS X development environment](http://robots.thoughtbot.com/post/8700977975/2011-rubyists-guide-to-a-mac-os-x-development)
- [boxen](https://github.com/boxen/our-boxen)

## LICENSE

  MIT

[dotfiles]: https://github.com/wilmoore/dotfiles
[homebrew]: https://github.com/wilmoore/homebrew-home


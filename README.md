# dotfiles

Stephen does dotfiles. Inspired by several fantastic dotfiles projects on GitHub, including work by [@mathiasbynens](https://github.com/mathiasbynens/dotfiles), [@holman](https://github.com/holman/dotfiles), [@driesvints](https://github.com/driesvints/dotfiles), and [@anglinb](https://github.com/anglinb/dotfiles).

The goal of this project is to make gettings started with a new machine easy through automation and configuration. Every installer contained here is designed to be as **idempotent** as possible, to make it easy to rerun processes and update my preferences between machines as they evolve.

## Prerequisites

Before running any installers, consider verifying that the following steps have been completed:

- Update macOS to the latest version on the App Store
- Install Xcode from the App Store, open it, and accept the license agreement
- Install macOS Command Line Tools by running `xcode-select --install`

## Installation

Generate a new SSH keypair for this machine if one doesn't exist already.

- A great [GitHub Help article](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/) to walk you through the process.
- Copy any other public or private SSH keys to `~/.ssh` and make sure they're set to `600`.

Configure your default git credentials:

```sh
git config --global user.name "Jane Doe"
git config --global user.email janedoe@example.com
```

Clone the repo to `~/.dotfiles` and run `bootstrap.sh` to install:

```sh
git clone git@github.com:syhchen/dotfiles.git ~/.dotfiles
cd ~/.dotfiles
source ./bootstrap.sh
```

## Other Setup

Not every aspect of setting up a new machine is practical to automate. This section contains written documentation that outlines some other steps that might be useful in the process. Some of these steps might be candidates for automation in the future.

**Finder**

Set Finder shortcut for tags (see: [Stack Exchange](https://apple.stackexchange.com/a/342314)):

1. System Preferences > Keyboard > Shortcuts > App Shortcuts.
1. Click the "+" button, set the Application dropdown to Finder.app, and enter "Tags…" (with the ellipsis character) in the Menu Title tag field.
1. Pick a keyboard shortcut and click "Add".

**Terminal**

Enable "New Terminal Tab at Folder":

1. Keyboard > Shortcuts > Services.
1. Check the box for "New Terminal Tab at Folder".

Set up theme profile for Terminal ([Atom One Dark)](https://github.com/nathanbuchar/atom-one-dark-terminal):

1. Click to open `~/.dotfiles/terminal/atom-one-dark.terminal`.
1. Select the new theme and click "Default" to set it to default.

**iTunes**

Stop auto-syncing in iTunes when connecting an iPhone, iPad, or iPod:

1. iTunes > Preferences > Devices.
1. Check the box for "Prevent iPods, iPhones and iPads from syncing automatically".

**Other Apps**

- [Adobe Creative Cloud](https://creative.adobe.com/products/download/creative-cloud)

## TODOs

- Finish VSCode config.
- Automatically configure `.bash_profile`.
- Add guidlines for home directory config (~/Developer, ~/Designer, etc).
- For VS Code, copy config to symlinked directory from original directory before deleting it.

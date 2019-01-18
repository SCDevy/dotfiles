# dotfiles

Stephen does dotfiles. Inspired by several fantastic dotfiles projects on GitHub, including work by [@mathiasbynens](https://github.com/mathiasbynens/dotfiles), [@holman](https://github.com/holman/dotfiles), [@driesvints](https://github.com/driesvints/dotfiles), and [@anglinb](https://github.com/anglinb/dotfiles).

The goal of this project is to make gettings started with a new machine easy through automation and configuration. Every installer contained here is designed to be as **idempotent** as possible, to make it easy to rerun processes and update my preferences between machines as they evolve.

## Prerequisites

Before running any installers, consider verifying that the following steps have been completed:

- Update macOS to the latest version on the App Store
- Install Xcode from the App Store, open it, and accept the license agreement
- Install macOS Command Line Tools by running `xcode-select --install`

## Installation

Clone the repo to `~/.dotfiles` and run `bootstrap.sh` to install:

```sh
git clone git@github.com:SCDevy/dotfiles.git ~/.dotfiles
cd ~/.dotfiles
source ./bootstrap.sh
```

## Other Setup

Not every aspect of setting up a new machine is practical to automate. This section contains written documentation that outlines some other steps that might be useful in the process. Some of these steps might be candidates for automation in the future.

**SSH**

- Generate a new SSH keypair for this machine if one doesn't exist already. A great [GitHub Help article](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/) to walk you through the process.
- Copy any other public or private SSH keys to `~/.ssh` and make sure they're set to `600`.

**Git**

- Configure your default git credentials:

```sh
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

**VS Code**

See [vscode/README.md](vscode/README.md);

**iTunes**

To stop auto-syncing in iTunes when connecting an iPhone, iPad, or iPod:

1. iTunes > Preferences > Devices.
1. Check the box for "Prevent iPods, iPhones and iPads from syncing automatically".

**Utilities**

- [ColorSnapper 2](https://itunes.apple.com/us/app/colorsnapper-2/id969418666) on the Mac App Store.
- [Magnet](https://itunes.apple.com/us/app/magnet/id441258766) on the Mac App Store.

## TODOs

- Disable swipe between pages in `.macos` config.
- VS Code:
    - Copy files to symlinked directory from original config before removing it.

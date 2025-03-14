# Environment Setup for macOS

This short guide is intended to help new macOS users quickly get setup and familiar with some of the key features.

## Common Keyboard Shortcuts

- Many Windows shortcuts combining `ctrl` with other keys are the same, but with `cmd` being used instead. For example, the shortcuts for copying and pasting are `cmd` + `c` and `cmd` + `v` respectively.
- Search for anything using [Spotlight](https://support.apple.com/en-ca/guide/mac-help/mchlp1008/mac): `cmd` + `space`.
- Open a file: `cmd` + `down arrow`.
- Rename a file: `enter`.
- Delete a file: `cmd` + `backspace`.
- Open the screenshot tool: `cmd` + `shift` + `5`
- Switch between tabs: `cmd` + `tab`.
- Logout/display the lock screen: `ctrl` + `cmd` + `q`.

For more information: [Apple. "Mac keyboard shortcuts".](https://support.apple.com/en-ca/102650)

## Organizing Files

The Finder is used to view, access, and organize almost everything on a Mac.

To quickly open the Finder, use the shortcut `cmd` + `space` to open the Spotlight Search and type "Finder".

For more information: [Apple. "Mac User Guide: Use the Finder on Mac".](https://support.apple.com/en-ca/guide/mac-help/mchlp2605/mac)

## Software Development Setup

### The Command Line

The default command-line interface is called the Terminal.

The Terminal can be opened by searching for it using Spotlight, or using the Finder to locate and open the application directly within `Applications/Utilities/Terminal`.

#### Unix

macOS is a Unix-based operating system. Starting in 2019, the default Unix shell for macOS is the Z shell.

Whenever a new terminal session (i.e. window or tab) is started, various scripts can be loaded via Z shell configuration files. In most cases, these scripts should be added to the `.zshrc` file.

To verify whether the `.zshrc` file exists, please review steps 1 and 2 from the guide on [How to Display the Current Git Branch from the Terminal](terminal-git-branch.md).

#### Xcode Command Line Tools

Apple provides some additional software and tooling for the command-line that isn't installed out-of-the-box. These are the Xcode command line tools. To download and install, run the command: `xcode-select --install`.

#### Support Files

The files required to run all of the installed software and applications are stored within various support folders.

To view the support files for macOS, use the command: `ls ~/Library/Application\ Support`

To view the support file for Unix, use the commands:

```sh
ls ~/.config
```

```sh
ls ~/.local
```

### Homebrew Package Manager

https://brew.sh/

Homebrew is a widely used package manager for installing and updating open-source packages and applications.

For some recommended packages, please review the [Suggested Homebrew Packages](homebrew-suggestions.md).

## Other Guides

- [FromSergio. "Mac Settings That ACTUALLY Make A Difference". YouTube.](https://www.youtube.com/watch?v=Kft9Y33oc2I)
- [Download and Setup Java](java-setup.md)
- [How to Display the Current Git Branch from the Terminal](terminal-git-branch.md)

## Other Tools

- [iTerm2](https://iterm2.com/) - Terminal emulator as alternative to Apple's Terminal app
- [Podman](https://podman.io/) - An open source Open Container Initiative (OCI)-compliant[2] container management tool
- [The Unarchiver](https://theunarchiver.com/) - Open any archive in seconds

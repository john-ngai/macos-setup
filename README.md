# Environment Setup for macOS

This guide is intended to help users who are migrating from Windows to macOS get setup.

## Common Keyboard Shortcuts

- Many Windows shortcuts that combine `ctrl` + another key are similar in that they use `cmd` instead. For example, the shortcuts to copy and paste text are `cmd` + `c` and `cmd` + `v` respectively.
- Search for anything using [Spotlight](https://support.apple.com/en-ca/guide/mac-help/mchlp1008/mac): `cmd` + `space`.
- Open a file: `cmd` + `down arrow`.
- Rename a file: `enter`.
- Delete a file: `cmd` + `backspace`.
- Switch between tabs: `cmd` + `tab`.
- Logout/display the lock screen: `ctrl` + `cmd` + `q`.

For more information: [Apple. "Mac keyboard shortcuts".](https://support.apple.com/en-ca/102650)

## Organizing Files

The Finder is used to view, access, and organize almost everything on a Mac.

To quickly open the Finder, use the shortcut `cmd` + `space` to open the Spotlight search and type "Finder".

For more information: [Apple. "Mac User Guide: Use the Finder on Mac".](https://support.apple.com/en-ca/guide/mac-help/mchlp2605/mac)

## Software Development Setup

### The Command Line

The default command-line interface is called the Terminal.

The Terminal can be opened by searching for it using Spotlight, or using the Finder to locate and open the application directly within `Applications/Utilities/Terminal`.

macOS is a Unix-based operating system. Starting in 2019, the default Unix shell for macOS is the Z shell.

Whenever a new terminal session (i.e. window or tab) is started, various scripts can be loaded via Z shell configuration files. In most cases, these scripts should be added to the `.zshrc` file.

To verify whether the `.zshrc` file exists, please review the guide on [How to Display the Current Git Branch from the Terminal](terminal-git-branch.md).

### Homebrew Package Manager

https://brew.sh/

Homebrew is a widely used package manager for installing and updating open-source packages and applications.

However, it's not strictly required software development.

### Other Guides

TBA

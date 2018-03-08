## Benefits to Community

Visual Studio Code (VS Code) is a popular open source and cross-platform text editor.
Initially released in 2015, it has since gained over 2.6 million monthly active users.
VSCodeVim is an extension for VS Code which provides Vim emulation,
and with over 1.8 million downloads it is one of VS Code's most-installed extensions.
Because VSCodeVim only emulates Vim functionality, it provides a subset of Vim features.
The goal for this proposal is to make use of `nvim`'s remote UI protocol from within VSCodeVim which will:

1. Increase the number of Vim commands and features available in VS Code
2. Decrase the number of emulation bugs affecting users
3. Improve the VSCodeVim codebase for future contributions
4. Make VS Code a more welcoming editor for developers who rely on Vim

In my experience, VS Code provides the best editor features for web developers and Vim provides my favorite text editing capabilities.
Combining VS Code and a true Vim experience through `nvim` will create the ultimate development environment for developers like me.

## Deliverables

Completion of this proposal will yield:

1. A working `nvim` integration within VSCodeVim, with as many of the following addressed as possible:
    - Multicursor support
    - Proper operator handling
    - Sequential actions
    - Cross-file support
    - Proper split and fold handling
    - Settings
    - Snippets
    - Autocomplete
    - Read-only file handling
    - Search highlighting
    - Key Remapping
    - Testing framework
2. Improvements to https://github.com/neovim/node-client where necessary
3. Improvements to https://github.com/neovim/neovim where necessary

Week   Dates          Tasks
------ -------------- ------
1      14-18 May      a
2      21-25 May      b
3      28 May - 1 Jun c
4      4-8 Jun        d
5      11-15 Jun      e
6      18-22 Jun      f
7      25-29 Jun      g
8      2-6 Jul        h
9      9-13 Jul       i
10     16-20 Jul      j
11     23-27 Jul      k
12     30 Jul - 3 Aug l

## Related Work

VSCodeVim
VSCodeNeovim
ActualVim https://github.com/lunixbochs/actualvim
https://github.com/daa84/neovim-gtk and https://github.com/dzhou121/gonvim use the most UI protocol features.
https://github.com/neovim/node-client

## Biographical Information

Contributor to and user of VSCodeVim extension. I feel the need for a fundamental improvement to VSCodeVim as a dev on the project and a user.
Extensive experience with web technologies make navigating VS Code and VSCodeVim a breeze.
Coding in limited-power environments has given me experience suitable to writing responsive UIs and fast data structures.
Actually using the product daily makes me care about user experience, not just deliverable checkmarks.

When necessary, I am comfortable with debugging or extending https://github.com/neovim/node-client.

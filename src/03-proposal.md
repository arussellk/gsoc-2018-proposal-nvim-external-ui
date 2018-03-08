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

## Proposed Timeline

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

The bulk of this proposal will take place in the VSCodeNeovim project.
This project is a fork of VSCodeVim owned by this proposal's mentor Chillee

---------------------- ----------------------------------------------------------
Project Name           Description
---------------------- ----------------------------------------------------------
Neovim                 Vim fork which provides the `nvim` executable. \
                       https://github.com/neovim/neovim \

Neovim Node Client     NodeJS bindings for `nvim`. \
                       https://github.com/neovim/node-client \

VS Code                Graphical text editor. \
                       https://github.com/Microsoft/vscode \

VSCodeVim              VS Code extension which emulates some Vim functionality. \
                       https://github.com/VSCodeVim/Vim \

VSCodeNeovim           Fork of VSCodeVim which holds the starting codebase for this proposal. \
                       https://github.com/Chillee/VSCodeNeovim \

ActualVim              `nvim`-backed extension for Sublime Text. This project provides good implementation ideas. \
                       https://github.com/lunixbochs/actualvim
---------------------- ----------------------------------------------------------

## Biographical Information

I am a long-time user of the VSCodeVim extension and have also contributed to add functionality to it.
I feel the need for a fundamental improvement to VSCodeVim and believe that integrating with `nvim` will improve the extension for both contributors and users.
Having worked professionally with web technologies for several years, I can navigate the VSCodeVim codebase and write maintainable Typescript with ease.
My work in UI/UX has given me the skills to tune perceived performance and I have the development experience to make efficient and maintainable design decisions.
Because I use VS Code daily, I care about the user experience beyond deliverable checkmarks - I want Vim-lovers to feel at home in VS Code!

## Benefits to Community

Visual Studio Code (VS Code) is a popular open source and cross-platform
text editor. Initially released in 2015, it has since gained over
2.6 million monthly active users. VSCodeVim is an extension for VS Code
which provides Vim emulation, and with over 1.8 million downloads
it is one of VS Code's most-installed extensions. Because VSCodeVim only
emulates Vim functionality, it provides a subset of Vim features.
The goal for this proposal is to make use of `nvim`'s remote UI protocol
from within VSCodeVim which will:

1. Increase the number of Vim commands and features available in VS Code
2. Decrase the number of emulation bugs affecting users
3. Improve the VSCodeVim codebase for future contributions
4. Make VS Code a more welcoming editor for developers who rely on Vim

In my experience, VS Code provides the best editor features for
web developers and Vim provides my favorite text editing capabilities.
Combining VS Code and a true Vim experience through `nvim` will create
the ultimate development environment for developers like me.

## Deliverables

The beginning work of this proposal will take place in the VSCodeNeovim
project. (VSCodeNeovim is a fork of VSCodeVim and is owned by this
proposal's mentor, Chillee.) Once VSCodeNeovim is working sufficiently
well, we will merge our `nvim` integration back into VSCodeVim to
expand our user base. After the `nvim` integration is stable, we will
phase out the existing Vim emulation. We will wrap up the end of the
proposal with time for bug fixes and enhancements. Ultimately, we will
provide a stable, predictable, and complete Vim editing experience to
VS Code users.

Completion of this proposal will yield:

TODO: Divide the following list into "Required" and "Optional" tasks.
Put "Required" tasks at the beginning of the timeline and "Optional"
tasks later in the timeline.

1. A working `nvim` integration within VSCodeVim, with as many of the
following addressed as possible:
    - Handle operators without storing state in VSCodeVim
        - For example: `2dd` should cause two lines to be deleted without
          any special logic in VSCodeVim
        - Related: https://github.com/neovim/neovim/issues/6166
    - Cross-file support
        - Actions such as `gd` should keep `nvim` and VSCodeVim in sync
    - Handle split and fold
        - `:sp` and similar commands should work as-expected
        - Fold commands should work as-expected
        - Override `j`, `k`, `gj`, `gk` and related commands
    - Settings
        - Support `.vimrc` files
        - Determine whether VSCodeVim or `nvim` should be the source of
          truth for settings
    - Autocomplete/Snippets
        - Research best solution
        - Handle any auto-expanded text as if the user typed it
        - Related: https://github.com/lunixbochs/ActualVim/issues/97
    - Automated testing framework
    - Filter commands that VSCodeVim should handle and do not send them
      to `nvim`
    - Handle file opening and other events
        - Use autocommands to sync VSCode and `nvim` state
    - Performance
        - To improve performance we need diffs from `nvim`
        - Related: https://github.com/neovim/neovim/pull/5269
        - Related: https://github.com/neovim/neovim/pull/7917
    - Key Remapping
        - (@Chillee: I don't understand this task from the
          PDF you sent me in Slack.)
    - Handle read-only files
        - Research best solution
    - Search highlighting
        - Research best solution
    - Multicursor support
        - Once implemented we will need to ensure that actions are
          sequential
        - Related: https://github.com/neovim/neovim/issues/211
2. Improvements to https://github.com/neovim/node-client where necessary
3. Improvements to https://github.com/neovim/neovim where necessary

Table: Proposed Timeline

------ -------------- ----------------------------------------------------
Week   Dates          Tasks
------ -------------- ----------------------------------------------------
1      14-18 May      1. Gain familiarity with existing codebase. \

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
------ -------------- ----------------------------------------------------

## Related Work

The majority of the coding in this proposal will take place in the
VSCodeNeovim and VSCodeVim projects. VSCodeNeoim already contains a
starting point for a VS Code/`nvim` integration.

The ActualVim project is an extension for Sublime Text which
accomplishes some of what this proposal sets out to do. We will
reference it when appropriate.

Neovim and Neovim Node Client are two projects which our proposal
depend on. We will debug and contribute to both projects as-necessary
to accomplish the goals of this proposal.

Table: Related Projects Summary

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

ActualVim              `nvim`-backed Vim extension for Sublime Text. This project provides good implementation ideas. \
                       https://github.com/lunixbochs/actualvim
---------------------- ----------------------------------------------------------

## Biographical Information

I am a long-time user of the VSCodeVim extension and have also
contributed to add functionality to it. I feel the need for a
fundamental improvement to VSCodeVim and believe that integrating with
`nvim` will improve the extension for both contributors and users.
Having worked professionally with web technologies for several years,
I can navigate the VSCodeVim codebase and write maintainable Typescript
with ease. My work in UI/UX has given me the skills to tune perceived
performance and I have the development experience to make efficient and
maintainable design decisions. Because I use VS Code daily, I care about
the user experience beyond deliverable checkmarks - I want Vim-lovers
to feel at home in VS Code!

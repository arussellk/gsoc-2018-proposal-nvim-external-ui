# GSoC 2018 Neovim Proposal

Use `nvim` to bring Vim functionality to Visual Studio Code

## Summary

This is a proposal to implement "Vim mode" in Visual Studio Code
(VS Code) using `nvim`'s remote UI protocol. VS Code currently has a
popular extension called VSCodeVim which emulates some Vim functionality.
The existing functionality is limited and in some cases error-prone
due to technical challenges with emulating Vim. Changing VSCodeVim
to use `nvim` will expose more of Vim's functionality to users and
allow future development on VSCodeVim to focus on tuning performance
and improving user experience. Using `nvim` will also give VSCodeVim
support for existing `.vimrc` files and many native Vim plugins.
In short, using `nvim` in VSCodeVim will combine the power of Vim
and the convenience of VS Code to improve the everyday lives of
developers.

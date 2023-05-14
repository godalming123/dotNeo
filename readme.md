# dotNeo
My neovim **dot**files with all of the new **neo** and as little of the old vim as possible hense the name `dotNeo`. *Note:* these dofiles are also based off of [kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim)

## Changes
A list of changes compared to the original `kickstart.nvim` (in this repo each commit will implement one of these changes)
 - [X] Remove the unnecessary comments
 - [X] Remove the `which-key.nvim` plugin
 - [X] Remove unnecessary languages from the treesitter setup
 - [X] Set scrolloff to a something more then 0
 - [X] Add a keymap to move the selected text up/down
 - [X] Add a keymap to find and replace the current word
 - [X] Get rid of `vim-sleuth` and replace it with tab indents where each tab is shown a 4 spaces on-screen
 - [ ] Add the undotree plugin
 - [X] Replace the custom LSP with `lsp-zero`
 - [ ] Replace all of the spaces in the `init.lua` with tabs

## Dependencys
 - neovim
 - wl-clipboard

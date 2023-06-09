***My Neovim Cheatsheet***
A cheatsheet for this configuration and neovim in general.
*Note:* Things marked with ***!SPECIFIC*** are not available on all neovim installations but only this configuration.

# Modes
*Note:* From any mode, use ESC to enter normal mode.
      There are also multiple ways of entering another mode.
      However, the keys shown by the mode headings are the primary ways.

## Normal - ESC
There two things you can do in normal mode; enter another mode or edit and navigate text.
To enter another mode you can use the keys by the headers of this modes list.
As for editing and navigating text, there are several syntaxes to do this:
 - {instruction}
 - {commands}{motion}
 - {motion}
*Note:* All of the above can be used with a number to do the operation specified twice.
 - **Commands:**
        Commands are used in conjunction with motions to edit text.
        *Note:* Commands can usually be pressed twice to do a common action - EG: `dd` deletes a line.
              They often also do something slightly deferrent when they are capitalised.
        - **d** deletes text from the cursor to the motion specified and adds it to the clipboard
        - **c** changes text from the cursor to the motion specified
 - **Motions:**
        Normaly, motions can be used to navigate text however in conjuction with *COMMANDS*, they can be used to modify text.
        *Note:* For some motions you can prefix them with i when using commands and visual.
              For example, `diw` deletes the word no matter where you are inside it rathor then deleting to the end of the word.
         - **h/j/k/l** move left/down/up/right
         - **w**       move to the start of the next word
         - **b**       move to the start of the previous word
         - **e**       move to the end of the next word
         - **ge**      move backwords to the end of a word
         - **$**       go to end of line
         - **0**       go to very start of line
         - **^**       go to the begining of code on line (first non-empty charecter)
         - **H/M/L**   go to top/middle/bottom of screen
         - **G**       go to end of file
         - **gg**      go to start of file
         - **}**       jump to next paragraph (or function/block, when editing code) 
         - **{**       jump to previous paragraph (or function/block, when editing code) 
 - **Instructions:**
        Instructions are like commands but already come with a motion attached. EG: x(instruction) = d(command)l(motion)
         - **~**        change case of letter under cursor and move cursor forwards
         - **x**        deletes the letter under the cursor - equivilant to dl
         - **u**        undo
         - **U**        undo all history on line
         - **ctrl + r** redo
         - **o**        enter newline below and start inserting
         - **O**        enter newline above and start inserting
         - **p**        pastes text from the neovim clipboard
         - **r**        replace currently selected letter
         - **zz**       scroll so cursor is centred on screen
         - **zt**       scroll so cursor is on top of screen
         - **zb**       scroll so cursor is on bottom of screen
         - **i**        insert at cursor
         - **I**        insert at begining of line
         - **a**        append at cursor
         - **A**        append at end of line
         - **J**        join line below to current one with one space in-between
         - **S**        delete line and substitute text (like cc)
         - **.**        repeat last command

## Insert - i
 - The primary mode to type text
 - Just type use normal keys such as the arrow keys to move and then press **ESC** when you are done to get back to normal mode.
- **Ctrl + t** indent one line in insert mode
- **Ctrl + d** de-indent one line in insert mode

## Visual - v
 - The mode used to selected text.
 - Use *MOTIONS* to expand/contract your selection
 - Use *COMMANDS/INSTRUCTIONS* to perform operations on your selection
 - Use **o** to switch which end of your selection you are expanding/contracting
 - Their are also other operations that can be performed such as:
         - **U** converts selection to uppercase
         - **u** converts selection to lowercase
         - **J** ***!SPECIFIC*** Move selection down
         - **K** ***!SPECIFIC*** Move selection up

## Visual line - capital V
 - Like visual but select whole lines rathor then charecters

## Visual block - ctrl + v
 - Like visual but selects text in a block

## Replace - R
 - Like insert but when you type this removes the charecter in front of your cursor.

## Command - :
 - Used to type vim commands

# Find
 - Use `/` to search forward in a file
 - Use `?` to search backward in a file
 - Ounce you have pressed enter on your search you can use `n` and `N` to navigate the results

# Find and replace
 - *Note:* you can use leader + fr to find and replace the current selected word ***!SPECIFIC***
 - **Use:** :{range}%s/{pattern}/{string}/{flags} {count}
 - **Range:** (Change occurences...)
         - **%**     In entire file
         - **3,10**  From line 3 to line 10
         - **7**     On line 7
         - **.,+4s** From current line to next four lines
 - **Pattern:**
 - **String:**
         - The string you would like to replace the text with
 - **Flags:**
         - **g**  replace all mathches
         - **gc** replace all mathes with confirmations
 - **Example:**
         - :%s/foo/bar
         - :%s/\(.\)noremap(/vim.keymap.set("\1

# Keyboard shortcuts
 - **Ctrl + g** display current file information
 - **Ctrl + o** go to older cursor position
 - **Ctrl + i** go to more recent cursor position
 - **Ctrl + d/u** go up/down half a page
 - **K** show documentation ***!SPECIFIC***
# !SPECIFIC Keyboard shortcuts
## Search
 - [leader] [S]earch [H]elp
 - [leader] [S]earch [F]iles
 - [leader] [S]earch [?] recent
 - [leader] [S]earch [D]iagnostics
 - [leader] [S]earch for current [W]ord
 - [leader] [G]it [F]iles
 - [leader] [ ] find buffer
 - [leader] [/] fuzzy find buffer

## !SPECIFIC Diagnostics:
 - **]d** - next diagnostic
 - **[d** - previous diagnostic

## Navigation
 - **Goto:**
         - [G]oto [D]efinition
         - [G]oto [R]eferences (opens a references search window)
         - [G]oto [↑D]eclartion

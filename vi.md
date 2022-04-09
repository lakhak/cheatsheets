# VI

Useful commands for vi

`:help` see help page

## editing
- `i` insert mode
- `CTRL+N` word completion, next matching word while in insert mode
- `CTRL+P` word completion, previous matching word while in insert mode
- `y` copy line (in visual mode)
- `p` paste line
- `dd` delete line
- `{n}dd` delete n lines
- `dG` delete to end of file
- `CTRL-h` in insert mode to delete one character
- `CTRL-w` in insert mode to delete one word
- `CTRL-u` in insert mode to delete entire line

## tabs
- `:tabnew` open new tab
- `gt` go to next tab
- `gT` go to previous tab
- `{n}gt` go to nth tab
- :`tabc` close the current tab
- `:tabo` close all other tabs
- `:tabm {n}` move the current tab after tab n

## windows
- `:new` open new window above current one
- `:vnew` open new window to left of current one
- `CTRL+W {dir}` move cursor to next window in direction of dir
- `CTRL+W r` move window down and right
- `CTRL+W R` move window up and left
- `CTRL+W CTRL+O` close all other windows except the current one

## navigation
- `e` move cursor to end of word
- `b` move cursor to beginning of word
- `$` move cursor to end of line
- `^` move cursor to beginning of line
- `gg` start of file
- `G` end of file
- `{n}gg` go to line n
- `{n}j` move cursor down n lines
- `{n}k` move cursor up n lines
- `:set number` show line numbers (add to ~/.vimrc to make permanent)
- `:set nonumber` hide line numbers

## visual mode
- `v` enter visual mode

## sed
- `:%s/regex/rep/g` sed substitution in vi

## indentation
- `=` after entering visual mode and highlighting lines
- `gg,v,G,=` indent entire file
- `:setlocal shiftwidth={n}` set indentation to n spaces
- `:setlocal tabstop={n}` set tab character to n spaces
- `~/.vim/after/ftplugin/{filetype}.vim` override shiftwidth, tabstop etc. per file type e.g. `html.vim`

## quickfix
- `:copen` to open quickfix list
- `:ccl` to close it
- `:cn` go to next item in quickfix list
- `:cp` go to previous item
- `:cfdo {cmd}` execute cmd for each item in quickfix list e.g. `:cfdo %s/foo/bar/g | :w`

## NERDTree
- `:NERDTree` open NERDTree
- `r` in NERDTree window to refresh
- `map <C-n> :NERDTreeToggle<CR>` add to .vimrc to map shortcut to toggle NERDTree
- `:let g:NERDTreeWinSize=40` adjust window size
- `m` open NERDTree menu for options on adding, deleting etc.

## fugitive
- `:Git` open staging view
- `ri` interactively rebase commit under cursor
- `dv`, `dh` show git diff

## fzf/ripgrep
- `:FZF` open find window and search, then:
  - `Enter` to replace current window with selected
  - `CTRL+O` to open selected in vsplit window
  - `CTRL+X` to open selected in hsplit window
- `:Rg` to search files
	- `Alt` to add individual items to quickfix list
	- `Alt+a` to add all items to quickfix list

## other
- `:!{command}` execute external command
- `:help {v|i}_{key}` help on what `key` does in `v` (visual) or `i` (insert) mode 

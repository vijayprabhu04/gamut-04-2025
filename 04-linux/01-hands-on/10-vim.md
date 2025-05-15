# VIM introduction

- Vim is an editor to create or edit a text file
- There are two modes in vim. One is the command mode and another is the insert mode
- In the command mode, user can move around the file, delete text, etc
- In the insert mode, user can insert text

## Changing mode from one to another

- From command mode to insert mode type `i`
- From insert mode to command mode type Esc

## Command mode

| Command  | Description                                  |
| -------- | -------------------------------------------- |
| `h`      | Moves the cursor one character to the left   |
| `l`      | Moves the cursor one character to the right  |
| `k`      | Moves the cursor up one line                 |
| `j`      | Moves the cursor down one line               |
| `$`      | Move cursor to the end of current line       |
| `0`      | Move cursor to the beginning of current line |
| `set nu` | set numbers for every line                   |


## Exit Commands

| Command  | Description                                                       |
| -------- | ----------------------------------------------------------------- |
| `wq`     | Write file to disk and quit the editor                            |
| `wq!`    | Write file to disk and quit the editor (no warning) (forceful)    |
| `q!`     | Quit (no warning) (forceful)                                      |
| `q`      | Quit (a warning is printed if a modified file has not been saved) |

## Text deletion commands

| Command | Description                      |
| ------- | -------------------------------- |
| `x`     | delete a character               |
| `dw`    | delete word from cursor on       |
| `db`    | delete word backward             |
| `dd`    | delete line                      |
| `d$`    | delete till eof line from cursor |
| `5dd`   | delete 5 lines                   |

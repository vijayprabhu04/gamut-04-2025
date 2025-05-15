# ECHO 

- Echo command in linux is used to display line of text/string that are passed as an argument
- This is a built in cmd that is mostly used in shell scripts & cmd line to output text on screen or a file

## Syntax :

`echo [option] [string]`

### Displaying a text/string

| Command                             | Description                                          | Flags                                      |
| ----------------------------------- | ---------------------------------------------------- | ------------------------------------------ |
| `echo [string]`                     | Just print the provided string                       |                                            |
| `echo "[string]"`                   | Can also be wrapped with double quotes               |                                            |
| `echo '[string]'`                   | Can also be wrapped with single quotes               |                                            |
| `echo -e "hello \bworld"`           | remove spaces & enable backslash escape              | `-e` = enables backslash escapes           |
|                                     |                                                      | `\b` = removes all spaces between the text |
| `echo -e "hello \cworld"`           | remove text & enable backslash escape                | `-e` = enables backslash escapes           |
|                                     |                                                      | `\c` = text after \c is not printed        |
| `echo -e "hello \nworld"`           | print strings in new line                            | `-e` = enables backslash escapes           |
|                                     |                                                      | `\n` = print text in next line             |
| `echo -e "hello \tworld"`           | creates horizondal tab space                         | `-e` = enables backslash escapes           |
|                                     |                                                      | `\t` = print text with tab space           |
| `echo -e "hello \rworld"`           | prints text before \r                                | `-e` = enables backslash escapes           |
|                                     |                                                      | `\r` = text after \r will be printed       |
| `echo -e "hello \vworld"`           | creates vertical tab space                           | `-e` = enables backslash escapes           |
|                                     |                                                      | `\v` = print text with tab space           |
| `echo *`                            | print all files/folders, similar to ls command       |                                            |
| `echo *.md`                         | print all files with .md extension                   |                                            |
| `echo "hello world" > filename`     | can be used with redirect operator to output to file |                                            |
| `echo $USER`                        | view current logged user                             |                                            |
| `echo $?`                           | used to check exit status                            |                                            |
| `echo "listing directories: $(ls)"` | adding string along with command                     |                                            |
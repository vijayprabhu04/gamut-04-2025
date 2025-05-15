# Grep module

## Grep stands for Global Regular Expression Print

### Usecase

- Grep is a Linux command-line tool used to search for a string in a specified file
- This text search pattern is called a regular expression
- When it finds a match, it prints the line with the result
- The grep command is handy when searching through large log files

#### Grep to search a file

- Using grep to print any line from a file that contains a specific characters

| Command                              | Description                  |
| ------------------------------------ | ---------------------------- |
| `grep <word-to-search> <filename>`   | Search word in file          |
| `grep "<word-to-search>" <filename>` | using quotations are allowed |

#### Grep to search multiple files

- We can search multiple files with the grep command
- Insert the filenames you want to search, separated with a space character

| Command                                             | Description                  |
| --------------------------------------------------- | ---------------------------- |
| `grep <word-to-search> <filename-1> <filename-2>`   | Search word in file          |
| `grep "<word-to-search>" <filename-1> <filename-2>` | using quotations are allowed |

#### Search all files in directory

To search all files in the current directory, use an asterisk instead of a filename at the end of a grep command

| Command                   | Description                                                  |
| ------------------------- | ------------------------------------------------------------ |
| `grep <word-to-search> *` | Search word in all files under current working directroyfile |

#### Search complete word whatever given as it is

- Grep allows you to find and print the results only if the whole word matches

| Command                      | Description                                   |
| ---------------------------- | --------------------------------------------- |
| `grep -w <word-to-search> *` | only prints if the given word matches exactly |

- Test the same case without `-w` or by giving wrong match to understand better 

#### Ignore case sentive

- In general grep commands are case sensitive, one of the most useful operators for grep searches is -i
- Instead of printing lowercase results only, it ca displays both uppercase & lowercase results when we include -i

| Command                      | Description                                        |
| ---------------------------- | -------------------------------------------------- |
| `grep -i <word-to-search> *` | prints both upper & lower case when string matches |

#### To Search in Subdirectories

- To include all subdirectories in a search, add the -r operator to the grep command

| Command                      | Description                                     |
| ---------------------------- | ----------------------------------------------- |
| `grep -r <word-to-search> *` | find matching strings including in subdirectory |

#### Inverse grep search

- You can use grep to print all lines that do not match a specific pattern of characters, To invert the search, append -v to a grep command

| Command                      | Description                                     |
| ---------------------------- | ----------------------------------------------- |
| `grep -v <word-to-search> *` | avoid lines which is matching with given string |

#### To List directories Matching with given string

| Command                         | Description                                       |
| ------------------------------- | ------------------------------------------------- |
| `grep -l -r <word-to-search> *` | print directory names matching with given strings |

#### To Display Line Numbers with grep Matches

| Command                         | Description                               |
| ------------------------------- | ----------------------------------------- |
| `grep -n -r <word-to-search> *` | print the line number of matching strings |

# Create file

## create file using `touch` module

| Command                     | Description                    | Flags |
| --------------------------- | ------------------------------ | ----- |
| `touch file1.txt`           | Create file with touch         |       |
| `touch file1.txt file2.txt` | Create multiple files          |       |
| `touch /tmp/file1.txt`      | Create file under specific dir |       |
| `touch /tmp/file2.txt`      | Using verbose                  |       |

## Creating a File with the `Redirection Operator`

| Command       | Description                                                                             | 
| --------------| ----------------------------------------------------------------------------------------|
| `> file1.txt` | Redirection allows to capture o/p from cmd-line & send it as i/p to another cmd or file |

## Creating a File with `cat` module

| Command            | Description                                                                            | 
| ------------------| ----------------------------------------------------------------------------------------|
| `cat > file1.txt` | use cat cmd followed by redirection operator > and the name of file want to create      |

## Creating a File with `echo` module

`The echo command prints the strings that are passed as arguments` We can see echo in detail later

| Command                  | Description                                                                                        | 
| -------------------------| ---------------------------------------------------------------------------------------------------|
| `echo "abc" > file1.txt` | echo cmd followed by text to print & redirection operator > to write the o/p to file to be created |

## Creating a File using `Heredoc`

* Here document (Heredoc) is a type of redirection that allows you to pass multiple lines of input to a command

```
cat << EOF > file1.txt
Some line
Some other line
EOF
```

## Create file using vim or nano editor

| Command         | 
| ----------------| 
| `vim file1.txt` |

* Write all the lines need to be in the file
* save and exit the file using key bindings `esc + shift + wq`
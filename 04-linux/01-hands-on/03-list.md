# List module

## ls stands for list

| Command        | Description                           |
| -------------- | ------------------------------------- |
| `ls`           | list the file which is in same dir    |
| `ls ..`        | list the file which is in parent dir  |
| `ls ../../`    | list file which is two steps ahead    |
| `ls ../../etc` | list etc directory from different dir |


## Long listing

| Command       | Description                                            | Flags                                       |
| ------------- | ------------------------------------------------------ | ------------------------------------------- |
| `ls -l /etc`  | list the file which is in same dir                     | `l` = refers long listing                   |
| `ls -a /etc`  | list including hidden files                            | `a` = do not ignore files starting with [.] |
| `ls -lh /etc` | list file size in human readable formate [KB, MB & GB] | `h` = human readable                        |


## Combine all arguments

| Command   | Description                               |
| --------- | ----------------------------------------- |
| `ls -alh` | list hidden files, in human readable form |
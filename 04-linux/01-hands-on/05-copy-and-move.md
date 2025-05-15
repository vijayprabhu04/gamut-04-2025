# Copy module

| Command                | Description            | Flags           |
| ---------------------- | ---------------------- | --------------- |
| `cp [file] [file]`     | Copy one file to other |                 |
| `cp -r -v [dir] [dir]` | Copy one dir to other  | `r` = recursive |
|                        |                        | `v` = verbose   |

# Move module

SYNTAX : `mv [options] source dest`

| Command                            | Description                                      | Flags           |
| ---------------------------------- | ------------------------------------------------ | --------------- |
| `mv [file] [file]`                 | move one file to other                           |                 |
| `mv [file] [file] /tmp`            | move multiple files togather to /tmp             |                 |
| `mv file* /tmp/data`               | move all files starting with string file to /tmp |                 |
| `mv /tmp/bak/* /root.bak`          | move all files under /tmp/bak/ to /root          |                 |
| `mv main.c main.bak`               | Rename file                                      |                 |
| `mv -r -v -f /tmp/bak/* /root.bak` | Recursive copy                                   | `r` = recursive |
|                                    |                                                  | `v` = verbose   |
|                                    |                                                  | `f` = force     |

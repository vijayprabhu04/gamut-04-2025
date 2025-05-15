# Create directory

* To create directory in linux we can use `mkdir` module


| Command          | Description                                          | Flags                           |
| ---------------- | -----------------------------------------------------|---------------------------------|
| `mkdir /data`    | Create directory with name data under root partition |                                 |
| `mkdir /tmp/data`| Create directory with name data under tmp partition  |                                 |
| `mkdir -v /data` | Run command in verbose mode                          | v = refers verbose              |
|                  |                                                      | [-v] print results of given cmd |

# Create parent and sub directory

| Command                     | Description                               | Flags             | 
| ----------------------------| ------------------------------------------| ------------------|
| `mkdir -v -p /example/file` | Create parent directory and sub directory | [p] refers parent |
|                             |                                           | [v] refers verbose|
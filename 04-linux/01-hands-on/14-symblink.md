# Symbolic Links and Their Use

- A symlink is a symbolic link that points to another file or folder on your computer system
- This is similar to a Windows shortcut

# Symlinks can take two forms

- Soft links
- Hard links

<Mark> Important difference between these are 
hard links can only work within the same filesystem 
while symbolic links can go across different filesystems </mark>

## Hard link creation

`ln <file/folder-to-be-linked> <link-file>`

## Soft link creation

`ln -s <file/folder-to-be-liked> <link-file>`

sample : `ln -s /data/script.sh script`

## To make a hard link directly into a soft link, use the -P flag like this

`ln -P <file/folder-to-be-linked> <link-file>`
# SSH stands for secure shell

- SSH helps to connect with linux machines securly
- By default it uses port number 22
- You can connect to any linux machines via ssh using username/password
- Default ssh config file `/etc/ssh/sshd_config`
- Restart ssh service `service sshd restart`

## Connect via password

- SSH to any machine with command `ssh <username>@<ipaddress>`
- Provide the password while its prompting for to login into machine

## Provide password as an argument at command line

- To provide password as an additional argument you can use tool called `SSHPASS`
- To install SSHPASS in ubuntu `apt install sshpass`
- Connect to target machine by using SSHPASS `sshpass -p "******" ssh <username>@<ipaddress>

## Password less connection

- To connect with another linux machine without providing password we can use SSH keys
- Source machine public key to be copied to target machine where you need to connect
- How to generate key in source machine ?
    * ssh-keygen
    * To check if key is generated `cat .ssh` folder under your home directory
- How to copy the key to target machine
    * ssh-copy-id <username>@<ipaddress>
    * Provide password at prompt to copy the key to target machine

## Tools used for SSH in general

- putty      (windows)
- mtputty    (windows)
- powershell (windows)
- cmd prompt (windows)
- vscode     (windows & mac)
- iterm      (mac)
- terminal   (mac)
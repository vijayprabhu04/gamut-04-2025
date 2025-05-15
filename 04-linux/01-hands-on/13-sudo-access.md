# Managing sudo access in linux is challanging

- To control sudo access we can defind who can do what in linux file `/etc/suoders`


## Sample edit

- How to provide access for certain users to just restart some services
- create all users who need access to restart services
  `useradd dbuser1 dbuser2`
- create group to add all these users into it
  `groupadd dbadmin`
- add all users into the group
  `usermod -aG dbadmin dbuser1 dbuser2`
- Goto /etc/sudoers file to delegate access for group dbadmin

### lines to be pasted at eof

```
Cmnd_Alias PROCESSES = /bin/nice, /bin/kill, /usr/bin/kill, /usr/bin/killall
Cmnd_Alias SERVICES = /sbin/service, /sbin/chkconfig, /usr/sbin/service
Cmnd_Alias DELEGATING = /bin/vi, /bin/mkdir

%dbadmin     ALL=NOPASSWD: PROCESSES, SERVICES, DELEGATING
```

### Validate

- Swith to those users using command sudo su - <username>
- Run commands relevant to service restart and check if its working without prompting for password

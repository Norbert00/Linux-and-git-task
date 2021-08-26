# Linux-and-git-task

## sshd_config
I used an Ubuntu server set up with EC2 AWS to complete the task. 
I allowed myself to modify the task a bit because by default root is not able to log into the instance. 
I initially modified the sshd_config file to be able to login as root. 
Additionally I modified /root/.ssh/authorized_keys file so that I don't get the message that I can't login as root.

[![Screenshot-from-2021-08-26-20-33-08.png](https://i.postimg.cc/xdC894Sv/Screenshot-from-2021-08-26-20-33-08.png)](https://postimg.cc/k20qcwGG)


Next I created own_sshd_config file which I keep in /tmp/dev_task/ and for it I created softlin in /etc/ssh/sshd_config, where I already forbid to login as root to the instance.

[![Screenshot-from-2021-08-26-20-29-43.png](https://i.postimg.cc/T2mw2bB4/Screenshot-from-2021-08-26-20-29-43.png)](https://postimg.cc/s1jywMjY)

[![Screenshot-from-2021-08-26-20-35-10.png](https://i.postimg.cc/GmM3gxsH/Screenshot-from-2021-08-26-20-35-10.png)](https://postimg.cc/3kvHdp1T)


## Motd
I removed all -x permissions in /etc/update-motd.d/ then created my own script that will display motd. I placed the script in /tmp/dev_task/
Next I created a softlink to it in /etc/update-motd.d/00-header and gave it +x permission to be executable which allowed me to display motd every time I logged in.

[![Screenshot-from-2021-08-26-21-03-15.png](https://i.postimg.cc/T3jNTtc3/Screenshot-from-2021-08-26-21-03-15.png)](https://postimg.cc/fVLfKjFG)


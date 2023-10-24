I did not know what a local daemon meant. Read up on what that is but 

Even tried ti manually connect to each port
nc -vz localhost 1-32000 2>&1 | grep succeeded | grep -o [3][0-9][0-9][0-9][0-9]

./suconnect 31960

![image](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/e3d82db6-4b51-4c9e-8c96-01173af753ce)



reading the task details again a few times I realised maybe own network daemon meant opening a port on localhost of bandit20. 


Read up how to open a port to listen for incoming data on Linux and found ```nc -l -p <port_name>``` on this article https://www.howtouselinux.com/post/linux-command-open-a-port-on-linux


On doing this it was a blank terminal waiting for input,so i logged in a bandit20 on another terminal and tried to do ./suconnect 4000 on that 
and it also was a blinking curson waiting for some input. 


So as per the question, i sent the password as input on the original terminal and got back the level 21 password. Going back to the new terminal showed this output:

```
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT

Password matches, sending next password
```

![image](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/e3582e22-4187-4484-8ae2-0ac1eda30936)



 

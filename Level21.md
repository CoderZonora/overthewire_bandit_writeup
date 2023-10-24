I did not know what a local daemon meant. Read up on what that is but not meaningful about how to get the password came up.

Used ```nc -vz localhost 1-32000 2>&1 | grep succeeded | grep -o [3][0-9][0-9][0-9][0-9]``` to get list of ports and tried to manually connect to each port 
using ./suconnect <port_name> but no port returned the password.

![image](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/e3d82db6-4b51-4c9e-8c96-01173af753ce)



After reading the task details again a few times I realised maybe connecting to own network daemon meant opening a port on localhost of bandit20. 


Read up how to open a port to listen for incoming data on Linux and found ```nc -l -p <port_name>``` on this article https://www.howtouselinux.com/post/linux-command-open-a-port-on-linux


On doing this it was a blank terminal waiting for input,so I logged in a bandit20 on another terminal and tried to do ./suconnect 4000 on that 
and it also returned a blinking curson waiting for some input. 


So as per the question, I sent the password as input on the original terminal and got back the level 21 password. Going back to the new terminal showed this output:

```
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT

Password matches, sending next password
```
![image](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/cf168e63-b9cc-4799-b1c0-ad2657b85a31)

Pass for bandit21: NvEJF7oVjkddltPSrdKEFOllh9V1IBcq

![image](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/e3582e22-4187-4484-8ae2-0ac1eda30936)






 

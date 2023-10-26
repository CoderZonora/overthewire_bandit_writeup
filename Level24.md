Reading the cronjob in ```/etc/cron.d``` showed that the script ```/usr/bin/cronjob_bandit24.sh``` would be executed as **bandit24**.
![image](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/c6710ba6-9271-4db3-8536-45924c16da27)



After reading the script ```/usr/bin/cronjob_bandit24.sh``` and reading about **timeout** I understood that the script would simply execute the files in the 
```/var/spool/bandit24/foo``` directory if the owner of them is bandit23 and then delete them. So I had to place my script in that directory.
![image](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/268250bf-c8e4-447b-a421-d5916ceeee55)

I created a directory **abc1** in ```/tmp``` to store my script. 

My first attempt was to copy the ```/etc/bandit_pass/bandit24``` file to the tmp directory but that did not work.
Running ```bash /usr/bin/cronjob_bandit24.sh``` it showed permission denied. So I got to know that the new files I create cannot be accesed by other users. 
I used ```chmod 777 test.sh``` to elevate the permissions for all users.


Next I thought to cat the contents of ```/etc/bandit_pass/bandit24``` but there was no output on the terminal. 
I thougth it was due to the ```&> /dev/null```in the cronjob ,so I thought maybe I could store the contents into a file im the tmp directory instead of directly trying to output to **stdout**.


So finally wrote the script:

```
#! /bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/abc1/24.txt

```
and gave permission ```chmod 777 test.sh``` but it just did not work.


After many tries to run it I finally realised that I did not elevate the permissions for the file in the abc1 drectory.
Doing this finally gave the password for bandit24 into the 24.txt file.

![image](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/5d45daf1-124d-41f9-a519-4f88c2ac376f)


Password for bandit24: VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar



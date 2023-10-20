Goal : The password for the next level is stored in the file data.txt and is the only line of text that occurs only once.


I started by reading up on the commmands proovided in the Level description. Go to know about the ```uniq``` command and instantly thought that this was an exact match to the problem. But doing ```uniq data.txt``` did not work. I tried the ```-c``` option and saw that almost all lines have a count of 1. I verified this by doing ``` uniq -c data.txt | grep -v '1' ``` but that showed that there were only three lines having count of 2 which was completely against what the question demanded.I was stuck at this point for some time.

![VirtualBox_Ubuntu_20_10_2023_18_56_02](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/71e97fae-ae68-476c-a63b-d23da12717dc)
![VirtualBox_Ubuntu_20_10_2023_18_55_11](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/529a1ed8-fe9a-4153-b695-65d69d1cb192)
![VirtualBox_Ubuntu_20_10_2023_19_01_11](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/183a8947-fc15-404a-b048-27ebc657a056)
![VirtualBox_Ubuntu_20_10_2023_18_56_14](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/afbec33b-a0f3-4712-8c2d-6b3e399e0449)
![VirtualBox_Ubuntu_20_10_2023_18_56_32](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/a414a84f-fcba-41d3-9bba-c87831cd1842)

But after trying for some more time I noticed that in the output of uniq 2 lines were same which prompted me to searched if uniq does not work for others for some reason and that as when I discovered that ```uniq``` only works with sorted data (via this thread https://askubuntu.com/questions/536775/uniq-command-not-working-properly ).


I just edited my initial command to ```sort data.txt | uniq -u ``` and got the required password.


![VirtualBox_Ubuntu_20_10_2023_19_03_37](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/c17752b5-e4c7-4551-93a3-ac7fba626327)


Password for bandit9 : EN632PlfYiZbn3PhVK3XOGSlNInNE00t



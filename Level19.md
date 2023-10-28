First I tried to see if maybe bandit17 had read prmissions to the readme file but it did not.


Next I tried to see if maybe connecting via telnet would work but it did not even after trying to read many thread to try to debug the errors.


After thinking a bit I had an idea. Maybe if I used ```scp``` to get the file to my local machine but not log in,it could work. 
Used the article  https://www.freecodecamp.org/news/scp-linux-command-example-how-to-ssh-file-transfer-from-remote-to-local/ 
to know about the scp syntax.


Used ```scp -P 2220 bandit18@bandit.labs.overthewire.org:readme . ``` to copy the file and get the password.

![VirtualBox_Ubuntu_24_10_2023_16_40_36](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/1fac1edc-f37e-40bd-8b7e-c4bdc2016349)


Password for bandit19:awhqfNnAbc1naukrpqDYcF95h7HoMTrC

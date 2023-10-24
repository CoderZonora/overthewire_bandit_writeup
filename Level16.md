Even though both protocols have much in common, under the hood SSH has its own transport protocol, independent from SSL. They are entirely different protocols.
So cannnot use ```ssh``` for this level.


***openssl*** was mentioned in the helpful commands list so read on how to connect to a server using ssl in linux. Found out about ```openssl s_client``` option.


used ```openssl s_client localhost:30001``` to set up a new ssl connection. Then provided password of current level to get password in return.



![VirtualBox_Ubuntu_24_10_2023_00_42_32](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/5a0dba53-28a2-4d93-aec6-cbf26c5a820f)


Pass for bandit16:JQttfApK4SeyHwDlI9SXGR50qclOAil1

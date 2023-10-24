Used ./bandit20-do to run the file. It gave output :

```
Run a command as another user.

  Example: ./bandit20-do id
```


i first tried to run ``` ./bandit20-do id ``` thinking and it showed the uid and guid of bandit 19 and 20. I thought maybe I could elevate the permissions of bandit19 
to those of bandit20 by running ``` ./bandit20-do 11019 ```,so that i could get its password from /etc/bandit_pass/bandit20, but that was wrong. 
It was then when I realised what i had to actually do. 


Ran ./bandit20-do cat /etc/bandit_pass/bandit20 and it worked

![image](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/dedf8b0c-7db1-4a37-93b2-f9797f064f6b)

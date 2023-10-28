I had read about the ```tr``` command as it was given in the list of useful commands. I tried to use it but got an error.


There was not encryption package installed to decrypt ROT-13(or encrypt it, it is it's own inverse) directly.
![VirtualBox_Ubuntu_20_10_2023_19_48_26](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/e005df29-f0d2-43a7-8dbd-7f820f319c9e)


Read about ROT-13 and found my answer in this thread on how to properly use ```tr``` for this use case:
https://stackoverflow.com/questions/5442436/using-rot13-and-tr-command-for-having-an-encrypted-email-address


Used the following command to get the password : ```cat data.txt| tr A-Za-z N-ZA-Mn-za-m```

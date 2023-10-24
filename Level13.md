I knew about the xxd command so I first tried to directly reverse the hexdump and pipe to gzip using ```xxd -r data.txt | gzip -d```. But it threw an error.
Next I tried command substitution using ``` gzip -d $(xxd -r data.txt ) ```but even that did not work.

![VirtualBox_Ubuntu_20_10_2023_23_52_40](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/34fe2376-9b28-4339-85a6-775b021f5440)

I moved on to trying to read about **bzip2** to see if maybe that helps.

![VirtualBox_Ubuntu_21_10_2023_00_07_17](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/46f347fd-519f-4ea7-a5dd-7f036e77f8af)

But it was not working so I took the hint in the level description and created a new directory, copied the original file into it, reversed the hexdump into a new file 
and tried to read more about all the commands given in the useful commands list.


I had to try different things and options in ```gzip``` as the ```-S``` confused me about how to use ```gzip```.
But even after that decompression using ```gzip``` or ```gunnzip``` or ```zcat``` just did not work.
I even renamed it to a **.gz** file after reading this thread(https://unix.stackexchange.com/questions/660312/cant-uncompress-a-gzip-compressed-data) but I was just using too many options and it did not work.

![VirtualBox_Ubuntu_20_10_2023_23_52_01](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/1154cb37-5f8c-42a4-93ba-6dd888539c46)
![VirtualBox_Ubuntu_20_10_2023_23_51_39](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/55a2ca2d-c142-4190-9f14-05bc3722ad74)

Finally I just tried using nothing extra and it clicked, no errors and I got a result. It was not a human-readable file still so I tried ```gzip -d``` again but it indicated that it was not a gzip file.


So used the ```file``` commmand and it was a bzip2 file. So decompressed that and the files continued to be of different formats(gzip,bzip2 and tar archive) and after 5-6 decompressions and renamings, 
finally got the ASCII test file containing the password.

![VirtualBox_Ubuntu_21_10_2023_00_07_36](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/e1923775-0ce6-4f31-8c5e-aec5286c7d3b)
![VirtualBox_Ubuntu_21_10_2023_00_07_45](https://github.com/CoderZonora/overthewire_bandit_writeup/assets/140229408/b1ac419b-2f52-4e14-a808-82baeb9ea0a8)



Password for bandit13: wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw

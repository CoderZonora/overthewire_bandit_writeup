Goal : The password for the next level is stored in the file data.txt and is the only line of text that occurs only once.


This should have been very quick and simple but ended up being a huge time waste.
I started by reading up on the commmands proovided in the Level description. Go to know about the ```uniq``` command and instantly thought that this was an exact match to the problem. But doing ```uniq data.txt``` did not work. I tried the -c option and saw that almost all lines have a count of 1. I verified this by doing ``` uniq -c data.txt | grep -v '1' ``` but that showed that there were only three lines having count of 2 which was completely against what the questin demanded.

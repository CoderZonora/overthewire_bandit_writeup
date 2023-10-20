I knew about the xxd command so I first tried to directly reverse the hexdump and pipe to gzip using ```xxd -r data.txt | gzip -d```. But it threw an error.
Next I tried command substitution using ``` gzip -d $(xxd -r data.txt ) ```but even that did not work.
I moved on to trying to read about **bzip2** to see if maybe that helps.
But it was not working so I took the hint in the level description and created a new directory, copied the original file into it, reversed the hexdump into a new file 
and tried to read more about all the commands given in the useful commands list.


I had to try different things and options in ```gzip``` as the ```-S``` confused me about how to use ```gzip```.
But even after that decompression using ```gzip``` or ```gunnzip``` or ```zcat``` just did not work.


Finally figured out that I had to rename it to a **.gz** file for it to work and won't work with file with no extension because of this thread even though I
had thought that it should upon reading the man pages : (https://unix.stackexchange.com/questions/660312/cant-uncompress-a-gzip-compressed-data)
The uncompressed file was still not readable so I reversed the gzip again but it threw error indicating that the file was not a gzip. 


So used the ```file``` commmand and it was a bzip2 file. So decompressed that and the files continued to be of different formats(gzip,bzip2 and tar archive) and after 5-6 decompressions and renamings, 
finally got the ASCII test file containing the password.


Password for bandit13: wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw

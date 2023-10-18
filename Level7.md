Goal - Find a file with following criteria:


    owned by user bandit7
    owned by group bandit6
    33 bytes in size

It took me a short while to figure out the file structure of this particular server as it was directly not having any familiar 
file structure.


After moving about in the directories I could not see any specific file which would directly give the password so I had to search using ```find``` or ```ls```.
First I thought of filtering files by user as maybe there is only one file under the user ```bandit7```, and searched about on how to do that .


My first approach was to use the ```-user``` option but the output was not detailed and most had **'Permission denied'** as output. I tried to pipe the output into grep and filter for lines
not containing **'Permission'** but that did not work as intended.


On further reading the ```man ls``` and moving about the server I found the -R option and thought maybe that's what was missing. I also got to know that ls -l output contains the username, group name and file size,
so I tried doing ```ls -lR``` and piping the output to grep to filter (After I had to stop the machine from listing the entire server file list). 


I used grep to filter for the pattern '**bandit7**' and '**33**' using ```ls -lR | grep -E 'bandit7.*33'```. I got 2 files back as result but only one had bandit6 as the group. Thus I navigated to 
/var/lib and using find to try to get the file but it did not show up. After some head scratching I filtered for files of size 33c  using ```find lib/* -size 33c``` and got the location 
of the file under ```lib/dpkg/info/bandit7.password```.



Final password for bandit7: z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

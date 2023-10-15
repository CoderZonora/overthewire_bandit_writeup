1) ```ssh bandit0@bandit.labs.overthewire.org -p 2220```


2) ```cat readme``` -> copy password


3) ```cat ./- ``` as UNIX filenames are legal in this format but cannot be used in commands. -> copy password


4) ```cat spaces\ in \this \filename ``` to make the file name valid to read


5) ```cd inhere``` -> ```ls -a``` to list all files. -> ```cat .hidden```

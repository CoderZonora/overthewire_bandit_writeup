
Commands used: ```find inhere/* -type f -not -executable -size 1033c -> cat inhere/maybeinhere07/.file2``` where f specifies Regualr file like Text and 1033c specifies 1033 bytes file size.


Approach : While serching around for the use of ```file``` and ```find``` command in one of the threads for the last level I got to know that /* infornt of a directory passes the contents
of entire directory to the commmand as input.
Also got to know about the flags such as ```-size -type ``` etc under the find command.

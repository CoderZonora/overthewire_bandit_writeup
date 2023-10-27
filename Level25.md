Tried to script a for loop to echo the password with ```$i``` after opening a ```nc``` shell to **localhost** on port **30002** but 
the script could not echo after connecting to the interactive shell.
So first used the following script to create all the commbinations and store in a txt file. 

```
#! /bin/bash
i=0
while [ $i -lt 20 ]
do
   echo VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i >> t1.txt
   ((++i))
done
```

Then used this script to get the password, after reading a few threads about how to send commands to a interactive shell.


```
#! /bin/bash
cat t1.txt | nc localhost 30002
```

Pass for bandit25: p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d

Knew about nmap so used that to scan open ports in this range.


Used ```nmap localhost -p 31000-32000 | grep -Po '3\d\d\d\d' >> temp.txt``` - get list of open ports
Tried to see if could try to connect to all these ports automaticallyy one by one and store the stdout but need scripting for that. 


This article helped understand what output of a particualr port meant  when using openssl: https://www.liquidweb.com/kb/how-to-test-ssl-connection-using-openssl/


Used chmod 600 to change permissions as temp.txt had open permissions which were not allowed by the ssl protocol.


Could not ssh from inside bandit as that was blocked,so had to use ```scp``` to copy ***temp.txt*** to my machine and logged in as bandit17 by using that as the identity file with the ```-i``` option.





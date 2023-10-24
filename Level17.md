```nmap localhost -p 31000-32000 | grep -Po '3\d\d\d\d' >> temp.txt``` - get list of open ports
Tried dynamic commands but need scripting for that. 


This article helped understand what output of a particualr port meant : https://www.liquidweb.com/kb/how-to-test-ssl-connection-using-openssl/


used chmod 600 to change permissions


could not ssh from inside bandit so had to ssh from my machine local user after logging out by copying the ssh key to my machine





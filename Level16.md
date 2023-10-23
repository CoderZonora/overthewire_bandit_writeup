People often wonder whether SSH uses SSL/TLS for traffic encryption.
The short answer is NO, even though both protocols have much in common, under the hood SSH has its own transport protocol, independent from SSL. 
They are entirely different protocols.
So cannnot use ssh.
google : how to connect to a server using ssl linux. Find about openssl s_client
used ```openssl s_client localhost:30001``` to set a new ssl connection. Then provided password of current level to get password in return.


tried openssl enc but did not know which exact cipher to use to encode and coud not touch new files to use in -in parameter

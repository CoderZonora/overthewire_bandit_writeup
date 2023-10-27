Used cat /etc/passwd | grep bandit26 to find that the shell for bandit26 is /usr/bin/showtext which reads:

```
#!/bin/sh
export TERM=linux
exec more ~/text.txt
exit 0
```

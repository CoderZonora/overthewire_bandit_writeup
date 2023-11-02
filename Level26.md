Used cat /etc/passwd | grep bandit26 to find that the shell for bandit26 is /usr/bin/showtext which reads:

```
#!/bin/sh
export TERM=linux
exec more ~/text.txt
exit 0
```

Saw this video after trying a lot to finally get how to proceed: https://www.youtube.com/watch?v=gFh6iAGgzys


Pass for bandit26: c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1

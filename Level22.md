cron.d file had :
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null

* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
Looked up what it was doing:
@reboot means to do this job at reboot time
Next the user as which the cronjob is done is specified
Next the actual job is specified, which here is a shelll file whose output is going into null so as not to fill mail anything the mailbox of the user which is a feature of cron.

 * * * * * specifies to do this job every minute of every hour of every day of every week of every month.


cat cronjob_bandit22.sh in /usr/bin which was changing all permissions the files to read and write for the owner, read for the group, and read for other users.
It was had ```cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv``` i.e. to sending the output of /etc/bandit_pass/bandit22 to a file in /tmp
cat for this file gave the password for the next level.
Pass for bandit22:WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff

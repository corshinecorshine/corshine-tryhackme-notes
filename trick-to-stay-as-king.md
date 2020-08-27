## Trick to stay as king on KOTH from Tryhackme.

> Method 1
```
#!/bin/bash
while :
do
        eval "echo [usernameHere] >> /root/king.txt"
        eval " > /root/king.txt"
done

#this script is created in 1 min :P
```
> Method 2

```
while [[ $(cat /root/king.txt) != "[usernameHere]" ]]; do echo "[usernamehere]" >> /root/king.txt; done

```
> Method 3 with crontab

`* * * * * echo "[usernameHere]" >> /root/king.txt >/dev/null 2>&1`




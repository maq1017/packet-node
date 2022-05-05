# Overview

To provide basic config for Direwolf with BPQ to work as a virtual TNC2 packet node

## Requirements:
- Linbpq / Pilinbpq
- Minicom
- Direwolf & Hamlib

Start direwolf with the included config file
```
direwolf -c ./direwolf_9700.conf
```
Start linbpq / pilinbpq - I recommend doing this as a background process or in screen, e.g. 
```
screen -d -m sudo ./linbpq
```

Start minicom to connect to Linbpq's virtual com ports, where the com port path is as the first one defined in your bpq32.cfg:
```
minicom -b 19200 -D /home/radio/tnc/com10
```


Additional config under 'node & mailbox' folder is for an unattended packetnode & mailbox which would usually run under a NoV callsign in the UK (e.g. GB7ABC)

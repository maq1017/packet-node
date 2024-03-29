# Overview

To provide Team Wave members basic config for Direwolf with BPQ to work as a virtual TNC2 packet node on Linux platorms

Further updates will provide full instructions for direwolf build  & compile along with hamlib, but for now this is simply a config repository. Please enure the user account you're using for direwolf / linbpq has access to use /dev/tty* devices. Usually an addition to the 'dialout' user group will suffice on Debian/Raspbian distros

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
screen -d -m ./linbpq
```

Start minicom with params to connect to Linbpq's virtual com port, where the com port path is as per the first one defined in your updated bpq32.cfg:
```
minicom -b 19200 -D /home/radio/tnc/com10
```

## Running an unattended packet node & mailbox

Additional config under 'node & mailbox' folder is for an unattended packetnode & mailbox which would usually run under a NoV callsign in the UK (e.g. GB7ABC)

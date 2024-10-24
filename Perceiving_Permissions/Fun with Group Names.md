# Fun with Group Names

## Code

```bash
id
chgrp grp/16266 /flag
cat /flag
```
## Explanation

when I used the id command, I discovered my group name was randomly assigned as grp22807. 
I then used chgrp grp22807 /flag to change the group ownership of the /flag file accordingly.

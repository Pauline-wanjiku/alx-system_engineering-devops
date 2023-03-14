# 0x03. Shell, init files, variables and expansions
### Tasks
#### 0. <o>
**script that creates an alias.**
Name: ls
Value: rm *

```
#!/bin/bash
alias ls ="rm *"
```
**script that prints hello user, where user is the current Linux user.**

```
#!/bin/bash
echo "hello $USER"

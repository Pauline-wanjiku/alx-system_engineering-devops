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

**Add /action to the PATH. /action should be the last directory the shell looks into when looking for a program.**
```
#!/bin/bash
export PATH=$PATH:/action
```

3. If the path be beautiful, let us not ask where it leads
script that counts the number of directories in the PATH.
```
#!/bin/bash
echo $PATH | tr -s ':' '\n' | wc -l
```
4. Global variables
**script that lists environment variables.**
```
printenv
```
5. Local variables
**script that lists all local variables and environment variables, and functions.**
```
#!/bin/bash
set
```

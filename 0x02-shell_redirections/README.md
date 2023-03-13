# 0x02. Shell, I/O Redirections and filters

## Tasks

#### 0. Hello World
**script that prints “Hello, World”, followed by a new line to the standard output**
```
echo -e \#\!/bin/bash "\nHello, World\n" > 0-hello_world
```

#### 1. Confused smiley
**script that displays a confused smiley "(Ôo)'**
```

"\"(Ôo)'"
```

#### 2. Let's display a file
**Display the content of the /etc/passwd file.**

```
cat /etc/passwd
```
#### 3. What about 2?
**Display the content of /etc/passwd and /etc/hosts**

```
cat /etc/passwd /etc/hosts
```
#### 4. Last lines of a file
**Display the last 10 lines of /etc/passwd**

```
tail -n 10 /etc/passwd
```
#### 5. I'd prefer the first ones actually

**Display the first 10 lines of /etc/passwd**
```
#!/bin/bash
head -n 10 /etc/passwd
```
####6-third_line
**script that displays the third line of the file**
```
#!/bin/bash
cat iacta |head -3 | tail -1
```

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
#### 6-third_line
**script that displays the third line of the file**
```
#!/bin/bash
cat iacta |head -3 | tail -1
```
#### 7-file
**script that creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the text Best School ending by a new line.**
```
#!/bin/bash
echo -e "Best School\n" > \\\*\\'"Best School"\'\\*$\?\*\*\*\*\*:\)

```

#### Save current state of directory
**script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it.**
```
#!/bin/bash
ls -la ls_cwd_content
```
#### Duplicate last line
**script that duplicates the last line of the file iacta**
```
#!/bin/bash
tail -1 iacta >> iacta
```
#### 10. No more javascript
**script that deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders.**
```
#!/bin/bash
find . -type f -name "*.js" -delete
```

#### 11. Don't just count your directories, make your directories count
Write a script that counts the number of directories and sub-directories in the current directory.

The current and parent directories should not be taken into account
Hidden directories should be counted

```
#!/bin/bash
find . -type d ! -path . |wc -l
```

#### 12. What’s new
Create a script that displays the 10 newest files in the current directory.

Requirements:

One file per line
Sorted from the newest to the oldest

```
#!/bin/bash
ls -t | head 
```
#### 13. Being unique is better than being perfect
script that takes a list of words as input and prints only words that appear exactly once.

Input format: One line, one word
Output format: One line, one word
Words should be sorted

```

sort | uniq -u     
```

#### 14. It must be in that file

```
grep ^root /etc/passwd

```

#### 15. Count that word
Display the number of lines that contain the pattern “bin” in the file /etc/passwd

```
grep -c "bin" /etc/passwd        

```

#### 16. whatsnext
Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd.

```
#!/bin/bash
grep -A 3 "root" /etc/passwd
```
17. I hate bins
**Display all the lines in the file /etc/passwd that do not contain the pattern “bin”.**
```
#!/bin/bash
grep -v "bin" /etc/passwd
```

18. Letters only please
**Display all lines of the file /etc/ssh/sshd_config starting with a letter.
include capital letters as well**
```
#!/bin/bash
grep ^[:alpha:] /etc/ssh/sshd_config
```

19. A to Z
**Replace all characters A and c from input to Z and e respectively.**
```
#!/bin/bash
tr 'Ac' 'Ze'
```

20. Without C, you would live in hiago
**script that removes all letters c and C from input.**
```
#!/bin/bash
sed 'c/C//'
```

21. esreveR
**script that reverse its input.**
```
#!/bin/bash
rev 
```

22. DJ Cut Killer
**script that displays all users and their home directories, sorted by users.**
```
#!/bin/bash
cat /etc/passwd | cut -d: -f1,6 | sort
```
23. Empty casks make the most noise
**command that finds all empty files and directories in the current directory and all sub-directories:
* Only the names of the files and directories should be displayed (not the entire path)
* Hidden files should be listed
* One file name per line
* The listing should end with a new line
* You are not allowed to use basename, grep, egrep, fgrep or rgrep**

```
#!/bin/bash
find . -empty -printf "%f\n" -type f -o -type d
```

####24. A gif is worth ten thousand words
**script that lists all the files with a .gif extension in the current directory and all its sub-directories.

* Hidden files should be listed
* Only regular files (not directories) should be listed
* The names of the files should be displayed without their extensions
* The files should be sorted by byte values, but case-insensitive (file aaa should be listed before file bbb, file .b should be listed before file a, and file Rona should be listed after file jay)
* One file name per line
* The listing should end with a new line
* You are not allowed to use basename, grep, egrep, fgrep or rgrep**

```
#!bin/bash
find -type f -name "*.gif" -printf "%f\n" | rev | cut -d '.' -f 2- | rev |LC_ALL=C sort -f
```

####25. Acrostic
**script that decodes acrostics that use the first letter of each line.

The ‘decoded’ message has to end with a new line
You are not allowed to use grep, egrep, fgrep or rgrep**

```
#!/bin/bash
cut -c 1 | paste -s -d ''
```

####26. The biggest fan
**script that parses web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests.**

* Order by number of requests, most active host or IP at the top
* You are not allowed to use grep, egrep, fgrep or rgrep
```
#!/bin/bash
tail -n +2 | cut -f -1 | sort -k 1 | uniq -c | sort -rnk 1 | head -n 11 | rev | cut -d ' ' -f -1 | rev    
```                         


# SHELL BASICS

scripts for different commands

1. print the absolute path name of the current working directory
		
		```pwd```

2. Display the contents list of your current directory
	
		```ls```

3. script that changes the working directory to the user’s home directory.
	
		```cd ```


4. Display current directory contents in a long format
		```ls -l```


5. Display current directory contents, including hidden files (starting with .)using the long format.
		
		```ls -a -l```


6. Long format with user and group IDs displayed numerically And hidden files (starting with .)

		```ls -na```

7. script that creates a directory named myfirstdirectory in the /tmp/ directory.
		```mkdir- /tmp/myfirstdirectory```


8. script to Move the file
		
		```mv betty /tmp/myfirstdirectory```


9. remove betty

		```rm /temp/8-firstdelete/betty```

10. changes the working directory to the previous one.

		```cd ..```


11. script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the /boot directory (in this order), in long format.

		```ls -al . .. /boot```


12. script to print type of file

		```file iamafile```


13. script to createe symbolic link

		```ln -s /bin/ls ls```


14. script to create directories

		```mkdir welcome/ welcome/to/ welcome/to/school```


15. script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory.

		```cp -un .html ../```

16. Create a script that moves all files beginning with an uppercase letter to the directory /tmp/u.

		```mv .*/[A-Z]* /tmp/u```

17. script that deletes all files in the current working directory that end with the character ~.

		```rm *~```

18. script that creates the directories welcome/, welcome/to/ and welcome/to/school in the current directory.

		```mkdir -p welcome/to/school```

19. Write a command that lists all the files and directories of the current directory, separated by commas (,).

* Directory names should end with a slash (/)
* Files and directories starting with a dot (.) should be listed
* The listing should be alpha ordered, except for the directories . and .. which should be listed at the very beginning
* Only digits and letters are used to sort; Digits should come first
* You can assume that all the files we will test with will have at least one letter or one digit
* The listing should end with a new line

		```#!/bin/bash```

		```ls -pam```


20. magic file school.mgc that can be used with the command file to detect School data files. School data files always contain the string SCHOOL at offset 0.

		```#!/bin/bash```

		```0 string SCHOOL School data```

		```!:mime School```

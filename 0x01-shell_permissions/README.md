# Shell permission
### Scripts
1. Switch the current user to another user(betty)

		```su betty```

2. print username of current user

       		```whoami```
      
  		```id -u -n```

3. print all the groups the current user is part of.

		```id Gn```	
		```groups```

4. change the file owner (e.g hello to the user betty).

		```sudo chown betty hello```

5.create an empty file called (e.g hello)

		```touch hello```

6.add execute permission to the owner of the file (e.g hello).

		```chmod u+x hello```

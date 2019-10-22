This project consist of all the 4 scenario which are asked in the challenge. Steps to do run the program and some TODO are as below - 


Steps to run the program

1. load the project from git to your any IDE e.g. eclipse.

2. Run the application right click on class SocialApplication and then select Run as ---> java application

3. Now you need to have any client ( for example postman) to hit different endpoints and you can hit different flows, as of requirement we have total 4 flows 
 Posting, Wall, Following, Timeline and we can run this flow as below

	a. Posting 
	
	1. Go to postman and type URL localhost:8080/socialNetworking/{UserName}/post ( request type should be POST )
		here username will be the name of user who is posting the application , it can be anything of type string ( example sunny )
		
	2. write any message below 140 character ( if you wanted to see postive scenario , else write more character and you will get error message).
	
	3. Send this request , you will get success message that your message has posted
	


	b. Wall
	
	1. Go to postman and type URL localhost:8080/socialNetworking/{UserName}/wall ( request type should be GET )
	
	2. hit this service and you will see all messages posted by user in reverse chronological order
	

	c. Following
	
	1. create two different user by using # a. posting  ( two user which will be created are {userName1} and {userName2} )
	
	2. now  in postman go to URL localhost:8080/socialNetworking/{UserName1}/wall ( request type should be POST )
	
	3. As you are login with {userName1} the in body section put other user {userName2} of other user and hit request.
	
	4. You will get success message or error if user doesn't exist.
	
	

	d.Timeline
	
	1. follow all the steps mentioned in # c. Following
	
	2. Go to postman and type URL localhost:8080/socialNetworking/{UserName}/timeline ( request type should be GET )
	
	3. hit the request, you will get all the post of the users which you userName is following

	
TODOs

1. Logging needs to be implemented.
2. in case of timeline we can also show who has posted message and at what time.
3. Unit testing and integration testing needs to be done.
4. Exceptional handling so that we can provide differentiate Error in reqeust and Error from server and sending error message and code accordingly.
5. In case of user in login first time, we need to send code 201, user has craeted.
6. Error code needs to be send in different scenarios. 	
7. We can implement java validations for different fields.
# UiPathDeleteUser
Delete User

This is a Robotic Process Automation(RPA) automation that will log into the orchestrator account of the user and go to the users using the robots. 
It will filter out the users whose robot access status is disabled only if they don't belong to the Administrator Group.
The details of these users is stored in an excel file. 
The automation then performs authentication using Authentication API POST Http request the credentials and obtains the access token.
For each user in the excel sheet their respective username is filtered and the username is in the GET API Http Request to retreive the Id for the user. 
Once the Id is receieved using the DELETE API Http request the user is deleted using the id.
Then the orchestrator list of user is refreshed and the initial user logs out.

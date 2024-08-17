<span style="font-size: 2em; font-weight: bold;">User Role:</span>

## Scenario 1: Register

**Happy Flow:**

Given a new user provides valid registration details (email, password)  
When the user submits the registration request  
Then the user should be successfully registered and receive a confirmation message along with a unique user ID.

**Negative Test 1:**

Given a new user provides an email without a password  
When the user submits the registration request  
Then the registration should fail, and the user should receive an error message indicating that the password is required.

**Negative Test 2:**

Given a new user provides an invalid email format  
When the user submits the registration request  
Then the registration should fail, and the user should receive an error message indicating that the email format is incorrect.

## Scenario 2: Login

**Happy Flow:**

Given a registered user provides valid login credentials (email, password)  
When the user submits the login request  
Then the user should be successfully logged in and receive a session token.

**Negative Test 1:**

Given a user provides incorrect login credentials (wrong password)  
When the user submits the login request  
Then the login should fail, and the user should receive an error message indicating invalid credentials.

**Negative Test 2:**

Given a user tries to log in without providing any credentials  
When the user submits the login request  
Then the login should fail, and the user should receive an error message indicating that both email and password are required.

## Scenario 3: Logout

**Happy Flow:**

Given a logged-in user with a valid session token  
When the user submits a logout request  
Then the user should be successfully logged out, and the session token should be invalidated.

**Negative Test 1:**

Given a user who is not logged in  
When the user submits a logout request  
Then the logout should fail, and the user should receive an error message indicating that no active session exists.

**Negative Test 2:**

Given a logged-in user with an invalid or expired session token  
When the user submits a logout request  
Then the logout should fail, and the user should receive an error message indicating that the session token is invalid.

<span style="font-size: 2em; font-weight: bold;">Admin Role:</span>

## Scenario 4: Update User

**Happy Flow:**

Given an admin provides valid details to update a user's profile (name, job)  
When the admin submits the update request  
Then the user’s profile should be successfully updated, and the admin should receive a confirmation message with updated details.

**Negative Test 1:**

Given an admin provides invalid user details (invalid name format)  
When the admin submits the update request  
Then the update should fail, and the admin should receive an error message indicating invalid input.

**Negative Test 2:**

Given an admin tries to update a non-existent user  
When the admin submits the update request  
Then the update should fail, and the admin should receive an error message indicating that the user was not found.

## Scenario 5: Delete User

**Happy Flow:**

Given an admin wants to delete an existing user  
When the admin submits the delete request with valid user details  
Then the user should be successfully deleted, and the admin should receive a confirmation message.

**Negative Test 1:**

Given an admin tries to delete a user without providing a user ID  
When the admin submits the delete request  
Then the deletion should fail, and the admin should receive an error message indicating that the user ID is required.

**Negative Test 2:**

Given an admin tries to delete a user who does not exist in the system  
When the admin submits the delete request  
Then the deletion should fail, and the admin should receive an error message indicating that the user was not found.

# Auth with Facebook

> ## Data:
* Access Token

> ## Primary flow
1. Get data (name, email, and Facebook ID) from Facebook API.
2. Check if there is an user with the previously received email.
3. Create an account for the user using the data received from Facebook
4. Create an access token from the user ID, with a 30 minutes expiration.
5. Returns generated access token

> ## Alternative flow: User already exists
3. Update the user account with received data from Facebook (Facebook ID and name, but only if the user account doesn't have a namer)

> ## Excepction flow: Invalid or expired token
1. Return an authentication error

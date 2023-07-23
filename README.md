# jwtToken

## Simple example for JWT token usecases


### How to run the code

1. `npm install` or `npm i`
2. `npm run dev` *To start the main server to serve posts*
3. `npm run devAuthToken` *To start the authentication server which runs on port: 4000*

## How does it work
- Server for posts is running on *(Posts)PORT:3000* and Auth server on *(Auth Server)PORT:4000*.
- We can login with Auth server to get the accessToken and refreshToken.
- **/token** is used to get new accessToken on expiration of accessToken
- To completely disable the refreshToken feature, which is typically utilized to generate new access tokens that expire after a certain time interval, you can permanently remove or disable the refreshToken mechanism from your application's code and database. By doing so, the application will no longer use refresh tokens to obtain new access tokens, and the refresh token data will be removed from the database, ensuring it no longer functions as part of the authentication process
- This can be achived by /logout the user
- Once the refresh token is deleted from the DB, User need to re-login to get new *Access Token* and *refresh token (which can then be used to generate new access token)*.

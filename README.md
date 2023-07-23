# jwtToken

## Simple use case for JWT token usecases


### How to run the code

`npm install` or `npm i`
`npm run dev` *To start the main server to serve posts*
`npm run devAuthToken` *To start the authentication server which runs on port: 4000*

- Server for posts is running on 3000 and Auth server on 4000
- We can login with Auth server to get the accessToken and refreshToken
- /token is used to get new accessToken on Forbidden expiration of accessToken
- to completely disable the refreshToken which was used to generate new access token will be removed from the DB
- Once the refresh token is deleted from the DB, User need to re-login to get new refresh token (which can then be used to generate new access token).
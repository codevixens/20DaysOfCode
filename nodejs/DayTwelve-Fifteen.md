## Goals
To secure your Nodejs API

## Summary
Secure all API routes you created for your vending machine service with bearer tokens, this means that any request made to your API without a valid access token should be denied access to the application.

## Deadline
On or before Wednesday 28th of December 2022, 11pm W.A.T.

## Tips
Knowledge of middlewares and bearer tokens are needed for this task

## Instructions
1. Create a new branch called `dev-tokenization` in the repository you created for the vending machine API.
2. Create an additional route called `/api/token/issue`.
3. The request type to this route will be a **POST** request.
4. The **POST** request parameters will contain a valid vending machine user’s **username** and **password**.
5. The route to issue a token should not be protected with a bearer token as this is the entry point to your application.
6. To access any protected route in your API, a bearer token has to be generated first via the api token issue endpoint after which the generated token is copied and used for future requests.
7. It is important to note that this token must not always be generated on accessing any protected route but should only be generated once and used for its lifespan period until it expires.
8. Make sure to cater for the following edge cases **(On Invalid token being passed and on no token being passed)**

## Returned Response
The following response should be returned:

<img width="1114" alt="Screenshot 2022-12-26 at 03 48 17" src="https://user-images.githubusercontent.com/82330194/209493334-51109859-c3c2-4ce6-9f4b-2c327ea60fea.png">



## Technical requirements
1. New branch name for this task will be `dev-tokenization`.
2. Create an additional **POST** endpoint named `api/token/issue`. 

## Nice to have (bonus points)
It would be a bonus if you create a post on either twitter or LinkedIn about your day 12-15 task using the hashtag **#Cdv20DaysOfCode**

## Submitting Your Task
Link to the GitHub repository in the Codevixens Academy slack channel for 20DaysOfCode #Day1215

## Resources
1. [Modern Token Authentication in Node with Express](https://developer.okta.com/blog/2019/02/14/modern-token-authentication-in-node-with-express)
2. [JWT Bearer token authentication for Express JS](https://medium.com/ms-club-of-sliit/jwt-bearer-token-authentication-for-express-js-5e95bf4dead0)
3. [A Complete Guide on How to Build Middleware For Node.js](https://www.turing.com/kb/building-middleware-for-node-js).
4. [How Node JS middleware Works?](https://selvaganesh93.medium.com/how-node-js-middleware-works-d8e02a936113)
5. [Writing middleware for use in Express apps](https://expressjs.com/en/guide/writing-middleware.html)
6. [Middleware in Express.js - GeeksforGeeks](https://www.geeksforgeeks.org/middleware-in-express-js/)


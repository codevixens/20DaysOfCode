## Goals
Add edge cases to your Nodejs API

## Summary
Secure all admin API routes, this means that any request made to the admin API endpoints won’t go through as the user does not have enough access.

## Deadline
On or before Thursday 28th of December 2022, 11pm W.A.T.

## Instructions
- Create a new branch called `dev-admin-protection` in the repository you created for the vending machine API.
- Create a super-admin user with the following credentials:
  - `username: admin`
  - `password: ADMINPASS`
  - `role: Admin`
- On accessing any of the routes below, if you are not an Admin (i.e role != Admin), a 401 unauthorised error must be returned.
  - `api/vd/user` **DELETE** endpoint.
  - `api/vd/buyer` **DELETE** endpoint.
  - `api/vd/seller` **DELETE** endpoint.
- If you are a buyer, you must not be able to access the following routes:
  - `api/vd/users/list` **GET** endpoint
  - `api/vd/buyers/list` **GET** endpoint
- If you are a seller, you must not be able to access the following routes:
  - `api/vd/users/list` **GET** endpoint
  - `api/vd/buyers/list` **GET** endpoint
- If you are a buyer, you should be able to access this route
  - `api/vd/seller/{uuid}` **GET** endpoint
- You must only be able to deposit coins if you are a buyer.
- You must only be able to refresh your deposit if you are a buyer.

## Returned Response
The following response should be returned:

<img width="1116" alt="Screenshot 2022-12-26 at 03 51 17" src="https://user-images.githubusercontent.com/82330194/209493919-70a66076-0da2-498e-8b3e-cda601d5f49f.png">

## Technical requirements
New branch name for this task will be `dev-admin-protection`

## Nice to have (bonus points)
It would be a bonus if you create a post on either twitter or LinkedIn about your day 16-19 task using the hashtag #Cdv20DaysOfCode

## Submitting Your Task
Link to the GitHub repository in the Codevixens Academy slack channel for 20DaysOfCode #Day1619

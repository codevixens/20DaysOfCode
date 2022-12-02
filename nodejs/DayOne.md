## Day 1
<img src="https://img.freepik.com/free-vector/cartoon-vending-machines-collection_52683-73161.jpg?w=2000">

### Goals
To see how well you can structure a database if given the opportunity.

### Deadline
Saturday 3rd of December 2022, 12pm W.A.T.

### Summary
Design a database diagram for a vending machine that allows users with a role of “seller” to add, update or remove products, while users with a role of “buyer” role can deposit coins into the machine and make purchases. 

### Instructions
- Create a Github repository with the name Vending Machine Api
- In the repository, create a folder with the name .diagrams
- Clone the repository to your local machine
- Create a database diagram for a vending machine using dbdiagram tool
- Make sure to create a relationship between the diagrams.
- On completion, export the final diagram to your local machine and save it in the .diagrams folder you created earlier.
- Rename the exported diagram to ‘database’.
- On completion of the above, push your changes to Github.

### Database Diagram Tool
https://dbdiagram.io/home

<br/>

### Database Table Structure

Table: `users`
| Name | Type | Comments |
| --- | --- | --- |
| `id` | autoincrement |  |
| `uuid` | string | UUID to allow easy migration between envs without breaking FK in the logic |
| `username` | string |  |
| `role` | string | If the user is a seller or buyer. |
| `password` | string | hjdkjsd |
| `created_at` | timestamp |  |
| `updated_at` | timestamp |  |

<br/>

Table: `products`
| Name | Type | Comments |
| --- | --- | --- |
| `id` | autoincrement |  |
| `uuid` | string | UUID to allow easy migration between envs without breaking FK in the logic |
| `title` | string | Title of the product  |
| `cost` | string | Price of the product |
| `sellerId` | string | ID of the seller who created the product |
| `created_at` | timestamp |  |
| `updated_at` | timestamp |  |
| `deleted_at` | timestamp |  |
 
 <br/>

Table: `deposits`
| Name | Type | Comments |
| --- | --- | --- |
| `id` | autoincrement |  |
| `uuid` | string | UUID to allow easy migration between envs without breaking FK in the logic |
| `buyerId` | string | ID of the buyer  |
| `amount` | string | How much the product was bought for |
| `created_at` | timestamp |  |
| `updated_at` | timestamp |  |

### Technical requirements
- The name of the Github repository must be Vending Machine Api.

### Nice to have (bonus points)
- It would be nice to have additional fields to the table models if you may.
- A readme.md file containing information about the project.
- Make a post about your progress for Day1 on either Twitter or LinkedIn with the hashtag #Cdv20DaysOfCode.

### Submitting Your Code
- When you are finished with creating the webpage, submit the following:
- Link to the Github repository in the Codevixens Academy slack channel for 20DaysOfCode #Day1
- Link to a your social media post made of your progress.. If any

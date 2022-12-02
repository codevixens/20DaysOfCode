## Day 1

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


Table: `deposits`
| Name | Type | Comments |
| --- | --- | --- |
| `id` | autoincrement |  |
| `uuid` | string | UUID to allow easy migration between envs without breaking FK in the logic |
| `buyerId` | string | ID of the buyer  |
| `amount` | string | How much the product was bought for |
| `created_at` | timestamp |  |
| `updated_at` | timestamp |  |



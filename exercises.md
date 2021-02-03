1) What are some resources offered by https://www.balldontlie.io?

GET https://www.balldontlie.io/api/v1/players

2) What are some resources offered by facebook (or another popular social media platform that you've interacted with)
business platform/marketing platform/large shop with thousand of potential buyers or supplier. audience for many good practice

3) What actions are allowed on each of these resources?

4) What are the 4 main HTTP verbs?
POST,GET PATCH AND DELETE

5) What is the difference between these two requests: `GET http://made-up-api.com/books/11` and `PUT http://made-up-api.com/books/11`?

FIRST REQUEST WILL See all available instances for the resource and SECOND REQUEST WILL Update an existing instance of the resource

6) Complete the table below. It refers to actions on the wines resource.

| Action                   | Nickname | Route       | HTTP Verb |
|See all available instances for the wine|Index|/{wine}|GET|

| | See all available wine_|Index   | /wine    |  GET
| See details about 1 wine | __Show |/wine/:id | _GET____|
| Create a new wine        | Create | _/wine__ | _POST|
| _update an existing wine | Update | _/wine:id|  PUT     |
| _Delete an existing wine_| Delete | /wine/:id| _DELETE_|


7) Complete this table about actions on the pets resource.

| Action                  | Nickname | Route     | HTTP Verb    |
|---         --------|----------|-----------|-----------        |
| See all available pets  | Index    | _/pets___|GET____        |
| See detail about 1 specific pet____| Show     |/pets/:id_| GET|
| Create a new instance of pets______| Create___|/pets | POST   |
| Update an existing pets | __update_| /pets/:id| PUT____       |
| Delete an existing pets  | _Delete_| /pets/:id| DELETE        |

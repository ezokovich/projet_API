# How to Use Our APIs

## Table of Contents
- [Introduction](#introduction)
- [Endpoints](#endpoints)
  - [Request methods](#request-methods)
  - [Examples](#examples)
- [Real-time example](#real-time_example)







 ## Introduction
 
this document is a simple documentation of the API. 
<br> the following will be dedicated to how to test it with different
<br> methods and types of Status Codes.


### Endpoints
Endpoints with literal and readable URLs is what makes an API great. To make it easy and convenient for you, we've specified how you should do it. You don't have to worry about whether you should use the plural or ":" anymore...



### request-methods


The request method is how we distinguish the type of action we are "asking" our endpoint to perform. For example, the GET method stands on its own. But we also have a few other methods that we use quite often. such as Post put ... .
| Method   | Description                              |
| -------- | ---------------------------------------- |
| `GET`    | Used to retrieve information about a player. |
| `POST`   | Used when inserting in the database a new data, for example the name and information of a new footballer |
| `PUT`    |Used to replace an entire element (all fields) with new data. For example, changing the age or number of wins (etc ...) of a player  |
| `DELETE` | Used to delete an item.                  |




### Examples

Now that we’ve learned about  the different request methods that we should use, it’s time for some examples:




| Method   | URL                                      | Description                              |
| -------- | ---------------------------------------- | ---------------------------------------- |
| `GET`    | `/api/v1/stats/id`                          | Retrieve all information from the player with the selected id.                      |
| `POST`   | `/api/v1/stats`                             | Create a new post.                       |
| `PUT`    | `/api/v1/stats/id`                          | edit post id.                       |
| `DELETE`   | `/api/v1/stats/id`                       | DELETE post id.                 |







## real-time_example

*`GET` method : <br>

   -- get the information of the players with id = 10

```
https://fathomless-depths-63942.herokuapp.com/api/v1/stats/10
```



```


 {
    "id": 10,
    "wins": 99,
    "losses": 0,
    "points_scored": 7869,
    "nom": "Messi",
    "surnom": "le genie"
}
```



*`POST` method : <br>

  -- Create a new post with id = 20
```
https://fathomless-depths-63942.herokuapp.com/api/v1/stats
```


```


 {
    "id": 20,
    "wins": 99,
    "losses": 3,
    "points_scored": 789,
    "nom": "Adebayor Emmanuel Shei",
    "surnom": "SEA"
}
```

*`PUT` method : <br>

-- edit post with id = 20

```
https://fathomless-depths-63942.herokuapp.com/api/v1/stats/20
```

```

  {
    "id": 20,
    "wins": 99,
    "losses": 45,
    "points_scored": 34,
    "nom": "Adebayor Shei",
    "surnom": "SEA"
}
```

*`DELETE` method : <br>

 -- Delete a post with id = 20
 
 ```
 
 ```
   
`Code 200`  to let you know that you have indeed deleted the post  <br>
   
   
## Status Codes

the status codes and their meaning if you see them on the postman test or other test :


| Code  | Title                     | Description                              |
| ----- | ------------------------- | ---------------------------------------- |
| `200` | `OK`                      | When a request was successfully processed (e.g. when using `GET`, `PATCH`, `PUT` or `DELETE`). |
| `201` | `Created`                 | Every time a record has been added to the database (e.g. when creating a new user or post). |
| `404` | `Not found`               | When URL or entity is not found. |
| `500` | `Internal server error`   | When an internal error has happened (e.g. when trying to add/update records in the database fails). |








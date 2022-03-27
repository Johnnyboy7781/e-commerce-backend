# E-commerce Back End 🛒
![Heroku](https://pyheroku-badge.herokuapp.com/?app=mysterious-garden-76426)

## Purpose
The back end of a theoretical e-commerce site. Interact with the database at the heroku deployment. Add new items, categories, and tags!

## Demo
Check out this quick demo before interacting with the API: https://www.youtube.com/watch?v=ibyqWmZzt2w&ab_channel=JonathanMcDonnell

## Deployment
Use this route when making requests: https://mysterious-garden-76426.herokuapp.com/api/

## Routes 📍
### READ/GET
Get requests can be made for categories, tags, and products. To make a get request, simply append the type of data you would like to retrieve.  
Example request to GET all categories: ```https://mysterious-garden-76426.herokuapp.com/api/categories```

Optionally, you can suppply an id to the end to get one specificed item.  
Example request to GET a product with an id of 1: ```https://mysterious-garden-76426.herokuapp.com/api/products/1```

### CREATE/POST
Create new data with a POST request. Make a request to the url and append it with the type of data you would like to create (new category, tag, or product). In the request body, supply the necessary information. Please follow the schema below:

#### New Category
```
{
    "category_name": "<category name>"
}
```

#### New Tag
```
{
    "tag_name": "<Tag name>"
}
```

#### New Product
```
{
    "product_name": "<Product name>",
    "price": <price>,
    "stock": <stock>,
    "category_id": <Id of category product belongs to>,
    "tagIds": [<Id of associated tag>, <Id of associated tag>, ...]
}
```

### UPDATE/PUT
Update data with a PUT request. Make a request to the url and append it with the type of data you would like to update. 

For updating categories, tags, and products, simply make a PUT request with a request body that includes the data that you would like to update.   
For products, the ```tagIds``` field in the request body is required.

### DELETE
Delete data from the database with a DELETE request. Make a request to the url and append it with the type of data and the id of the data you would like to delete.  
Example request to delete a tag with an id of 1: ```https://mysterious-garden-76426.herokuapp.com/api/tags/1```

## Built with
* Javascript
* Node
* Heroku
* Express
* MySQL
* MySQL2
* Sequalize
* dotenv

## Contribution
Made with ❤️ by Jonathan McDonnell



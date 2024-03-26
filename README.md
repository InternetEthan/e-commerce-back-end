# E-Commerce Back End

This project is a back end for an e-commerce site. It uses Express.js API and Sequelize to interact with a MySQL database.

## Installation
1. Clone the repository to your local machine.
2. Run `npm install` to install all dependencies.
3. Create a `.env` file in the root of your project with the following variables:
   ```
   DB_NAME='ecommerce_db'
   DB_USER='your_mysql_username'
   DB_PW='your_mysql_password'
   ```
4. Run `npm run seed` to seed data to your database.
5. Run `npm start` to start the server.

## Usage
This application doesn't have a front end yet. You can test the routes with API testing tools such as Postman or Insomnia.

## API Routes
### Categories
- GET /api/categories - Get all categories.
- GET /api/categories/:id - Get a single category by its id.
- POST /api/categories - Add a new category.
- PUT /api/categories/:id - Update a category by its id.
- DELETE /api/categories/:id - Delete a category by its id.

### Products
- GET /api/products - Get all products.
- GET /api/products/:id - Get a single product by its id.
- POST /api/products - Add a new product.
- PUT /api/products/:id - Update a product by its id.
- DELETE /api/products/:id - Delete a product by its id.

### Tags
- GET /api/tags - Get all tags.
- GET /api/tags/:id - Get a single tag by its id.
- POST /api/tags - Add a new tag.
- PUT /api/tags/:id - Update a tag by its id.
- DELETE /api/tags/:id - Delete a tag by its id.

## Models
The application has four models:
- Product
- Category
- Tag
- ProductTag

### Associations
- Product belongs to Category, and Category has many Product models, as a category can have multiple products but a product can only belong to one category.
- Product belongs to many Tag models, and Tag belongs to many Product models. This is a many-to-many relationship where a product can have multiple tags and a tag can have many products.
- The ProductTag model is used to create a through relationship between Product and Tag.

## Seeding
The seeds directory contains seed files for Product, Category, Tag, and ProductTag that you can use to seed your database using the `npm run seed` command.

## Technologies
- Node.js
- Express.js
- MySQL2
- Sequelize
- Dotenv

## License
This project is licensed under the terms of the MIT license.

Starter Code: [https://github.com/coding-boot-camp/fantastic-umbrella](https://github.com/coding-boot-camp/fantastic-umbrella)
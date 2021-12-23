# 13 Object-Relational Mapping (ORM): E-Commerce Back End

## E-Commerce Back End

This progam is for managers at internet retail company, especially the owners of Culture Cross Jewelery and have requested for the creator of this program to make them something that could be used in their online business and will see the program in 2022. Simply, it is a back end for an e-commerce website that uses the latest technologies.

A demonstration of this video can be seen at https://youtu.be/sCG6JXy2rRM.

## Operations/Rough How to Guide

WHEN the user adds their database name, MySQL username, and MySQL password to an environment variable file, then that user is able to connect to a database using Sequelize
Futhermore when a user enters schema and seed commands, then a development database is created and is seeded with test data. When user enters the command to invoke the application, then the server is started and the Sequelize models are synced to the MySQL database
Finally, when the user opens API GET routes in Insomnia Core for categories, products, or tags
THEN the data for each of these routes is displayed in a formatted JSON
WHEN I test API POST, PUT, and DELETE routes in Insomnia Core
THEN I am able to successfully create, update, and delete data in my database
```
The above Youtube video demonstrations how to operate these functions and again can be found at https://youtu.be/sCG6JXy2rRM.

### Database Models

THE CREATED DATABASE FOLLOWS THE FOLLOWING MODELS AND WERE A HELPFUL STARTING POINT.

* `Category`
  * `id`
    * Integer.
    * Doesn't allow null values.
    * Set as primary key.
    * Uses auto increment.

  * `category_name`
    * String.
    * Doesn't allow null values.

* `Product`
  * `id`
    * Integer.
    * Doesn't allow null values.
    * Set as primary key.
    * Uses auto increment.

  * `product_name`
    * String.
    * Doesn't allow null values.

  * `price`
    * Decimal.
    * Doesn't allow null values.
    * Validates that the value is a decimal.

  * `stock`
    * Integer.
    * Doesn't allow null values.
    * Set a default value of `10`.
    * Validates that the value is numeric.

  * `category_id`
    * Integer.
    * References the `Category` model's `id`.

* `Tag`
  * `id`
    * Integer.
    * Doesn't allow null values.
    * Set as primary key.
    * Uses auto increment.

  * `tag_name`
    * String.

* `ProductTag`
  * `id`
    * Integer.
    * Doesn't allow null values.
    * Set as primary key.
    * Uses auto increment.

  * `product_id`
    * Integer.
    * References the `Product` model's `id`.

  * `tag_id`
    * Integer.
    * References the `Tag` model's `id`.

## Associations

All the require association methods on your Sequelize models executed.

## Grading Fufillments.
All the grading requirements have been fufilled and are listed below. 

### Deliverables: 10%
*This GitHub repository contains my application code.

### Walkthrough Video: 37%
*The video walkthrough can be found at https://youtu.be/sCG6JXy2rRM and demonstrates all of the following.

* A walkthrough video that demonstrates the functionality of the e-commerce back end must be submitted, and a link to the video should be included in your readme file.
* The walkthrough video shows all of the technical acceptance criteria being met.
* The walkthrough video demonstrate how to create the schema from the MySQL shell.
* The walkthrough video demonstrate how to seed the database from the command line.
* The walkthrough video demonstrates how to start the application’s server.
* The walkthrough video demonstrates GET routes for all categories, all products, and all tags being tested in Insomnia Core.
* The walkthrough video demonstrates GET routes for a single category, a single product, and a single tag being tested in Insomnia Core.
* The walkthrough video demonstrates POST, PUT, and DELETE routes for categories, products, and tags being tested in Insomnia Core.

### Technical Acceptance Criteria: 40%
* This program satisfies all of the preceding acceptance criteria plus the following:
  * Connects to a MySQL database using the [MySQL2](https://www.npmjs.com/package/mysql) and [Sequelize](https://www.npmjs.com/package/sequelize) packages.
  * Stores sensitive data, like a user’s MySQL username, password, and database name, using environment variables through the [dotenv](https://www.npmjs.com/package/dotenv) package.
  * Syncs Sequelize models to a MySQL database on the server start.
  * Includes column definitions for all four models outlined in the homework instructions.
  * Includes model associations outlined in the homework instructions.

### Repository Quality: 13%
* Repository has a unique name.
* Repository follows best practices for file structure and naming conventions.
* Repository follows best practices for class/id naming conventions, indentation, quality comments, etc.
* Repository contains multiple descriptive commit messages.
* Repository contains quality readme with description and a link to a walkthrough video.

## Review
* A walkthrough video demonstrating the functionality of the application and all of the acceptance criteria being met. That video can be found at https://youtu.be/sCG6JXy2rRM.
* The URL of the GitHub repository. Give the repository a unique name and include a readme describing the project.
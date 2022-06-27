# Cinema App

![](https://filmcycle.files.wordpress.com/2012/07/movie_theater_1.jpg)

Project Description
-------------
This is a Hibernate and Spring-based cinema web application. Customers must log in to the application using their credentials to be able to perform CRUD-operations relating to the purchase of cinema tickets.

Functional areas of this application that users can access and the scope of activities that they can perform in those areas depend on their user role.

Features
-------------
Cinema App stores data about movies, cinema halls, movie sessions, users, user roles, tickets, shopping carts and orders in a relational database managed by MySQL. The app has both authentication and authorization features.

Everyone has access to the following pages: `/register` and `/login`

Both `Users` and `Admins` can perform the following operations:

Get a list of all movies (`GET: /movies`), get a list of all cinema halls (`GET: /cinema-halls`),
get all movie sessions by a movie's id (`GET: /movie-sessions/{id}`),
get a list of all of the movies shown in the cinema on any day (`GET: /movie-sessions/available`).

Only `Users` can perform the following operations:

Get a list of all the orders made by a user (`GET: /orders`), get your shopping cart (`GET: /shopping-carts/by-user`), add your order (`POST: /orders/complete`), change a movie session from your shopping cart by a movie session's id (`PUT: /shopping-carts/movie-sessions`).

Only `Admins` can perform the following operations:
Add a movie (`POST: /movies`), add a movie session (`POST: /movie-sessions`), add a cinema hall (`POST: /cinema-halls `), get a user by email (`GET: /users/by-email`), change a movie session by its id (`PUT: /movie-sessions/{id}`), delete a movie session by its id (`DELETE: /movie-sessions/{id}).`


Technology Stack
-------------
- Java 11
- Hibernate
- Spring (Core, Web, Security)
- MySQL
- Apache TomCat 9.0.50
- Maven

Getting Started
-------------
In order to run this application, install MySQL and Apache TomCat 9.0.50 on your computer and follow the instructions listed below:
1. Clone this project.
2. Create a schema in MySQL.
3. Create a connection to your database in the `resources` directory (`db.properties`) by using your credentials.
4. Configure TomCat. Use `/` as your application context path.
5. You can now run this application by using a TomCat local server.
6. You can use credentials defined in the `DataIntializer` class to log in as `Admin`. In order to log in as `User`, you can either use the credentials defined in the above class or create a new account.
7. Use Postman or any other Software to send HTTP-requests and receive HTTP-responses.
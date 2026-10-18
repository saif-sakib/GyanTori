# GyanTori — Peer-to-Peer Book Sharing

A desktop virtual library where students lend, borrow and catalog books with each other.
Built as a team project at MIST for 500+ students.

## Features

- Sign up, log in and edit your profile
- Explore and search the shared catalog, with book details and reviews
- Share your own books with the library
- Cart and a personal dashboard
- MongoDB schema for inventory relationships and transaction history

## Stack

Java 17 · JavaFX 17 (FXML) · Maven · MongoDB (Java driver) · Jackson

## Run it

Requirements: JDK 17+ and Maven.

```bash
cd bookshop
export MONGODB_URI="mongodb+srv://<user>:<password>@<cluster>/"   # your own MongoDB connection string
mvn clean javafx:run
```

The app reads its database connection from the `MONGODB_URI` environment variable and uses the
`gyantori` database. Never commit a real connection string.

## Project layout

```
bookshop/src/main/java/com/
  controllers/   JavaFX screen controllers (login, explore, cart, dashboard, ...)
  database/      MongoDB access (DatabaseManager, collections)
  models/        Book, Review
  services/      cart, search, session, book API
  start/App.java entry point
bookshop/src/main/resources/com/   FXML views
```

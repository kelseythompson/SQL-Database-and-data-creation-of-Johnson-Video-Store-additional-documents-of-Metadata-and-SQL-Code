# Johnson Video Store Database Schema

## Project Summary

In this milestone, regarding the **Johnson Video Store**, I provide the schema/data dictionary, SQL code for creating tables, and the seeding of the database. This repository contains:

- **Schema/Data Dictionary**: A detailed structure of all tables and their relationships.
- **SQL Code**: SQL files for creating tables in PostgreSQL and seeding the database.
- **Metadata**: Metadata is provided in an attached Excel file for better understanding of the table structure and column definitions.
- **Screenshots**: Visuals showing the successful execution of the code for table creation and database seeding in PostgreSQL.
  
The database is seeded with 20 rows of data for each table to ensure that it is functional and fully populated for testing purposes.

## Database Schema Overview

The **Johnson Video Store** database schema consists of **15 tables**, focusing on **one-to-many** and **many-to-many** relationships to efficiently manage inventory, sales, customer data, and distributor details.

### One-to-Many Relationships

These tables hold unique references that describe characteristics of the store’s data:
- **Version**: Contains information about the versions of movies available.
- **Studio, Country, Languages, Genre, Director**: Lookup/reference tables with attributes for each movie.
- **Foreign Keys**: These reference attributes are linked to the `Movie` table.

### Many-to-Many Relationships

Many-to-many relationships are handled through **bridge tables**, which are used to link multiple entities:
- **Bridge Tables**:
    - `Bridge_Awards`: Links awards to movies.
    - `bridge_genre` and `bridge_language`: Connects movies to multiple genres and languages.
    - `Actors`: Associates actors with the movies in which they participate.

### Inventory and Catalog Management

- **Inventory**: Tracks movie versions, stock levels, costs, and quantities from various distributors.
- **Catalog**: Provides detailed information about movie formats, prices, and availability.

### Sales and Orders

- **Sales**: Manages rental transactions, including dates for rental and return.
- **Orders**: Tracks the process of ordering movies from distributors and includes associated fees, costs, and discounts.

## Usage Instructions

### Setting Up the Schema

1. Clone this repository to your local machine.
2. Run the provided SQL files to create the tables and set up relationships in your PostgreSQL database.

### Seeding the Database

- Execute the provided seeding script to insert 20 rows of sample data into each table.

## Conclusion

This database structure supports the operations of **Johnson Video Store** by efficiently handling data related to movie inventory, rental orders, customer transactions, and distributor relations. It provides a scalable solution that can be easily extended to meet future business requirements.

---

Feel free to reach out if you have any questions or suggestions for improvements!


# Hajj Management Database System

## Project Overview
This project is a relational database system designed for managing Hajj operations and pilgrim information.  
The database was built using SQLite and Python, and includes multiple related tables such as pilgrims, companies, camps, houses, contracts, arrivals, inspectors, and violations.

The project demonstrates:

- Database design using ERD  
- Table creation using SQL (DDL)  
- Primary Keys and Foreign Keys  
- Relationships between tables  
- Data generation using Faker  
- SQL queries and JOIN operations  
- Data analysis using COUNT and GROUP BY  

---

## Technologies Used
- Python  
- SQLite  
- Pandas  
- Faker  
- Google Colab  
- DB Browser for SQLite  
- dbdiagram.io  

---

## Database Tables
The database contains the following tables:

- Pilgrims  
- Companies  
- Nationalities  
- Camps  
- Houses  
- Arrivals  
- Inspectors  
- Violations  
- Contracts  

---

## Database Relationships
The tables were connected using Primary Keys (PK) and Foreign Keys (FK) to maintain data integrity and establish relationships between entities.

### Example relationships:
- Pilgrims → Companies  
- Pilgrims → Nationalities  
- Pilgrims → Arrivals  
- Companies → Contracts  
- Contracts → Camps  
- Contracts → Houses  
- Inspectors → Violations  

### Important note:
Pilgrims do not contain `camp_id` or `house_id`.

The correct relationship is:

> Pilgrim → Company → Contract → Camp / House  

---

## Data Generation
Fake realistic data was generated using the Faker library for:

- Pilgrims  
- Companies  
- Contracts  
- Violations  
- Camps  
- Houses  
- Arrivals  
- Inspectors  

The generated data was inserted into the SQLite database using Pandas.

---

## SQL Queries
Several SQL queries were implemented to test database relationships and data retrieval, including:

- Retrieving pilgrims with company, contract, camp, and house information  
- Retrieving violations with inspector and company information  
- Counting violations for each company  
- Counting pilgrims in each camp and house  
- INNER JOIN between Pilgrims and Companies tables  

---

## Files Included
- `hajj_database.db` → SQLite database file  
- `project_code.ipynb` → Python/SQL implementation  
- `report.pdf` → Project report  
- `ERD.png` → Entity Relationship Diagram  

---

## Project Goal
The goal of this project is to demonstrate the design and implementation of a relational database system using SQL and Python while applying database relationships and query operations in a realistic Hajj management scenario.

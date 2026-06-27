# Football Ticket Booking System

A PostgreSQL database project for managing football ticket bookings. This project includes database schema design, an Entity Relationship Diagram (ERD), sample data insertion, and SQL queries demonstrating filtering, joins, subqueries, aggregation, and pagination.

---

## 📌 Project Overview

The Football Ticket Booking System allows football fans to purchase tickets for different matches while administrators manage match information and ticket availability.

The project consists of three relational database tables:

* **Users** – Stores customer and ticket manager information.
* **Matches** – Stores football match details.
* **Bookings** – Stores ticket booking records and connects users with matches.

---

## 🗂 Database Schema

### Users

| Column       | Description                    |
| ------------ | ------------------------------ |
| user_id      | Primary Key                    |
| full_name    | User's full name               |
| email        | Unique email address           |
| role         | Football Fan or Ticket Manager |
| phone_number | Contact number                 |

### Matches

| Column              | Description           |
| ------------------- | --------------------- |
| match_id            | Primary Key           |
| fixture             | Match fixture         |
| tournament_category | Competition name      |
| base_ticket_price   | Standard ticket price |
| match_status        | Match availability    |

### Bookings

| Column         | Description            |
| -------------- | ---------------------- |
| booking_id     | Primary Key            |
| user_id        | Foreign Key → Users    |
| match_id       | Foreign Key → Matches  |
| seat_number    | Allocated stadium seat |
| payment_status | Booking payment status |
| total_cost     | Total booking amount   |

---

## 🔗 Entity Relationship Diagram (ERD)

The database follows these relationships:

* One User → Many Bookings
* One Match → Many Bookings
* Users and Matches are connected through the Bookings table.

ERD Image:

```
ERD/football-ticket-booking-erd.png
```

---

## 💾 Database Features

* Primary Keys
* Foreign Keys
* Unique Constraints
* CHECK Constraints
* Referential Integrity
* Sample Data Seeding

---

## 📊 SQL Queries Included

The project contains solutions for the following SQL queries:

1. Retrieve available Champions League matches.
2. Search users using `ILIKE`.
3. Handle NULL payment status using `COALESCE`.
4. Retrieve booking information using `INNER JOIN`.
5. Display all users with booking information using `LEFT JOIN`.
6. Find bookings with total cost above average using a subquery.
7. Retrieve the top expensive matches using `LIMIT` and `OFFSET`.

---

## 🛠 Technologies Used

* PostgreSQL
* SQL
* Draw.io (ERD)

---

## 📂 Repository Structure

```
Football-Ticket-Booking-System
│
├── QUERY.sql
├── README.md
├── ERD/
│   └── football-ticket-booking-erd.png
```

---

## 🚀 How to Run

1. Clone the repository.

```bash
git clone https://github.com/ashikurahman1/Football-Ticket-Booking-System.git
```

2. Open PostgreSQL.

3. Execute the `QUERY.sql` file.

4. Run the SQL queries included at the end of the file.

---

## 👨‍💻 Author

**Mohammad Ashikur Rahman**

GitHub: https://github.com/ashikurahman1

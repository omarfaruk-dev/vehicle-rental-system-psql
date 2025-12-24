# VEHICLE RENTAL SYSTEM - Database Design & SQL Queries

---

## 📋 Business Logic

### Users Table:
- User role (Admin or Customer)
- Name, email, password, phone number
- Each email must be unique (no duplicate accounts)

### Vehicles Table:
- Vehicle name, type (car/bike/truck), model
- Registration number (must be unique)
- Rental price per day
- Availability status (available/rented/maintenance)

### Bookings Table:
- Which user made the booking (link to Users table)
- Which vehicle was booked (link to Vehicles table)
- Start date and end date of rental
- Booking status (pending/confirmed/completed/cancelled)
- Total cost of the booking

---

## 🔍 SQL Queries

### Query 1: INNER JOIN
**Retrieve booking information along with:**
- Customer name
- Vehicle name

**Concepts used:** INNER JOIN

---

### Query 2: NOT EXISTS
**Find all vehicles that have never been booked.**

**Concepts used:** NOT EXISTS

---

### Query 3: WHERE
**Retrieve all available vehicles of a specific type (e.g. cars).**

**Concepts used:** SELECT, WHERE

---

### Query 4: GROUP BY and HAVING
**Find the total number of bookings for each vehicle and display only those vehicles that have more than 2 bookings.**

**Concepts used:** GROUP BY, HAVING, COUNT

---

## 📊 Database Relationships

- **Users → Bookings**: One-to-Many (One user can make multiple bookings)
- **Vehicles → Bookings**: One-to-Many (One vehicle can have multiple bookings)

---

## 🗂️ Tables Structure

### Users
- id (Primary Key)
- user_role
- name
- email (Unique)
- password
- phone_number

### Vehicles
- vehicle_id (Primary Key)
- name
- type
- model
- registration_number (Unique)
- rental_price
- status

### Bookings
- booking_id (Primary Key)
- user_id (Foreign Key → Users)
- vehicle_id (Foreign Key → Vehicles)
- start_date
- end_date
- status
- total_cost

---

## 🚀 Installation

### Create Database:
```bash
CREATE DATABASE vehicle_rental_system;
\c vehicle_rental_system
\i queries.sql
```

---

**Links:**
- GitHub Repository: https://github.com/omarfaruk-dev/vehicle-rental-system-psql
- ERD: https://drawsql.app/teams/mcl-3/diagrams/vehicle-rental-system

---

## 📞 Contact

**Email:** [omar@brightfuturesoft.com]  
**GitHub:** [github.com/omarfaruk-dev]

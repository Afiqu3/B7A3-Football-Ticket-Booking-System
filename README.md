# Football Ticket Booking System

This project contains a SQL database setup template for a simple football ticket booking system. It defines tables for users, matches, and bookings, inserts sample data, and includes example queries for common reporting needs.

## Database Schema

- `Users`
  - `user_id` (primary key)
  - `full_name`
  - `email`
  - `role` (`Ticket Manager` or `Football Fan`)
  - `phone_number`

- `Matches`
  - `match_id` (primary key)
  - `fixture`
  - `tournament_category`
  - `base_ticket_price`
  - `match_status` (`Available`, `Selling Fast`, `Sold Out`, `Postponed`)

- `Bookings`
  - `booking_id` (primary key)
  - `user_id` (foreign key to `Users`)
  - `match_id` (foreign key to `Matches`)
  - `seat_number`
  - `payment_status` (`Pending`, `Confirmed`, `Cancelled`, `Refunded`)
  - `total_cost`

## Sample Data

The SQL script seeds:
- 4 users
- 5 matches
- 5 bookings

## Included Queries

1. Retrieve available Champions League matches.
2. Search users by name patterns.
3. Find bookings with missing payment status and label them `Action Required`.
4. Join bookings with user and match details.
5. List all users with booking IDs, including users without bookings.
6. Find bookings with total cost above the average booking cost.
7. Retrieve the 2 most expensive matches, skipping the highest-priced match.

## Usage

Run the SQL script in your database environment to create the tables, insert sample data, and execute the sample queries.

## Notes

- Replace placeholder types and constraints with actual production-ready definitions if needed.
- Ensure referential integrity by loading data in the correct order: `Users`, `Matches`, then `Bookings`.

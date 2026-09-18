# Problem Statement

## What's the problem?

Most small car rental shops still keep track of their cars and bookings on
paper or in a random Excel sheet. This causes a lot of issues in real life -
sometimes the same car gets rented out to two people because nobody checked
if it was already booked, and calculating the final bill (especially for
premium cars that cost extra per day) is done manually and can go wrong.
There's also no proper record of past rentals, so if someone asks "who
rented this car last month" there's no easy way to check.

For this project I built a **Car Rental Management System** in Java. It's a
console-based application (menu driven, runs in the terminal) that keeps
track of the cars, lets the shop staff rent them out to customers, handles
returns, and keeps a history of everything. The idea is to remove the manual
work and human error by letting the code handle the business rules - like
not allowing a car to be rented if it's already out, and automatically
adding the luxury charge for premium cars.

## Scope

- This is built for a single rental shop, not multiple branches.
- It's a console app only, no GUI or website.
- Data is stored in memory (ArrayLists) while the program is running - once
  you close it, the data is gone. There's no database connected.
- Two kinds of cars are supported: normal cars and luxury cars (luxury ones
  have an extra daily charge on top of the base price).
- Things I did NOT do (out of scope): saving data permanently to a
  database, online payments, multiple people using it at the same time, or
  a proper UI.

## Who is this for?

- **The rental shop staff/operator** - this is the main person who'll
  actually use the app. They'll add cars, rent them out, mark returns, and
  check history.
- **The shop owner** - not a direct user, but they benefit because now
  there's a proper (even if basic) system tracking availability and rental
  income instead of a messy notebook.

## What can it actually do?

1. **Managing the fleet** - add new cars (normal or luxury) and see which
   ones are currently free to rent.
2. **Renting a car out** - pick an available car, enter the customer's
   details and how many days they want it, and the app calculates the total
   automatically (including the luxury surcharge if it applies).
3. **Returning a car** - once a customer brings the car back, mark that
   rental as returned so the car becomes available again.
4. **Rental history** - see a full list of every rental that's happened so
   far, whether it's still active or already returned.

These four things basically cover the three (or more) major modules the
project guidelines asked for - I'm treating them as **Car Management**,
**Rental/Return Handling**, and **Customer & History Tracking**.
# Car Rental Management System

A simple console-based Java project for managing a car rental shop - add
cars, check what's available, rent them out, process returns, and see the
rental history. Made this for my course project to practice OOP concepts
like inheritance, encapsulation and polymorphism.

## What it does

Manually tracking rentals on paper/excel is a pain and leads to mistakes
(double booking, wrong billing etc). This is basically a small Java app
that fixes that by handling the rules in code instead. Full details on the
problem and scope are in ['statement.md'].

## Features

- **Car Management** - add a normal or luxury car to the fleet, and check
  which cars are currently free.
- **Renting** - rent out an available car to a customer for some number of
  days, total price gets calculated automatically (luxury cars add an
  extra daily charge on top).
- **Returns** - return a car using its Rental ID and it becomes available
  again.
- **History** - see every rental made so far and whether it's Active or
  Returned.
- Used inheritance so `LuxuryCar` extends `Car` and just overrides the
  pricing/display logic instead of copy-pasting everything.

## Tech used

- Java (should work fine on JDK 8+, I used OpenJDK while building this)
- Just core Java - `ArrayList` and `Scanner`, no extra libraries
- No database, everything's in memory for now
- Git/GitHub for version control

## Files in this repo

```
car-rental-system/
├── src/
│   ├── Car.java              # base car class
│   ├── LuxuryCar.java        # extends Car, adds luxury charge
│   ├── Customer.java         # customer info
│   ├── Rental.java           # one rental record
│   ├── CarRental.java        # main logic + console menu
│   ├── Main.java             # starts the program
│   └── RentalSystemTest.java # basic tests, no external library needed
├── diagrams/                 # class/use case/sequence/workflow diagrams
├── statement.md              # problem statement
├── diagrams.md               # all diagrams with explanations
├── README.md
└── Project_Report.pdf        # final report for submission
```

## How to run it

1. Check you've got a JDK installed (not just JRE):
   ```
   javac -version
   ```
2. Clone this repo and go into the src folder:
   ```
   git clone <your-repo-url>
   cd car-rental-system/src
   ```
3. Compile everything:
   ```
   javac *.java
   ```
4. Run it:
   ```
   java Main
   ```
5. Follow the menu - add a car, rent it, return it, whatever.

## Testing

I wrote a basic test file (`RentalSystemTest.java`) that checks the main
logic works properly - stuff like a new car being available by default,
renting making it unavailable, and the total amount being calculated
correctly for both normal and luxury cars. Didn't use JUnit, just kept it
simple with plain println checks.

```
cd src
javac *.java
java RentalSystemTest
```

It'll print `[PASS]` or `[FAIL]` for each check and a total count at the
end.

## Menu (what you'll see when you run it)

```
================================
       CAR RENTAL SYSTEM
================================
1. Add Car
2. View Available Cars
3. Rent Car
4. Return Car
5. Rental History
0. Exit
================================
Enter your choice:
```

Made by- Sarthak Shukla
Reg. No.: 25BAI10023

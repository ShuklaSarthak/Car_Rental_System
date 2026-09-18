# Design Diagrams

## 1. System Architecture

This shows the basic layers of the app - the entry point (Main), the main
logic/menu (CarRental), the model classes (Car, LuxuryCar, Customer,
Rental), and where the data is actually stored (just ArrayLists in memory).

<img width="1150" height="846" alt="image" src="https://github.com/user-attachments/assets/fe187cd7-be4d-42b2-a07c-717e1a14e2a2" />

## 2. Use Case Diagram

Shows what the Operator (the only user of this system) can actually do.
Renting a car also "includes" registering the customer and calculating the
total, since those happen automatically as part of renting.

<img width="1410" height="1110" alt="image" src="https://github.com/user-attachments/assets/319a0738-c41c-49d5-bdf5-367e961a1fde" />

## 3. Class Diagram

All 6 classes with their fields and methods, plus how LuxuryCar extends Car,
and how CarRental/Rental connect to Car and Customer.

<img width="948" height="1419" alt="image" src="https://github.com/user-attachments/assets/1401ffd4-6b56-46fd-bcd9-e25135b118f4" />

## 4. Sequence Diagram - Renting a Car

This walks through what happens step by step when someone rents a car -
from the Operator picking "Rent Car" in the menu, to CarRental checking if
the car's free, creating the Customer and Rental objects, and finally
showing the total amount back.

<img width="1635" height="1110" alt="image" src="https://github.com/user-attachments/assets/5907160c-d179-465f-a35d-b46ec0112725" />

## 5. Workflow / Process Flow

This is basically the whole program's flow as a flowchart - the main menu
loop and what happens for each option, including the yes/no checks for
renting and returning.

<img width="2145" height="969" alt="image" src="https://github.com/user-attachments/assets/04b08f30-33dd-4696-8a7e-4c6d069c4581" />

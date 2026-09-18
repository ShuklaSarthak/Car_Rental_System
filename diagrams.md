# Design Diagrams

All the diagram images are inside the [`diagrams/`](diagrams/) folder. Just
make sure that folder stays next to this file so the images actually show
up when you open this on GitHub.

---

## 1. System Architecture

This shows the basic layers of the app - the entry point (Main), the main
logic/menu (CarRental), the model classes (Car, LuxuryCar, Customer,
Rental), and where the data is actually stored (just ArrayLists in memory).

![System Architecture](diagrams/architecture_diagram.png)

---

## 2. Use Case Diagram

Shows what the Operator (the only user of this system) can actually do.
Renting a car also "includes" registering the customer and calculating the
total, since those happen automatically as part of renting.

![Use Case Diagram](diagrams/usecase_diagram.png)

---

## 3. Class Diagram

All 6 classes with their fields and methods, plus how LuxuryCar extends Car,
and how CarRental/Rental connect to Car and Customer.

![Class Diagram](diagrams/class_diagram.png)

---

## 4. Sequence Diagram - Renting a Car

This walks through what happens step by step when someone rents a car -
from the Operator picking "Rent Car" in the menu, to CarRental checking if
the car's free, creating the Customer and Rental objects, and finally
showing the total amount back.

![Sequence Diagram](diagrams/sequence_diagram.png)

---

## 5. Workflow / Process Flow

This is basically the whole program's flow as a flowchart - the main menu
loop and what happens for each option, including the yes/no checks for
renting and returning.

![Workflow Diagram](diagrams/workflow_diagram.png)

---

> Didn't add an ER diagram since there's no actual database here - just
> ArrayLists in memory. That's mentioned in the scope in `statement.md` too.

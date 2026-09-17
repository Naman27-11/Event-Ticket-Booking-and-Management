# Event Ticket Booking & Management System

## Overview of the Project
The **Event Ticket Booking & Management System** is a console-based transaction application designed to automate event scheduling, real-time seat inventory tracking, ticket purchases, and cancellation loops. Developed using clean Object-Oriented Programming (OOP) paradigms in Python, the system utilizes dynamic, highly efficient in-memory data maps to guarantee lightning-fast transactions under 50 milliseconds. It includes robust, defensive error-handling mechanics to gracefully intercept malformed inputs, out-of-bounds capacity selections, and invalid reference keys without risking application uptime or crashing.

## Features
* **Admin Module:** Dynamic creation of events with unique IDs, name definitions, maximum seating limits, and fixed ticket prices.
* **User Booking Module:** Formatted live event roster views displaying active seating indices, real-time availability checking, and instant balance calculations.
* **Unique Transaction Key Generator:** Automatic creation of an 8-character alphanumeric uppercase booking ID token using secure UUIDv4 segmentation.
* **Cancellation Module:** Instant reservation verification checks and safe removal of booking tracking nodes that automatically restores seats to the parent event pool.
* **Defensive Exception Trapping:** Unified root-level `try-except` wrappers to cleanly capture string-to-number casting faults, duplicates, and logic overflows.

## Technologies/Tools Used
* **Programming Language:** Python 3.x
* **Core Standard Modules:** `uuid` (for reference generation)
* **Development Environment:** Any standard IDE or Text Editor (e.g., VS Code, PyCharm, IDLE)
* **Version Control:** Git & GitHub

## Steps to Install & Run the Project

### Prerequisites
Make sure you have **Python 3.x** installed on your system. You can verify your installation by running:
```bash
python --version
```

### Installation
1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com
   ```
2. Navigate into the project repository folder:
   ```bash
   cd event-ticket-booking
   ```

### Running the Application
Launch the text-driven interactive console engine using the standard Python interpreter:
```bash
python main.py
```

## Instructions for Testing
Run the application and input the following test inputs inside the interactive console menu interface to verify the integrity rules:

1. **Test Case 1 (Event Creation):** Go to option `1`. Create an event with ID `E101`, Capacity `50`, and Price `100`. Verify that it passes successfully. Try creating `E101` again to ensure the duplicate-key protection catches the error safely.
2. **Test Case 2 (Seat Booking):** Select option `2`. Input event ID `E101`, enter your name, and request `5` seats. Check that the console confirms the total cost (\$500.00) and displays an 8-character transactional tracking reference string.
3. **Test Case 3 (Capacity Check):** Select option `2` again. Attempt to book `60` seats for event `E101`. Verify that the engine gracefully blocks the attempt with a message stating that seats are insufficient.
4. **Test Case 4 (Cancellation & Sync):** Select option `3`. Input the exact 8-character booking ID generated during Test Case 2. Check that the system clears the booking data and returns the 5 seats safely to the `E101` availability balance.

## Screenshots
### Main Interactive Menu & Roster Overview
```text
==================================================
WELCOME TO THE CONSOLE EVENT TICKET ENGINE
==================================================

--- GLOBAL OPTIONS ---
1. Admin Module: Add New Event
2. User Module: View Events & Book Tickets
3. User Module: Cancel Booked Ticket
4. Exit System Application
Select an option (1-4): 2

[AVAILABLE EVENTS COLLECTION]
ID         | Event Name           | Available Seats | Price   
------------------------------------------------------------
E101       | Music Festival       | 100             | \$75.00  
E102       | Tech Conference      | 50              | \$120.00 
```

# TICKET-BOOKING-SYSTEM-USING-QUEUE-
Console-based Dynamic Booking Dispatch System built in C. It uses a custom-implemented queue data structure to manage patron service flow (FIFO), featuring ticket issuing, serving, and an array-shifting method for voiding specific tickets out of order while preserving queue integrity. Ideal for demonstrating core data structure operations.
Dynamic Booking Dispatch System
A robust, console-based ticket management system implemented in C, leveraging a Queue
data structure (First-In, First-Out) to ensure fair and sequential service for patrons.
This project demonstrates practical data structure implementation for managing linear service
flow, while also including a non-standard utility for ticket cancellation (voiding) which requires
shifting elements within the queue's underlying storage.

🚀 Features

●​ Issue New Ticket (Enqueue): Adds a new patron to the end of the line, assigning a
unique Receipt ID.
●​ Serve Next Patron (Dequeue): Removes the patron at the front of the line (the next in
the queue) and processes their request.
●​ Void Specific Ticket: Allows for the cancellation and removal of any ticket holder,
regardless of their position, maintaining the queue integrity by shifting subsequent entries.
●​ Display Manifest: Shows the current order and status of all patrons waiting in the queue.
●​ Capacity Management: Prevents overbooking by enforcing a hard limit (CAPACITY =
100).

🛠️ Technology Stack

●​ Language: C (C99 standard or newer)
●​ Data Structure: Array-based Queue

💻 Setup and Compilation
This is a single-file C program that can be compiled and run using any standard C compiler (like
GCC or Clang).

Prerequisites
You need a C compiler installed on your system (e.g., gcc on Linux/macOS or MinGW on
Windows).

Steps
1.​ Clone the Repository:​
git clone
[https://github.com/YourUsername/dynamic-booking-system.git](https
://github.com/YourUsername/dynamic-booking-system.git)​
cd dynamic-booking-system​
2.​ Compile the Source Code: Use your preferred compiler to build the executable.​
gcc booking_system.c -o booking_system​

3.​ Run the System: Execute the compiled program in your terminal.​
./booking_system​

Example Session
====== Dynamic Booking Dispatch System (C Queue) ======​
1. Issue New Ticket​
2. Serve Next Patron​
3. Void Specific Ticket​
4. Display Queue Manifest​
5. Terminate System​
Enter action: 1​
Enter Patron Name: Alice​
​
Ticket issued successfully! Receipt ID: 1​
​
Enter action: 1​
Enter Patron Name: Bob​
​
Ticket issued successfully! Receipt ID: 2​
​
Enter action: 4​
​
--- Current Booking Manifest ---​
Receipt ID: 1 | Name: Alice​
Receipt ID: 2 | Name: Bob​
​
Enter action: 2​
​
Patron Served: Alice (Receipt ID: 1)​
​
Enter action: 4​
​
--- Current Booking Manifest ---​
Receipt ID: 2 | Name: Bob​

💡 Queue Implementation Details

The core structure uses a fixed array and integer indices (head and tail) to track the start and
end of the queue.
●​ head: Index of the next patron to be served (Front).
●​ tail: Index of the last patron who booked a ticket (Rear).
When a ticket is voided, all subsequent patrons in the queue are shifted forward by one position
to maintain the sequential service order, which is an operation that makes this implementation

distinct from a pure circular queue structure.

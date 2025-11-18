# TICKET-BOOKING-SYSTEM-USING-QUEUE-
TICKET BOOKING SYSTEM (C LANGUAGE)

==================================================

🎯 PROJECT GOAL AND CONCEPT

This project implements a fundamental Ticket Booking and Patron Dispatch System using the C programming language. Its core function is to model a waiting line (or queue) where patrons are served in the order they arrive.

The system strictly adheres to the First-In, First-Out (FIFO) principle, meaning the patron who issues their ticket first is the next one to be served.

--------------------------------------------------

🏗️ DATA STRUCTURE: ARRAY-BASED QUEUE

The system's logic is built around an array-based implementation of a Queue.

* Structure: The BookingQueue structure manages an array of Patron records, utilizing 'head' and 'tail' indices to track the front and end of the line.
* Capacity: The queue has a defined capacity of 100 patrons (#define CAPACITY 100).
* Pointers:
    * 'head': Points to the patron who is next in line to be served (front of the queue).
    * 'tail': Points to the most recently added patron (rear of the queue).

--------------------------------------------------

⚙️ CORE FUNCTIONALITY

1. Issue New Ticket (issue_ticket): Adds a new patron to the end of the line (Enqueue).
2. Serve Next Patron (serve_patron): Removes and processes the patron at the front of the line (Dequeue).
3. Void Specific Ticket (void_ticket): Finds a specific patron by their Receipt ID and removes them from the line, shifting subsequent entries to maintain queue integrity. (Arbitrary Deletion)
4. Display Queue Manifest (show_queue): Displays the full list of all patrons currently waiting.
5. Terminate System (exit(0)): Closes the program.

--------------------------------------------------

🚀 GETTING STARTED

### Prerequisites
A C compiler (e.g., GCC, MinGW, Clang) is required.

### 1. Compilation
1.  Save the C source code as booking_system.c.
2.  Open your terminal or command prompt.
3.  Compile the file using your C compiler:

    gcc booking_system.c -o ticket_dispatch

### 2. Execution
Run the compiled executable:

    ./ticket_dispatch

--------------------------------------------------

💡 NOTE ON void_ticket

The 'void_ticket' function implements non-standard queue behavior by allowing the removal of an element from the middle of the line. This is achieved by searching the array for the matching Receipt ID and then shifting all subsequent elements forward one position to close the gap.

==================================================

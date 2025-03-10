# Sample Programs for Algorithm, Flowchart, and Pseudocode Development

## 1. Student Grade Calculator

**Program Description:**
Create a program that calculates the final grade for a student based on assignments (30%), midterm exam (30%), and final exam (40%). The program should determine if the student passed (≥60%) or failed.

**Key Features:**
- Input assignment scores, midterm score, and final exam score
- Calculate weighted average based on predefined percentages
- Determine pass/fail status
- Display final grade and status to user
- ALGORITHM
- Algorithm
Start
Input assignment scores (list of scores)
Input midterm score
Input final exam score
Calculate the average of assignment scores
Calculate the weighted average:
Weighted average = (Average of assignments * 0.3) + (Midterm score * 0.3) + (Final exam score * 0.4)
Determine if the weighted average is greater than or equal to 60%
If yes, set status to "Pass"
If no, set status to "Fail"
Display the final grade and status
End
- 
START
    DECLARE assignmentScores AS LIST
    DECLARE midtermScore AS FLOAT
    DECLARE finalExamScore AS FLOAT
    DECLARE averageAssignments AS FLOAT
    DECLARE weightedAverage AS FLOAT
    DECLARE status AS STRING

    PRINT "Enter assignment scores (separated by spaces):"
    INPUT assignmentScores

    PRINT "Enter midterm score:"
    INPUT midtermScore

    PRINT "Enter final exam score:"
    INPUT finalExamScore

    averageAssignments = AVERAGE(assignmentScores)

    weightedAverage = (averageAssignments * 0.3) + (midtermScore * 0.3) + (finalExamScore * 0.4)

    IF weightedAverage >= 60 THEN
        status = "Pass"
    ELSE
        status = "Fail"
    ENDIF

    PRINT "Final Grade: ", weightedAverage
    PRINT "Status: ", status
END
## 2. ATM Banking System

**Program Description:**
Develop a program that simulates an ATM with options to check balance, deposit money, withdraw money, and exit. The program should maintain a running balance and prevent withdrawals that would result in a negative balance.

**Key Features:**
- Authenticate user with PIN
- Display menu of available operations
- Handle balance inquiries
- Process deposits and update balance
- Validate withdrawal requests against available balance
- Provide transaction receipts
- Allow user to exit system
   ATM Algorithm:

# Initialize balance.

 Display menu.
 Get choice.
 If check balance: display balance.
  If deposit: add to balance (if valid).
  If withdraw: subtract from balance (if valid).
 If exit:
 end loop.
START 
DISPLAY"enter your pin:"
INPUT userpin
IF userpin is incorrect THEN 
DISPLAY "invalid pin try again."
EXIT
ENDIF
SET balance=1000
REPEAT
DISPLAY"ATM menu:"
DISPLAY"1.check balance"
DISPLAY"2.deposit money"
DISPLAY"3.withdraw money"
DISPLAY"4.exit"
DISPLAY"choose an option:"
INPUT choice

IF choice=1 THEN
DISPLAY "your balance is",balance
ELSE IF choice=2 THEN
DISPLAY"enter amount to deposit:"
INPUT depositAmount
  SET balance = balance + depositAmount
  DISPLAY "Deposit successful. New balance: ", balance
  ELSE IF choice = 3 THEN
  DISPLAY "Enter amount to withdraw:"
  INPUT withdrawAmount
  IF withdrawAmount > balance THEN
  DISPLAY "Insufficient funds!"
ELSE
 SET balance = balance - withdrawAmount
DISPLAY "Withdrawal successful. New balance: ", balance
ENDIF
ELSE IF choice = 4 THEN
DISPLAY "Thank you for using our ATM."
EXIT
ELSE
DISPLAY "Invalid choice. Please try again."
 ENDIF
    UNTIL choice = 4
END
 



## 3. Inventory Management System

**Program Description:**
Design a program that manages a store's inventory by allowing users to add new items, update quantities, remove items, and display the current inventory. Each item should have an ID, name, price, and quantity.

**Key Features:**
- Add new products to inventory with unique IDs
- Update existing product information
- Remove products from inventory
- Search for products by ID or name
- Display current inventory status
- Track low stock items
- Generate inventory reports
Algorithm for Inventory Management:

Create empty inventory list.
 If ID exists, error; else, add item (ID, name, price, quantity) to list.
   Find item by ID; update name, price, or quantity.
   Find item by ID; remove from list.
  Find items by ID or name; display results.
  Show all items in inventory.
  Show items with quantity below threshold.
  Write inventory data to file.

Start
DECLARE inventory as a list

FUNCTION addProduct(id, name, price, quantity)
    CREATE product as dictionary with keys (id, name, price, quantity)
    ADD product to inventory
    DISPLAY "Product added successfully."

FUNCTION updateProduct(id, new_price, new_quantity)
    FOR each product in inventory
        IF product.id == id THEN
            SET product.price = new_price
            SET product.quantity = new_quantity
            DISPLAY "Product updated successfully."
            RETURN
    DISPLAY "Product not found."

FUNCTION removeProduct(id)
    FOR each product in inventory
        IF product.id == id THEN
            REMOVE product from inventory
            DISPLAY "Product removed successfully."
            RETURN
    DISPLAY "Product not found."

FUNCTION searchProduct(id_or_name)
    FOR each product in inventory
        IF product.id == id_or_name OR product.name == id_or_name THEN
            DISPLAY product details
            RETURN
    DISPLAY "Product not found."

FUNCTION displayInventory()
    IF inventory is empty THEN
        DISPLAY "Inventory is empty."
    ELSE
        FOR each product in inventory
            DISPLAY product details
            FUNCTION trackLowStock(threshold)
    FOR each product in inventory
        IF product.quantity < threshold THEN
            DISPLAY "Low stock:", product details

FUNCTION generateReport()
    DISPLAY "Inventory Report:"
    DISPLAY "Total Products:", COUNT(inventory)
    DISPLAY all product details

LOOP
    DISPLAY "1. Add Product"
    DISPLAY "2. Update Product"
    DISPLAY "3. Remove Product"
    DISPLAY "4. Search Product"
    DISPLAY "5. Display Inventory"
    DISPLAY "6. Track Low Stock"
    DISPLAY "7. Generate Report"
    DISPLAY "8. Exit"
    DISPLAY "Enter your choice: "
    INPUT choice

  SWITCH(choice)
        CASE 1: CALL addProduct()
        CASE 2: CALL updateProduct()
        CASE 3: CALL removeProduct()
        CASE 4: CALL searchProduct()
        CASE 5: CALL displayInventory()
        CASE 6: CALL trackLowStock()
        CASE 7: CALL generateReport()
        CASE 8: EXIT program
        DEFAULT: DISPLAY "Invalid choice, try again."

END


  
## 4. Prime Number Checker

**Program Description:**
Create a program that determines whether a given number is prime or not. A prime number is only divisible by 1 and itself with no other factors.

**Key Features:**
- Accept numerical input from user
- Verify if input is valid (positive integer)
- Use efficient algorithm to check for primality
- Display result with explanation
- Option to check additional numbers
- Algorithm to Determine if a Number is Prime:

 Get a number 'n' as input.
If 'n' is less than or equal to 1, return False (not prime).
Iterate from 'i' = 2 up to the square root of 'n'.
For each 'i', check if 'n' is divisible by 'i' (i.e., if 'n' % 'i' == 0).
 If 'n' is divisible by any 'i', return False (not prime).
 If the loop completes without finding any divisors, return True ('n' is prime).


 START

FUNCTION isPrime(number)
    IF number <= 1 THEN
        RETURN false
    IF number is 2 THEN
        RETURN true
    FOR i FROM 2 TO square root of number DO
        IF number MOD i == 0 THEN
            RETURN false
    RETURN true

LOOP
    DISPLAY "Enter a positive integer: "
    INPUT number

  IF number is not a positive integer THEN
        DISPLAY "Invalid input. Please enter a positive integer."
        CONTINUE

   IF isPrime(number) THEN
        DISPLAY number, "is a prime number."
    ELSE
        DISPLAY number, "is not a prime number."

  DISPLAY "Do you want to check another number? (yes/no)"
    INPUT choice
    IF choice is "no" THEN
        EXIT LOOP

END


## 5. Temperature Conversion Tool

**Program Description:**
Develop a program that converts temperatures between Celsius, Fahrenheit, and Kelvin. The user should be able to select the input and output temperature scales.

**Key Features:**
- Accept temperature value input
- Allow selection of source unit (C, F, or K)
- Allow selection of target unit (C, F, or K)
- Perform accurate conversion using correct formulas
- Display converted result with appropriate unit
- Option for multiple conversions

Algorithm for Temperature Conversion:
    Get the temperature value (number).
     Get the input temperature scale (Celsius, Fahrenheit, or Kelvin).
     Get the output temperature scale (Celsius, Fahrenheit, or Kelvin).
    *Celsius to Fahrenheit:*
        * Fahrenheit = (Celsius * 9/5) + 32
      *Celsius to Kelvin:*
        * Kelvin = Celsius + 273.15
      *Fahrenheit to Celsius:*
        * Celsius = (Fahrenheit - 32) * 5/9
      *Fahrenheit to Kelvin:*
        * Kelvin = (Fahrenheit - 32) * 5/9 + 273.15
      *Kelvin to Celsius:*
        * Celsius = Kelvin - 273.15
      *Kelvin to Fahrenheit:*
       Fahrenheit = (Kelvin - 273.15) * 9/5 + 32
    Use conditional statements (if/else or switch/case) to determine the correct conversion based on the input and output scales.
      If input and output scales are the same, the output is the same as the input.
      Display the converted temperature value along with the output temperature scale.


    
  START

FUNCTION convertTemperature(value, sourceUnit, targetUnit)
    IF sourceUnit == "C" AND targetUnit == "F" THEN
        RETURN (value * 9/5) + 32
    ELSE IF sourceUnit == "C" AND targetUnit == "K" THEN
        RETURN value + 273.15
    ELSE IF sourceUnit == "F" AND targetUnit == "C" THEN
        RETURN (value - 32) * 5/9
    ELSE IF sourceUnit == "F" AND targetUnit == "K" THEN
        RETURN (value - 32) * 5/9 + 273.15
    ELSE IF sourceUnit == "K" AND targetUnit == "C" THEN
        RETURN value - 273.15
    ELSE IF sourceUnit == "K" AND targetUnit == "F" THEN
        RETURN (value - 273.15) * 9/5 + 32
    ELSE
        RETURN value  // No conversion needed if units are the same

LOOP
    DISPLAY "Enter temperature value: "
    INPUT value

    DISPLAY "Enter source unit (C, F, K): "
    INPUT sourceUnit

    DISPLAY "Enter target unit (C, F, K): "
    INPUT targetUnit

    convertedValue = convertTemperature(value, sourceUnit, targetUnit)
    DISPLAY "Converted Temperature: ", convertedValue, targetUnit

    DISPLAY "Do you want to convert another temperature? (yes/no)"
    INPUT choice
    IF choice == "no" THEN
        EXIT LOOP

END
## 6. Library Book Management System

**Program Description:**
Design a program that manages a library's book collection, allowing librarians to add books, remove books, check out books to members, and return books. Track availability status for each book.

**Key Features:**
- Maintain database of books (title, author, ISBN, status)
- Maintain database of library members
- Process for adding new books to collection
- Process for removing obsolete books
- Book checkout procedure with due dates
- Book return procedure with potential late fees
- Search functionality by title, author, or ISBN
- Report generation for overdue books

- # Library Book Management Algorithm:
 Append book to library's book list.
 Find book by ISBN, remove if found.
 Find book by ISBN, mark unavailable if found and available.
 Find book by ISBN, mark available if found and checked out.
 List titles of available books.

 
 DEFINE Book class:
    Attributes: title, author, ISBN, status (Available/Checked Out)

DEFINE Member class:
    Attributes: name, member_id, borrowed_books (list)

DEFINE Library class:
    Attributes: books (list), members (list)
    
  FUNCTION add_book(title, author, ISBN):
        Create new Book object with status "Available"
        Add to books list

   FUNCTION remove_book(ISBN):
        Find book by ISBN
        IF found THEN remove from books list

  FUNCTION register_member(name, member_id):
        Create new Member object
        Add to members list

   FUNCTION checkout_book(member_id, ISBN):
        Find book and member
        IF book is available THEN
            Change status to "Checked Out"
            Add book to member's borrowed_books list
        ELSE
            DISPLAY "Book not available"

  FUNCTION return_book(member_id, ISBN):
        Find member and book
        IF book is in member's borrowed_books THEN
            Change status to "Available"
            Remove book from member's borrowed_books list
        ELSE
            DISPLAY "Book not checked out"

   FUNCTION search_book(query):
        Search books by title, author, or ISBN
        DISPLAY matching results

   FUNCTION generate_overdue_report():
        CHECK due dates and list overdue books

LOOP
    DISPLAY menu: Add Book, Remove Book, Register Member, Checkout, Return, Search, Overdue Report, Exit
    INPUT choice
    EXECUTE corresponding function based on choice
    IF choice == "Exit" THEN EXIT LOOP

END


 

## 7. Fibonacci Sequence Generator

**Program Description:*
Create a program that generates the Fibonacci sequence up to a specified number of terms. The Fibonacci sequence starts with 0 and 1, and each subsequent number is the sum of the two preceding numbers.

**Key Features:**
- Accept number of terms to generate
- Validate input is reasonable (positive integer within limits)
- Generate sequence using efficient algorithm
- Display sequence with appropriate formatting
- Option to save sequence to file
- # Algorithm for Fibonacci Sequence Generation

# Input: Number of terms (n)

 Initialize a list or array called fib_sequence with the first two Fibonacci numbers: [0, 1]

 If n is less than or equal to 2:
    Return the first n elements of fib_sequence.

 While the length of fib_sequence is less than n:
Calculate the next Fibonacci number by adding the last two numbers in fib_sequence.
Append the calculated number to fib_sequence.
Return fib_sequence.
start
FUNCTION generate_fibonacci(n):
    IF n <= 0 THEN
        DISPLAY "Enter a positive integer"
        RETURN
    ELSE IF n == 1 THEN
        RETURN [0]
    ELSE IF n == 2 THEN
        RETURN [0, 1]

   INITIALIZE sequence = [0, 1]
    FOR i FROM 2 TO n-1:
        NEXT_TERM = sequence[i-1] + sequence[i-2]
        APPEND NEXT_TERM to sequence

  RETURN sequence

FUNCTION save_to_file(sequence):
    OPEN "fibonacci.txt" in write mode
    WRITE sequence to file
    CLOSE file

LOOP
    DISPLAY "Enter the number of Fibonacci terms to generate:"
    INPUT n
    VALIDATE n is a positive integer
    CALL generate_fibonacci(n) → result
    DISPLAY result

   DISPLAY "Do you want to save the sequence to a file? (yes/no)"
    INPUT choice
    IF choice == "yes" THEN
        CALL save_to_file(result)
        DISPLAY "Sequence saved successfully"

   DISPLAY "Do you want to generate another sequence? (yes/no)"
    INPUT repeat
    IF repeat == "no" THEN EXIT LOOP

END


## 8. Calendar Event Scheduler

**Program Description:**
Develop a program that allows users to schedule events on a calendar. Users should be able to add events with dates, times, and descriptions, view all events, and delete events.

**Key Features:**
- Add events with title, date, time, and description
- Validate date and time inputs
- Store events in organized data structure
- Display events for a specific day, week, or month
- Search events by title or description
- Delete or modify existing events
- Set reminders for upcoming events
- Check for schedule conflicts
- # Calendar Algorithm:

Create event, add to calendar.
Display all events.
 Find and remove matching event.
Loop, get user input, call functions.

START
DEFINE event_list as an empty list

FUNCTION add_event(title, date, time, description):
    VALIDATE date and time
    CHECK for conflicts with existing events
    IF no conflict THEN
        APPEND (title, date, time, description) to event_list
        DISPLAY "Event added successfully"
    ELSE
        DISPLAY "Schedule conflict detected"

FUNCTION display_events(filter_type, filter_value):
    IF filter_type is "day/week/month":
        FILTER event_list based on filter_value
    DISPLAY filtered events

FUNCTION search_event(keyword):
    SEARCH event_list for keyword in title or description
    DISPLAY matching events

FUNCTION delete_event(title, date, time):
    FIND event in event_list
    IF event exists THEN
        REMOVE event from event_list
        DISPLAY "Event deleted successfully"
    ELSE
        DISPLAY "Event not found"

FUNCTION modify_event(title, date, time, new_details):
    FIND event in event_list
    IF event exists THEN
        UPDATE event details
        DISPLAY "Event modified successfully"
    ELSE
        DISPLAY "Event not found"

FUNCTION set_reminder(title, date, time, reminder_time):
    VALIDATE reminder_time
    SCHEDULE reminder notification
    DISPLAY "Reminder set"

LOOP
    DISPLAY menu (Add, View, Search, Delete, Modify, Set Reminder, Exit)
    INPUT choice
    PERFORM corresponding function based on choice
    IF choice == "Exit" THEN EXIT LOOP

END

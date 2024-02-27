# Library-Management-System-Project
Library Management System Project implementing Object Oriented Programming using C++ 
# Library Management System Documentation

This project is a simple console-based Library Management System implemented in C++. It provides a simple interface for managing books and transactions in a library.

## Classes

### 1. Book

This is the base class for all types of books. It contains the following data members:

- `id`: An integer representing the unique identifier of the book.
- `title`: A string representing the title of the book.
- `author`: A string representing the author of the book.
- `publicationYear`: An integer representing the year the book was published.
- `quantity`: An integer representing the quantity of the book available in the library.

The class also contains the following member functions:

- `get_booktype()`: A virtual function that returns the type of the book.
- `inputDetails()`: A function to input the details of the book.
- `displayDetails()`: A function to display the details of the book.
- Getter functions for `author`, `title`, `publicationYear`, and `id`.

### 2. ReferenceBook

This class is derived from the `Book` class and represents a reference book. It contains an additional data member `category` which represents the category of the reference book. It also overrides the `get_booktype()`, `inputDetails()`, and `displayDetails()` functions from the `Book` class.

### 3. FictionBook

This class is derived from the `Book` class and represents a fiction book. It contains an additional data member `genre` which represents the genre of the fiction book. It also overrides the `get_booktype()`, `inputDetails()`, and `displayDetails()` functions from the `Book` class.

### 4. Transaction

This class represents a transaction in the library. It contains the following data members:

- `id`: An integer representing the unique identifier of the transaction.
- `user_id`: An integer representing the unique identifier of the user.
- `date_issued`: A string representing the date the book was issued.
- `due_date`: A string representing the due date for returning the book.
- `date_returned`: A string representing the date the book was returned.

The class also contains the following member functions:

- A constructor that initializes the data members.
- `trans()`: A function to perform a transaction.
- `returnitem()`: A function to return an item.
- Getter functions for `id`, `issuedate`, `returndate`, `duedate`, and `userid`.

### 5. Library

This class represents the library. It contains the following data members:

- `books[]`: An array of pointers to `Book` objects representing the books in the library.
- `Trans[]`: An array of `Transaction` objects representing the transactions in the library.
- `Transaction_counter`: A static integer representing the number of transactions.
- `numBooks`: A static integer representing the number of books.

The class also contains the following member functions:

- `addBook()`: A function to add a book to the library.
- `displayAllBooks()`: A function to display all the books in the library.
- `printtransactions()`: A function to print all the transactions.
- `checkbook()`: A function to check a book by its id.
- `issuebook()`: A function to issue a book.
- `return_item()`: A function to return a book.
- `saveToFile()`: A function to save the library data to a file.
- `loadFromFile()`: A function to load the library data from a file.
- `saveTransaction()`: A function to save the transaction data to a file.
- `loadTransaction()`: A function to load the transaction data from a file.

## Main Function

The `main()` function provides a menu-driven interface for the user to interact with the library. The user can add books, display all books, search for a book by id, issue a book, return a book, print transaction history, save library data to a file, load library data from a file, save transaction data to a file, and load transaction data from a file.

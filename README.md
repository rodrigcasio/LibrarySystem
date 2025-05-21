# LibrarySystem: C++ Console Project

A lightweight C++ console-based system for managing a library, designed to demonstrate the use of **variable scopes** and **storage classes** through book management, reservations, and membership tracking.

## Features

- **Book Management**: Add books (up to 100) with budget tracking, list available books with formatted output.
 
- **Waitlist System**: Reserve books to prevent borrowing, borrow unreserved books, with error handling for reserved or non-existent books.
 
- **Membership System**: Register members (up to 100), list members, and track total membership count.

- **Counters**: Track borrowed books and members using static variables, accessible via static methods.

## C++ Principles: 
  - **Variable Scopes**: Uses `auto` for iterators, range-based `for` loops, and `*it` dereferencing in `borrowBook()` to demonstrate iterator mechanics and scope control.

  - **Storage Classes**: Employs `static` for global counters (`totalBorrowedBooks`, `totalMembersCount`), `mutable` for `reservedBooks` in `const` methods, and `const` for read-only functions.

  - **Iterators**: Combines manual `for` loop with `*it` dereferencing and `std::find` in `borrowBook()` to showcase iterator efficiency and flexibility.

  - **Vectors**: Uses `std::vector<std::string>` for `bookList`, `reservedBooks`, and `libraryMembers`, with dynamic management.

## Purpose

Developed as part of my C++ learning journey to demonstrate the use of **variable scopes** and **storage classes**. This project showcases my ability to design and implement functional systems using vectors, iterators, and storage modifiers, building on projects like `SchoolSystem` and `FLightBookingEx`.

## How to Run
```
g++ src/mainLibrarySystem.cpp src/fns_LibrarySystem.cpp -I include -o library
./library
```

## Sample Output
```
Current library budget is: $5000

-------- Adding books to library ------------
To Sleep in a Sea of Stars has been added to the library successfully.
Six Easy Pieces has been added to the library successfully.
Relativity for Beginners has been added to the library successfully.
Alex's Adventures in Numberland has been added to the library successfully.

-------- Displaying available books in myLibrary ------------
	=== Books ===
- To Sleep in a Sea of Stars
- Six Easy Pieces
- Relativity for Beginners
- Alex's Adventures in Numberland

-------- Reserving books ------------
Book reserved: Six Easy Pieces
Reserved book count: 1
Six Easy Pieces cannot be reserved. Book already reserved.
Imaginary Book cannot be reserved. Book is not available in the library.

-------- Borrowing books ------------
Relativity for Beginners has been borrowed successfully. Enjoy.
Six Easy Pieces is reserved and cannot be borrowed.
Imaginary book is not available in the library.
...
```

## Author 
Rodrigo Casio ([View my Github profile](https://github.com/rodrigcasio))

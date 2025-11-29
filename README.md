# LibrarySystem (C++)

This is a small C++ console project I made to practice using variable scopes, storage classes, and basic C++ programming. The program simulates a simple library system where you can add books, manage reservations, and keep track of members.

## Features

- **Book Management**: Add books (up to 100) with budget tracking, list available books with formatted output.
 
- **Waitlist System**: Reserve books to prevent borrowing, borrow unreserved books, with error handling for reserved or non-existent books.
 
- **Membership System**: Register members (up to 100), list members, and track total membership count.

- **Counters**: Track borrowed books and members using static variables, accessible via static methods.

## Purpose

I made this project to get better at using things like `static` variables, `const` methods, and vectors in C++. It helped me understand how to organize code for a small system and how to use different storage classes and variable scopes.

## How to Run

This project uses **CMake** build system generator for easy, cross-platform compilation. Follow these steps from the root directory of the project `LibrarySystem/`

1. **Ensure CMake is installed:**
- Make sure you have CMake (version 3.1- or higher please) and a C++ compiler (g++ or clang++) installed on your system.

2. **Generate the build system (configure):**
- Create a separated directory for the build files  and run CMake inside it. Keeping source files clean

```bash
mkdir build
cd build
cmake ..
```

3. **Build:**
- Use generated build system (`make` on Unix-like systems) to compile the executable.

```bash 
make
```

4. **Run the program:**
- The executable (LibrarySystem) will be placed inside the `build` directory.

```bash 
./LibrarySystem
```

**IMPORTANT: Note for windows users:**

- Windows developers have two ways to build the project using CMake.
  - **Command line (MSYS2/Cygwin):** If you use an environment like **MSYS2** or **WLS** (Windows Subsystem for Linux), you can follow the **Standard Build** steps above exactly.
  - **Visual Studio:** CMake can generate a Visual Studio solution. Run CMake from your `developer command prompt`, specify the generator:

```bash 
cmake .. -G "Visual Studio 17 2022"
```

Then, open the generated `.sln` file and build within Visual Studio IDE.

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

Rodrigo Casio  
[My GitHub Profile](https://github.com/rodrigcasio)

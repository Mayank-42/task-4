Name: Mayank raj
Company:CODTECH IT SOLUTION
ID:CT08DS388
Domain: Java programing
Duration:December 2024to January 2025
Mentor:Muzammil Ahmed  

Overview of the Library Management System Java Code:
The provided Java code is for a Library Management System designed to manage resources (books, magazines, DVDs) in a library. The system supports functionality for adding new items, checking out and returning items, calculating overdue fines, and searching for items. Additionally, the system supports two types of users: Librarians and Patrons, each with different permissions. The application also handles basic user authentication and item management, storing items in an in-memory list.

Key Components of the Code:
LibraryItem Class:

Represents a generic item in the library.
Attributes:
title: Title of the item.
author: Author of the item.
category: Category of the item (e.g., Book, Magazine, DVD).
isCheckedOut: Boolean indicating whether the item is currently checked out.
dueDate: Due date for returning the item.
Methods:
checkout(): Marks the item as checked out and sets the due date.
returnItem(): Marks the item as returned and clears the due date.
calculateFine(): Calculates any overdue fines based on the due date.
getDetails(): Returns a formatted string with details about the item.
Subclasses of LibraryItem:

Book, Magazine, and DVD are specialized types of LibraryItem, each representing a different kind of library resource.
User Class:

Represents a generic user in the system, containing:
username: Username for the user.
password: Password for the user.
Method:
authenticate(): Authenticates the user based on the provided password.
Librarian and Patron Classes:

Both classes inherit from User, with additional specific permissions:
Librarian: Can add new items to the library (addItem()).
Patron: Can check out items (checkoutItem()), return items (returnItem()), and calculate fines (calculateFine()).
Library Class:

Manages the collection of LibraryItem objects and users (Librarian and Patron).
Attributes:
inventory: A list that holds all library items.
users: A list that holds all users.
Methods:
addItem(): Adds a new item to the library.
listItems(): Lists all items in the library and their current status (checked out or available).
searchItem(): Searches for items in the library by title, author, or category.
addUser(): Adds a new user to the system.
authenticateUser(): Authenticates a user based on their username and password.
Main Program (LibrarySystem Class):

Handles the main application logic and user interaction via the console:
Users are prompted to log in with their username and password.
Based on the type of user (Librarian or Patron), the program allows the user to perform various actions (e.g., add new books, search for items, checkout and return items, calculate fines).
If the user is a Librarian, they can:
Add new books to the library inventory.
List all items in the library.
If the user is a Patron, they can:
Search for library items by title or author.
Checkout or return items.
Calculate overdue fines for checked-out items.
User Interaction:
The program first asks the user to input their username and password.
If the credentials are correct, the user is assigned a role (either Librarian or Patron) and can perform role-specific actions:
Librarians have the ability to add new items to the library and list existing items.
Patrons can search for, check out, and return items, and check any fines for overdue items.




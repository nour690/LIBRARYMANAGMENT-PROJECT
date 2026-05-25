# 📚 Library Management System

A desktop Library Management System built using Python, PyQt5, and SQLite.

The application provides an intuitive graphical interface for librarians and customers to manage books, borrowing operations, return requests, fines, and user accounts efficiently.

It follows a layered architecture where:

---

the GUI handles user interaction,
DatabaseManager handles business logic and database operations,
SQLite stores persistent system data.

---

## ✨ Features

### 👨‍💼 Librarian / Admin
- Add new books
- Update book information
- Delete books
- Manage members/users
- Verify or unverify users
- Approve return requests
- View dashboard statistics
- Handle customer book requests
- Monitor borrowed books and overdue returns
- 
### 🙋 Customer / Member
- Register and log in
- Browse available books
- Add books to cart
- Borrow books
- Request book returns
- Send book requests
- Receive librarian replies/messages
- View borrowing history

## 🔐 Roles & Permissions
Role	Capabilities
Admin/Librarian	Full access to books, users, requests, returns, dashboard
Customer	Browse and borrow books, request returns, manage own account
🛒 Borrowing Workflow

| Role                | Capabilities                                                 |
| ------------------- | ------------------------------------------------------------ |
| **Admin/Librarian** | Full access to books, users, requests, returns, dashboard    |
| **User**            | Browse and borrow books, request returns, manage own account |

---

The borrowing system follows a multi-step workflow:

User browses books
Books are added to the cart
System validates borrowing rules:
verified account required
no overdue books
no unpaid fines
maximum borrowing limit
Checkout converts cart items into official borrowing records
Available book copies are updated automatically
🔁 Return Request System

Instead of directly returning books, customers submit a return request.

The librarian:

reviews the request,
checks book condition,
calculates possible fines,
approves the return.

This simulates a more realistic library workflow.

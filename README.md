# 📚 Library Management System

A desktop Library Management System built using Python, PyQt5, and SQLite.

The application provides an intuitive graphical interface for librarians and customers to manage books, borrowing operations, return requests, fines, and user accounts efficiently.

It follows a layered architecture where:

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

| Role                | Capabilities                                                 |
| ------------------- | ------------------------------------------------------------ |
| **Admin/Librarian** | Full access to books, users, requests, returns, dashboard    |
| **User**            | Browse and borrow books, request returns, manage own account |

---

## 🛒 Borrowing Workflow

The borrowing system follows a multi-step workflow:

1. User browses books
2. Books are added to the cart
3. System validates borrowing rules:
   - verified account required
   - no overdue books
   - no unpaid fines
   - maximum borrowing limit
4. Checkout converts cart items into official borrowing records
5. Available book copies are updated automatically

---

## 🔁 Return Request System

Instead of directly returning books, customers submit a return request.

The librarian:
- reviews the request,
- checks book condition,
- calculates possible fines,
- approves the return.

This simulates a more realistic library workflow.

---

## 💰 Fine Calculation

Fines are calculated based on:
- overdue days,
- book condition.

### Book Conditions

| Condition | Fine |
|---|---|
| Excellent | 0 |
| Good | 2 |
| Bad | 5 |
| Damaged | 10 |

Additional overdue fines:

```python
delay_fine = delay_days * 5
```

---

# 🧩 Architecture

## GUI Layer

Built with **PyQt5**.

Handles:
- pages,
- forms,
- tables,
- navigation,
- user interaction.

---

## Business Logic Layer

The `DatabaseManager` class centralizes:
- authentication,
- borrowing logic,
- fine calculations,
- validation,
- SQL operations.

This keeps the project modular and easier to maintain.

---

## Database Layer

SQLite database stores all persistent data.

Main tables:
- `users`
- `books`
- `cart`
- `borrowed_books`
- `return_requests`
- `messages`
- `book_requests`

---

## 🧱 Tech Stack

| Component | Technology |
|---|---|
| Language | Python |
| GUI | PyQt5 |
| Database | SQLite |
| IDE | VS Code |
| UI Design | Qt Designer |

---

# 🛠️ Setup & Installation

## 1️⃣ Prerequisites

- Python 3.10+
- PyQt5
- SQLite3
- VS Code (recommended)

Install PyQt5:

```bash
pip install PyQt5
```

---

## 2️⃣ Running the Application

Clone the repository:

```bash
git clone YOUR_REPO_LINK
```

Open the project folder:

```bash
cd project-name
```

Run the application:

```bash
python main.py
```

---

# 👨‍💻 Author

Mohammad Nour ALTURKMANI

Software Engineering Student @ FSMVU

📍 Passionate about software engineering, GUI development, and database systems.

🗓️ Final project developed during the Spring 2026 semester.

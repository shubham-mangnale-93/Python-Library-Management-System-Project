# 📚 Library Management System

A Python **OOPs-based Library Management System** that manages books, members, and all core library operations — from issuing to returning books. 🐍✨

---

## 🧾 Project Overview

This system manages:

- 📖 Books
- 🧑‍🤝‍🧑 Library members
- 🔢 Book quantities
- 📤 Book issuing
- 📥 Book returning
- ➕ Adding books
- 👤 Adding members
- ➖ Removing book copies
- 🖥️ Displaying books and members

---

## 🏗️ Classes Used

### 1️⃣ `Book`

Represents a book in the library.

**Attributes:**
- `book_name`
- `author`
- `quantity`

**Methods:**
| Method | Description |
|--------|-------------|
| `add_copies(count)` | ➕ Adds copies to the available quantity |
| `remove_copy()` | ➖ Removes one copy if available |
| `display_book()` | 🖨️ Displays book details |

```python
book1 = Book("Python Programming", "Mark Lutz", 5)
```

---

### 2️⃣ `Member`

Represents a library member.

**Attributes:**
- `member_id`
- `member_name`
- `issued_books`

**Methods:**
| Method | Description |
|--------|-------------|
| `issue_book(book)` | 📕 Adds a book to the member's issued list |
| `return_book(book)` | 🔄 Removes a returned book from the member's list |
| `display_member()` | 🖨️ Displays member details and issued books |

```python
member1 = Member(101, "Vaibhav")
```

---

### 3️⃣ `Library`

Manages books and members using **composition**.

**Attributes:**
- `library_name`
- `books` 📚
- `members` 👥

```python
self.books = []
self.members = []
```

**Methods:**
| Method | Description |
|--------|-------------|
| `add_book(book)` | ➕ Adds a new book or extra copies |
| `add_member(member)` | 👤 Registers a member |
| `remove_book(book_name, count)` | 🗑️ Removes specified copies |
| `display_books()` | 📖 Displays all available books |
| `display_members()` | 🧑‍🤝‍🧑 Displays all registered members |
| `issue_book(book_name, member_id)` | 📤 Issues a book after checking availability |
| `return_book(book_name, member_id)` | 📥 Returns an issued book |

---

## 🧠 OOPs Concepts Used

### 🔹 Class and Object
Three classes power the system — `Book`, `Member`, and `Library`.

```python
book1 = Book("Python Programming", "Mark Lutz", 5)
member1 = Member(101, "Vaibhav")
library = Library("ABC Central Library")
```

### 🔹 Constructor
Every class uses `__init__()` to initialize its data.

```python
def __init__(self, book_name, author, quantity):
    self.book_name = book_name
    self.author = author
    self.quantity = quantity
```

### 🔹 Composition 🧩
The `Library` **HAS-A** collection of `Book`s and `Member`s.

```python
self.books = []
self.members = []

library.add_book(book1)
library.add_member(member1)
```

### 🔹 Encapsulation 🔒
Data and logic are bundled inside their respective classes:

```python
book.add_copies(2)
book.remove_copy()
```

---

## 🔄 Project Flow

```
📖 Create Book Objects
        ↓
🧑 Create Member Objects
        ↓
🏛️ Create Library Object
        ↓
➕ Add Books
        ↓
👤 Add Members
        ↓
🖥️ Display Books and Members
        ↓
📤 Issue Books
        ↓
🖥️ Display Updated Data
        ↓
📥 Return Books
        ↓
🖥️ Display Updated Data
        ↓
🗑️ Remove Book Copies
```

---

## ⚙️ Sample Operations

### ➕ Add Books
```python
library.add_book(book1)
library.add_book(book2)
library.add_book(book3)
```

### 👤 Add Members
```python
library.add_member(member1)
library.add_member(member2)
library.add_member(member3)
```

### 📤 Issue Books
```python
library.issue_book("Python Programming", 101)
library.issue_book("Machine Learning", 102)
library.issue_book("Data Science", 103)
```

**When a book is issued:**
1. 🔍 The book is searched in the library
2. 🔍 The member is searched
3. ✅ Book availability is checked
4. ➖ One copy is removed from the library
5. 📥 The book is added to the member's `issued_books` list

### 📥 Return Book
```python
library.return_book("Python Programming", 101)
```

**When a book is returned:**
1. 🔍 The member is searched
2. ✅ The issued book is checked
3. ➖ The book is removed from the member's issued list
4. ➕ One copy is added back to the library

### 🗑️ Remove Book Copies
```python
library.remove_book("Machine Learning", 1)
```
> ⚠️ Checks whether enough copies are available before removing them.

---

## 🗂️ Project Structure

```
Library_Management/
│
├── 📄 book.py
├── 📄 member.py
├── 📄 library.py
└── 📄 main.py
```

---

## 🛠️ Technologies Used

- 🐍 Python
- 🧱 Object-Oriented Programming
- 🏛️ Classes and Objects
- 🧩 Constructors
- 🔗 Composition
- 📋 Lists
- ⚙️ Methods
- 🔀 Conditional Statements
- 🔁 Loops

---

## ▶️ How to Run

Open the project in **VS Code** and run:

```bash
python main.py
```

---

## ⭐ Project Highlights

- ✅ Manages books and their quantities
- ✅ Registers library members
- ✅ Issues books to members
- ✅ Handles book returns
- 🚫 Prevents issuing unavailable books
- 🚫 Prevents removing more copies than available
- 🖥️ Displays current library and member information

---

<div align="center">

Made with ❤️ using Python & OOPs

</div>

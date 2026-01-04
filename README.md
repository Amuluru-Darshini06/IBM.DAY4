# IBM.DAY5


📚 Library Management System (Node.js + MongoDB)

A simple **Library Management System REST API** built using **Node.js**, **Express**, and **MongoDB (Mongoose)**.
This project allows managing books with full **CRUD operations**, filtering, and validations.


 🚀 Features

* ➕ Add multiple books at once
* 📖 View all books
* 🔍 Filter books by **category**
* 📅 Get books published **after 2015**
* ✏️ Update available copies (increase/decrease)
* 🔄 Change book category
* ❌ Delete books only when copies = 0
* ✅ MongoDB schema validation


 🛠️ Tech Stack

* **Node.js**
* **Express.js**
* **MongoDB**
* **Mongoose**



 📁 Project Structure


library-management-system/
│
├── app.js          # Express server & routes
├── bookmodel.js    # Book schema (Mongoose)
├── db.js           # MongoDB connection
├── package.json
└── README.md


⚙️ Installation & Setup
1️⃣ Clone the repository


git clone https://github.com/your-username/library-management-system.git
cd library-management-system

 2️⃣ Install dependencies

```bash
npm install


 3️⃣ Start MongoDB

Make sure MongoDB is running locally:

mongod


4️⃣ Run the server


node app.js

Server will start at:

http://localhost:3000


📌 API Endpoints

 ➕ Add Books (Insert 7 books)
http
POST /addBooks


 📖 Get All Books

http
GET /books


 🔍 Get Books by Category

http
GET /books/category/:category

Example:
/books/category/Programming

📅 Get Books Published After 2015

http
GET /books/year/after2015


✏️ Update Available Copies
http
PUT /books/updateCopies/:id

**Body:**

json
{
  "change": 2
}


🔄 Change Book Category

http
PUT /books/changeCategory/:id

**Body:**

json
{
  "category": "AI"
}


 ❌ Delete Book (Only if copies = 0)

http
DELETE /books/delete/:id


🧪 Sample Book Model

json
{
  "title": "Clean Code",
  "author": "Robert C Martin",
  "category": "Programming",
  "publishedYear": 2008,
  "availableCopies": 5
}


📌 Validation Rules

* ❗ Available copies cannot be negative
* ❗ Books with available copies **cannot be deleted**


 📈 Future Enhancements

* Authentication (Admin/User)
* Frontend using React
* Pagination & search
* Book issue/return system


 👩‍💻 Author

**Darshini Amuluru**
B.Tech | Node.js & MongoDB Project


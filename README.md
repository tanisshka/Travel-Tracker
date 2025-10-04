
# 🌍 Visited Countries Tracker

A simple and interactive web app built with **Node.js**, **Express**, **EJS**, and **PostgreSQL** that lets users track the countries they have visited.  
Add new countries, view your visited list, and see your total travel count — all in one place.

---

## 🚀 Features
- Add countries dynamically via form input.  
- Display a list of visited countries with their total count.  
- Error handling for invalid or duplicate entries.  
- Secure environment variables using `.env`.  
- Clean and responsive front-end built with **EJS** templates.

---

## 🛠️ Tech Stack
- **Frontend:** EJS, HTML, CSS  
- **Backend:** Node.js, Express  
- **Database:** PostgreSQL  
- **Environment Management:** dotenv  

---

## ⚙️ Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/visited-countries-tracker.git
cd visited-countries-tracker
````

### 2. Install Dependencies

```bash
npm install
```

### 3. Setup Database

Create a PostgreSQL database named `world` with two tables:

```sql
CREATE TABLE countries (
  country_code VARCHAR(2) PRIMARY KEY,
  country_name TEXT NOT NULL
);

CREATE TABLE visited_countries (
  id SERIAL PRIMARY KEY,
  country_code VARCHAR(2) REFERENCES countries(country_code) UNIQUE
);
```

### 4. Add Environment Variables

Create a `.env` file in your root folder:

```
DB_USER=postgres
DB_HOST=localhost
DB_NAME=world
DB_PASSWORD=yourpassword
DB_PORT=5432
PORT=3000
```

### 5. Run the App

```bash
npm start
```

Now open:
👉 [http://localhost:3000](http://localhost:3000)

---

## 📁 Folder Structure

```
.
├── public/
│   └── style.css
├── views/
│   └── index.ejs
├── index.js
├── .env
├── .gitignore
└── package.json
```

---

## 💡 Live Demo

Coming soon! (You can deploy via Render, Railway, or Vercel)

---

## 🧑‍💻 Author

**Tanishka Patil**
Built with ❤️ using Node.js and PostgreSQL.

---

## 📜 License

This project is open-source and available under the **MIT License**.

```

---

Would you like me to include a short **database seed script** (to auto-insert countries into the `countries` table) in the README too? It makes your setup easier when others clone your repo.
```

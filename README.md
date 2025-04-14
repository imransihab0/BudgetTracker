# Budget Tracker 💸

A simple Java-based web application for managing your budget, built with **Tomcat**, **MySQL** (via XAMPP), and **JSP** for the front end. The application allows users to add, edit, delete, and view budget entries with a title, amount, and details. Each entry has a timestamp of when it was created.

## Features ✨

- **Add Budget**: Allows users to input a title, amount, and details for a new budget entry. 📝
- **Edit Budget**: Users can edit the details of an existing budget entry. ✏️
- **Delete Budget**: Users can remove a budget entry. 🗑️
- **View All Budgets**: View a list of all budgets with the date and time they were created. 📅

## Technologies Used 🛠️

- **Backend**: Java (JSP, Servlets) ☕
- **Database**: MySQL (via XAMPP) 🗄️
- **Web Server**: Apache Tomcat 🚀
- **Frontend**: HTML, CSS (Minimalist UI) 🎨

## Prerequisites 🖥️

Before running the project, make sure you have the following installed:

1. **JDK** (Java Development Kit) – For running the Java code. ☕
2. **Tomcat** – For running the web application. 🌐
3. **MySQL** (via XAMPP) – For the database. 🗃️
4. **Git** – For version control (optional, if you want to clone or manage your code). 🧑‍💻

## Setup 🔧

### Step 1: Clone the repository

Clone this repository to your local machine:

```bash
git clone https://github.com/yourusername/BudgetTracker.git
```

## Step 2: Configure the MySQL Database

- Start XAMPP and ensure MySQL is running. 🔴
- Open phpMyAdmin in your browser (usually at `http://localhost/phpmyadmin`). 🖥️
- Create a new database called `budget_tracker`. 🗂️
- Run the following SQL query to create the `budgets` table:

```sql
CREATE TABLE budgets (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    amount DECIMAL(10, 2) NOT NULL,
    details TEXT NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

## Step 3: Configure the Database Connection

Update the `DBConnection.java` file to match your MySQL setup. Change the following:

```java
private static final String DB_URL = "jdbc:mysql://localhost:3306/budget_tracker";  // Change the database name if needed
private static final String USER = "root";  // Your MySQL username
private static final String PASS = "";  // Your MySQL password (default is empty for XAMPP)
```

## Step 4: Deploy the Project to Tomcat

- Copy the entire project folder to the `webapps` directory of your Tomcat server. 📂
- Start Tomcat by running `startup.bat` (in the `bin` folder). ⚡
- Open your browser and navigate to `http://localhost:8080/BudgetTracker`. 🌐

---

## Step 5: Using the Application

- **Add a budget**: Enter a title, amount, and details, then click "Add Budget." 💡
- **Edit a budget**: Click "Edit" next to the budget you want to modify. ✏️
- **Delete a budget**: Click "Delete" next to the budget you want to remove. 🗑️
- **View all budgets**: The list of all budgets will be displayed with the creation date and time. 📅

---

## Contributing 🤝

If you'd like to contribute to this project:

- Fork the repository. 🍴
- Create a new branch for your feature (`git checkout -b feature-name`).
- Commit your changes (`git commit -am 'Add new feature'`).
- Push to the branch (`git push origin feature-name`).
- Create a new pull request. 🔄

---

## License 📜

This project is open source and available under the MIT License.

---

## Acknowledgements 🙏

- **Tomcat** for providing the web server. 🚀
- **MySQL** and **XAMPP** for the database and local development environment. 🗃️


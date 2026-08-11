# QuickLoan – Online Loan Application System

QuickLoan is a simple web-based loan application system developed using **HTML, CSS, PHP, and MySQL**. The application provides users with information about different loan products and allows them to submit a loan application online.

## 🚀 Features

* Responsive QuickLoan homepage
* Attractive loan product section
* Home Loan
* Gold Loan
* Vehicle Loan
* Personal Loan
* Online loan application form
* Customer details collection
* MySQL database integration
* PHP backend for processing applications
* Form validation using HTML
* Application submission and redirection

## 🛠️ Technologies Used

| Technology   | Purpose                       |
| ------------ | ----------------------------- |
| HTML5        | Website structure             |
| CSS3         | Styling and responsive layout |
| PHP          | Backend processing            |
| MySQL        | Database storage              |
| Apache       | Web server                    |
| Git & GitHub | Version control               |

## 📁 Project Structure

```text
quick loan/
│
├── public/
│   ├── index.html
│   ├── apply.php
│   ├── submit_application.php
│   ├── styles.css
│   │
│   └── images/
│       ├── gold_loan.jpg
│       ├── home_loan.jpg
│       ├── personal_loan.jpg
│       ├── vehicle_loan.jpg
│       └── quickloan_logo.png
│
├── includes/
│   └── db_connect.php
│
└── README.md
```

## 💰 Loan Products

The website currently provides four loan options:

### 🏠 Home Loan

Flexible loan options to help customers purchase their dream home.

### 🪙 Gold Loan

Quick financial assistance against eligible gold assets.

### 🚗 Vehicle Loan

Loan facilities for purchasing vehicles.

### 👤 Personal Loan

Personal financial assistance for urgent and individual requirements.

## 📝 Loan Application Process

1. Open the QuickLoan homepage.
2. Click **Apply for Loan**.
3. Enter your:

   * Name
   * Contact Number
   * Email Address
   * Loan Type
4. Click **Submit**.
5. The application is processed using PHP.
6. Customer information is stored in the MySQL database.
7. The user is redirected to the homepage after successful submission.

## 🗄️ Database Setup

The application uses MySQL to store loan applications.

Create a database:

```sql
CREATE DATABASE quickloan;
```

Create the applications table:

```sql
CREATE TABLE applications (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    contact VARCHAR(20) NOT NULL,
    email VARCHAR(100) NOT NULL,
    loan_type VARCHAR(50) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

## ⚙️ Database Configuration

Update the database connection in:

```text
includes/db_connect.php
```

Example:

```php
<?php

$servername = "localhost";
$username = "root";
$password = "";
$dbname = "quickloan";

$conn = new mysqli($servername, $username, $password, $dbname);

if ($conn->connect_error) {
    die("Database connection failed: " . $conn->connect_error);
}

?>
```

> **Note:** Do not upload real database passwords or other sensitive credentials to GitHub.

## 💻 How to Run the Project Locally

### 1. Install XAMPP

Install XAMPP and start:

* Apache
* MySQL

### 2. Copy the Project

Copy the project folder into:

```text
C:\xampp\htdocs\
```

For example:

```text
C:\xampp\htdocs\quick loan\
```

### 3. Create the Database

Open:

```text
http://localhost/phpmyadmin
```

Create a database named:

```text
quickloan
```

Then execute the SQL table creation query provided above.

### 4. Configure Database Connection

Make sure:

```text
includes/db_connect.php
```

contains the correct MySQL credentials.

### 5. Run the Website

Open:

```text
http://localhost/quick%20loan/public/index.html
```

Or, if you rename the folder to `quick-loan`:

```text
http://localhost/quick-loan/public/index.html
```

## 🌐 GitHub

This project is maintained using Git and GitHub for version control.

Repository:

**QuickLoan**

```text
https://github.com/vishakhajadhav1409/quick-loan
```

## 🔮 Future Enhancements

The project can be improved by adding:

* User login and registration
* Admin dashboard
* Application status tracking
* Loan eligibility calculator
* EMI calculator
* Email notifications
* SMS notifications
* Document upload
* Customer dashboard
* Admin approval/rejection system
* AWS deployment
* HTTPS and security improvements
* Responsive mobile-first design

## 🔐 Security Improvements

For a production deployment, the following should be implemented:

* Server-side input validation
* Password hashing
* Environment variables for credentials
* CSRF protection
* Secure session management
* Input sanitization
* HTTPS
* Proper error handling
* Database access restrictions

## 👩‍💻 Author

**Vishakha Jadhav**

MCA Graduate | AWS & DevOps Learner

## 📄 License

This project is created for educational and project-development purposes.

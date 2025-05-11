# Banking-System-using-Java-JDBC
A console-based Java Banking System using JDBC and MySQL. Features include user registration, account creation, balance inquiry, debit, credit, and fund transfer with secure authentication and transaction management. Ideal for learning JDBC, SQL integration, and backend banking workflows.

# 💳 JDBC Banking Management System

A simple yet fully functional **Banking Management System** built using **Java** and **JDBC** (MySQL).  
This console-based application allows users to securely manage their bank accounts — including **registration**, **account management**, and **transactions**.

---

## 🚀 Features

- ✅ User Registration & Login Authentication
- ✅ Open a New Bank Account (with secure PIN)
- ✅ Debit & Credit Money from Account
- ✅ Transfer Money between Accounts
- ✅ Check Account Balance
- ✅ SQL Transaction Management (Atomicity & Consistency)
- ✅ JDBC Prepared Statements (SQL Injection Safe)

---

## 🛠️ Tech Stack

- **Java 17+**
- **JDBC (Java Database Connectivity)**
- **MySQL 8.0+**
- **SQL (Structured Query Language)**

---

## 📂 Project Structure

JDBC.Projects.Bank.bANK
├── AccountManager.java # Handles all banking operations (debit, credit, transfer, balance)
├── Accounts.java # Manages account creation and account info
├── User.java # Handles user registration & login
└── App.java # Entry-point / Main application


2️⃣ Create MySQL Database & Tables
Run the following SQL queries in your MySQL server:
CREATE DATABASE test;
USE test;

CREATE TABLE User (
    id INT AUTO_INCREMENT PRIMARY KEY,
    full_name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    password VARCHAR(100) NOT NULL
);

CREATE TABLE Accounts (
    account_number BIGINT PRIMARY KEY,
    full_name VARCHAR(100) NOT NULL,
    email VARCHAR(100) NOT NULL,
    balance DOUBLE NOT NULL,
    security_pin VARCHAR(10) NOT NULL
);


3️⃣ Configure Database Credentials
In App.java, update the following variables with your MySQL credentials:
private static final String url = "jdbc:mysql://localhost:3306/test";
private static final String username = "root";
private static final String password = "your_mysql_password";



✨ Usage
Action	                                           Description
Register	                                  Create a user account
Open Account	                              Open a bank account linked to your email
Debit Money	                                Withdraw money from your account
Credit Money	                              Deposit money into your account
Transfer Money	                            Send money to another account
Check Balance	                              View your current balance
Log Out	                                    End session securely

🛡️ Security Highlights
Password and PIN verification before sensitive operations

SQL Prepared Statements to prevent SQL Injection

Atomic Transactions with commit & rollback for safe fund transfers

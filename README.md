# Bank Account Management System 
<p align="center">
  <img width="94" height="94" src="https://github.com/AnkitKumar-Mohbey/github-header-image.png"/>
</p>


## Overview
The **Bank Account Management System** is a Java-based application designed to manage bank accounts securely. The system provides functionalities such as user authentication, account management, balance inquiries, deposits, and withdrawals. It leverages a SQLite database to store customer and account information, ensuring data persistence and security.

## Key Features and Functionalities

### User Authentication:
- **Login**: Validates user credentials (username and password) to authenticate users before granting access.
- **Logout**: Ends the user session by resetting the authentication status.

### Account Management:
- **Account Creation**: Initializes account objects with unique identifiers, account types, and balances.
- **Balance Inquiry**: Allows users to check their current account balance.
- **Deposits**: Facilitates secure deposits into user accounts with validation checks.
- **Withdrawals**: Handles withdrawals with validation to prevent overdrafts and invalid amounts.

### Exception Handling:
- **AmountException**: Custom exception to handle errors related to invalid deposit and withdrawal amounts.
- **LoginException**: Handles errors during user login attempts, such as incorrect username or password.

### Database Integration:
- **SQLite Database**: Stores customer and account information persistently.
- **DataSource Class**: Manages database connections and executes SQL queries to interact with the database.
- **Prepared Statements**: Utilized to prevent SQL injection attacks and ensure secure data transactions.

### Menu-Driven Interface:
- **Interactive Menu**: Provides users with options to perform various banking operations.
- **User Prompts**: Guides users through authentication, balance inquiries, deposits, and withdrawals.

## Technical Stack
- **Programming Language**: Java
- **Database**: SQLite
- **Libraries and Frameworks**: JDBC (Java Database Connectivity)
- **Exception Handling**: Custom Exceptions (AmountException, LoginException)
- **Design Patterns**: Singleton for DataSource management

## Classes and Responsibilities

### Menu.java
- **Purpose**: Provides the main entry point and user interface for interacting with the banking system.
- **Key Methods**:
  - `main(String[] args)`: Initializes the application and prompts user authentication.
  - `authenticateUser()`: Prompts user for credentials and authenticates them.
  - `showMenu(Customer customer, Account account)`: Displays the menu and handles user selections.

### Account.java
- **Purpose**: Represents a bank account with functionalities to manage deposits and withdrawals.
- **Key Methods**:
  - `deposit(double amount)`: Adds funds to the account.
  - `Withdraw(double amount)`: Deducts funds from the account, with validation checks.

### Authenticator.java
- **Purpose**: Handles user authentication processes.
- **Key Methods**:
  - `login(String username, String password)`: Authenticates a user and returns the customer object.
  - `logout(Customer customer)`: Resets the authentication status of the user.

### Customer.java
- **Purpose**: Represents a bank customer with personal and account-related information.
- **Key Attributes**:
  - `id`: Unique identifier for the customer.
  - `username`: User's login name.
  - `passward`: User's password.
  - `accountId`: Associated account identifier.
  - `authenticated`: Authentication status flag.

### DataSource.java
- **Purpose**: Manages database connections and executes SQL queries.
- **Key Methods**:
  - `connect()`: Establishes a connection to the SQLite database.
  - `getCustomer(String username)`: Retrieves customer data from the database.
  - `getAccount(int accountId)`: Retrieves account data from the database.
  - `updateAccountBalance(int accountId, double balance)`: Updates the account balance in the database.

### AmountException.java
- **Purpose**: Custom exception to handle invalid amounts during deposits and withdrawals.

## Highlighted Achievements for Resume

- Developed a comprehensive banking system using Java, incorporating user authentication, account management, and secure database interactions.
- Implemented custom exception handling to manage and prevent invalid transactions and authentication errors.
- Utilized JDBC with SQLite to ensure robust and secure data storage and retrieval.
- Designed and developed a user-friendly menu-driven interface for seamless user interaction.
- Applied best practices for security, including SQL injection prevention and secure password handling (in real-world scenarios).

## Getting Started

### Forking the Repository
To contribute to the project, you can fork the repository on GitHub. Follow these steps:
1. Go to the repository page: [Bank Account Management System](https://github.com/AnkitKumar-Mohbey/Bank-Account-Management-System).
2. Click the **Fork** button in the top-right corner of the page.

### Downloading the Project
To download the project, follow these steps:
1. Go to your forked repository on GitHub.
2. Click the **Code** button.
3. Choose **Download ZIP** to download the project files.

### Cloning the Repository
Alternatively, you can clone the repository using Git:
```bash
git clone https://github.com/YourUsername/Bank-Account-Management-System.git

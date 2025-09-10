# Banking System - Java Swing Application

## Overview
A comprehensive Java Swing-based banking system that simulates real-world banking operations with a user-friendly graphical interface. The application provides complete account management, transaction processing, and administrative functions.

## Features

### Core Banking Operations
- **Account Management**
  - Create new accounts (Current, Savings, Student)
  - View account details and balances
  - Account listing and search functionality

- **Transaction Processing**
  - Deposit money to accounts
  - Withdraw money from accounts
  - Real-time balance updates
  - Transaction confirmation dialogs

- **User Interface**
  - Modern Java Swing GUI
  - Login authentication system
  - Intuitive navigation between different modules
  - Error handling with user-friendly messages

### Account Types
1. **Current Account** - Standard checking account
2. **Savings Account** - Interest-bearing savings account
3. **Student Account** - Special account type for students



## Technologies Used
- **Java 17+** - Core programming language
- **Java Swing** - GUI framework
- **File I/O** - Data persistence
- **Exception Handling** - Robust error management

## Project Structure
```
src/
├── Application.java              # Main application entry point
├── Bank/                         # Core banking logic
│   ├── Bank.java                # Main bank class
│   ├── BankAccount.java         # Base account class
│   ├── CurrentAccount.java      # Current account implementation
│   ├── SavingsAccount.java      # Savings account implementation
│   └── StudentAccount.java      # Student account implementation
├── GUI/                         # User interface components
│   ├── GUIForm.java            # Main GUI controller
│   ├── Login.java              # Login screen
│   ├── Menu.java               # Main menu
│   ├── AddAccount.java         # Account creation forms
│   ├── DepositAcc.java         # Deposit functionality
│   ├── WithdrawAcc.java        # Withdrawal functionality
│   └── DisplayList.java        # Account listing
├── Data/
│   └── FileIO.java             # File operations
└── Exceptions/                  # Custom exception classes
    ├── AccNotFound.java
    ├── InvalidAmount.java
    ├── MaxBalance.java
    └── MaxWithdraw.java
```

## Installation & Setup

### Prerequisites
- Java Development Kit (JDK) 17 or higher
- Git (for cloning the repository)

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone <>
   cd BankingSystem-master
   ```

2. **Compile the project**
   ```bash
   javac -d bin -cp src src/Application.java
   ```

3. **Run the application**
   ```bash
   java -cp bin Application
   ```

## Usage

### Login
1. Launch the application
2. Use the following credentials:
   - **Username:** `admin`
   - **Password:** `admin`
3. Click "Login" to access the main menu

### Main Operations

#### Account Management
- **Create Account**: Navigate to "Add Account" and select account type
- **View Accounts**: Use "Display List" to see all accounts
- **Account Details**: View account numbers, balances, and account types

#### Transactions
- **Deposit**: Select "Deposit" from menu, enter account number and amount
- **Withdraw**: Select "Withdraw" from menu, enter account number and amount
- **Balance Inquiry**: View current balance for any account

### Navigation
- Use the main menu to navigate between different functions
- All forms include proper validation and error handling
- Confirmation dialogs for important operations

## Known Issues & Notes

### Current Issues
- **Deposit Function**: There's a known NumberFormatException when the amount field is empty
  - **Workaround**: Always ensure amount fields are filled before submitting

### Error Handling
The application includes comprehensive error handling for:
- Invalid account numbers
- Insufficient funds
- Invalid amounts
- Maximum balance/withdrawal limits

## Development

### Building from Source
```bash
# Compile all source files
javac -d bin -cp src src/**/*.java

# Run the application
java -cp bin Application
```

### Code Structure
- **MVC Pattern**: Clear separation between GUI, business logic, and data
- **Exception Handling**: Custom exceptions for different error scenarios
- **File Persistence**: Data is saved to `data.bin` file
- **Modular Design**: Each GUI component is a separate class

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -m 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

## Future Enhancements

- [ ] Database integration (replace file-based storage)
- [ ] Enhanced security features
- [ ] Transaction history logging
- [ ] Interest calculation for savings accounts
- [ ] Account statement generation
- [ ] Multi-user support with role-based access
- [ ] Data encryption for sensitive information

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Java Swing framework for the GUI components
- Java community for excellent documentation and examples
- Contributors who have helped improve this project

## Support

For issues, questions, or contributions, please:
1. Check the existing issues in the repository
2. Create a new issue with detailed description
3. Follow the contribution guidelines

---

**Note**: This is a demonstration project for educational purposes. It should not be used for actual banking operations without proper security measures and compliance with banking regulations.

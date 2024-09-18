### Overview
1. *Database Setup:* The notebook connects to a SQLite database (Online_Store.db) and initializes three tables:
   - signup: Stores user information (email, name, phone number, password).
   - store: Stores product information (product ID, name, quantity, price).
   - cart: Stores cart details (order ID, product name, quantity, total).

2. *Features:*
   - *Signup/Login:* Users can sign up and log in using their email and password.
   - *Product Management:* Users can check available products.
   - *Cart Management:* Users can add items to their cart and check out.

3. *Authentication:* There’s a hardcoded check for an employee ID (123) and password (1111) to access the system’s functionality.

### External Libraries:
- *SQLite3:* For database management.
- *Matplotlib & Numpy:* These libraries are imported but seem unused in the provided cells.
- *Getpass:* For password input masking.

The QR code might link to this system or its repository, which we can integrate into the README.

Let me proceed to draft the README based on this information.

# README for Online Store Management System

## Project Overview

The *Online Store Management System* is a simple Python-based application that manages an online store's users, products, and shopping carts. The system is built using *Python* and *SQLite* and provides essential functionalities like user signup/login, product browsing, and adding items to a shopping cart.

This project is useful for anyone looking to create a simple e-commerce backend using a database-driven approach. The application is designed to run in a Jupyter Notebook environment, making it easy to visualize and execute code in a sequential manner.

## Prerequisites

To run the program, you will need the following:

1. *Python 3.x* installed on your machine.
2. The following Python libraries:
   - sqlite3
   - getpass
   - numpy (though not used in current functionality)
   - matplotlib (imported but unused)
   
   You can install missing dependencies via pip:
   bash
   pip install numpy matplotlib
   

3. *Jupyter Notebook* or any environment that can run .ipynb files.

## Files in the Project

### 1. Online_Store.ipynb
This Jupyter Notebook contains the code that powers the online store. It includes the following key functionalities:

- *Database Setup:* 
  - The notebook connects to an SQLite database named Online_Store.db.
  - It creates three tables (signup, store, and cart) if they do not already exist.
  
- *Signup and Login:*
  - Users can sign up with their email, name, phone number, and password.
  - The system checks for existing emails to prevent duplicate signups.
  - Users can log in with their credentials, or administrators can log in using hardcoded employee credentials.
  
- *Product Browsing:*
  - The system allows users to view available products from the store table in the database.
  
- *Cart Management:*
  - Users can add items to their shopping cart and complete transactions.

### 2. Online_Store.db
This is the SQLite database file that stores all user, product, and order information. The following tables are used:

- *signup:* Holds user credentials such as email, name, phone number, and password.
- *store:* Stores product details including product ID, name, quantity, and price.
- *cart:* Stores cart data for each user's order including product name, quantity, and the total cost.

The application interacts with this database file to retrieve and update information.

### 3. qrcode.png
This image file contains a QR code, which may direct users to the online repository or a webpage for the project. This can be printed on flyers or posters for easy access to the project files or system link.

## How to Run the Project

1. *Set up the Environment:*
   Ensure you have all necessary Python libraries installed. If running this from a Jupyter Notebook environment, ensure it supports these libraries.

2. *Run the Notebook:*
   Open the Online_Store.ipynb file in Jupyter Notebook and execute the cells in order. 

   - *Employee Login:*
     The initial login requires an employee ID (123) and a password (1111). This ensures the user has administrative privileges to access the system.
   
   - *Main Menu Options:*
     Once logged in, users will see the following options:
     
     Press 1 for Signup
     Press 2 for Login
     Press 3 for Check Products
     Press 4 for Exit
     

     - *Press 1:* To create a new user account by providing an email, name, phone number, and password.
     - *Press 2:* To log in as an existing user.
     - *Press 3:* To browse products from the store and view their details (product name, quantity, price).
     - *Press 4:* To exit the system.

3. *Database Management:*
   - *Add Products:* You can manually add products to the store table using SQLite queries if needed. This step is essential if you want to populate the store with products for users to browse.

4. *Usage:*
   - After login, users can browse available products, add items to their cart, and proceed to checkout.
   - The cart data is stored in the cart table with details such as product name, quantity, and total price.
  
5. *QR Code Usage:*
   The included qrcode.png can be used to direct users to the project repository or to a website where this system is hosted. To scan the QR code:
   - Use any QR code scanner on your mobile device.
   - It will take you to the relevant link (this part depends on how you set up the QR code).

## Example Workflow

1. *Admin Login:*
   
   Employee ID: 123
   Password: ****
   

2. *Main Menu Options:*
   
   Press 1 for Signup
   Press 2 for Login
   Press 3 for Check Products
   Press 4 for Exit
   

3. *User Signup (if not registered):*
   - Enter email, name, phone number, and a password.

4. *Browse Products:*
   - View the list of available products along with their prices and quantities.

5. *Add to Cart:*
   - Choose products and specify the quantity to add to your cart.

6. *Checkout:*
   - Once products are added to the cart, you can proceed to checkout and complete the transaction.

7. *Exit the System:*
   - Press 4 to safely exit the system.

## Notes

- *Security:* The login and signup process should be updated with more secure password management methods (e.g., password hashing) for production use. In the current version, passwords are stored in plaintext, which is not secure.
  
- *Data Management:* The system uses a basic SQLite database for data management. If scaling to larger environments, consider using a more robust database like PostgreSQL or MySQL.

- *Additional Features:* The code contains provisions for future enhancements such as product recommendations, order history tracking, and analytics, which can be easily integrated.

## Conclusion

This system is a minimal yet functional example of how an online store's backend can be managed using Python and SQLite. With a few enhancements, it could serve as a useful prototype for a small-scale e-commerce application.
Feel free to extend this system by adding more functionalities or integrating a front-end to make the store interactive!

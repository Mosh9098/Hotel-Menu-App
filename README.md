# Application Name: MENU MANAGEMENT SYSTEM

#### By: David Maina

## Description

The Menu Management System is a web-based application designed to streamline and manage menu items for a hotel. The system allows users to log in, create orders from the menu, and enables administrators to add, edit, and delete menu items. This ensures efficient management of the menu and provides a user-friendly interface for both staff and administrators to handle daily operations.

## Key Features

- **User Authentication**: Secure login functionality allowing only authorized users to access the system.
  - **Staff**: Can log in and create orders from the menu.
  - **Admin**: Can log in, add new menu items, edit existing items, and delete items no longer offered.
- **Menu Management**: Administrators can manage the menu by adding, editing, and deleting items.
- **Order Management**: Staff can create orders by selecting items from the menu and view a list of all orders, including details such as items ordered, quantities, and total cost.

## How It Works

1. **User Authentication**:
   - Users (both staff and admin) need to log in with their Email and their passwords to access the main home pages system.

2. **Admin Functions**:
   - After logging in, admins can add new menu items by navigating to the "Menu main page" section, filling in the details, and adding item.
   - Admins can edit existing items by selecting an item from the menu list, updating the details, and saving the changes.
   - Admins can delete items no longer offered by selecting the item and confirming the deletion.
    - Admins can view all items that are in oders that have been created by the staff.
     - Admins can View everything that is on menu list.
    

3. **Staff Functions**:
   - After logging in, staff can create orders by selecting items from the menu and adding them to the order list this will be through adding to cart this will create an order.
   - Staff can search a specific meal that they want from what we offer.
   - Staff can view all created orders, including details such as items ordered, quantities, and total cost.

4. **Order Management**:
   - All users can view a list of all orders, including detailed information about each order including their prices too but this is mostly controlled by the admin.


## Technologies used
- HTML
- CSS
- Github
- React
- Python 3.8+
- Flask
- SQLite

## Introduction to how to acess Whats in our App
## Installation

To install and run the Menu Management System locally, follow these steps:


1  **Clone the repository**:
git clone https://github.com/tubisaffo/python-p4-Hotel-Menu-project
cd repository-python-p4-Hotel-Menu-project 


2 **Set up virtual environment** (Must ):
 pipenv install

 pipenv shell
3  **Set up database**:
Do not worry we have deployed that for you in render so relax.
4  **Run the application**:
- npm install
- npm start
- This will start the react front end
-  Check that your the React client displays a default page You can run your React app on [`localhost:3000`](http://localhost:3000) by
running:

5  **Login**:
- Use the provided credentials (admin or staff) to log in and start using the system.

6 **Start managing menus and orders**:
- Explore the menu management and order creation features as described in the README.

## The Menu Management System's database schema includes the following tables:

    Users:
        id: Integer, Primary Key
        email: String, Unique
        password: String
        role: String (either 'admin' or 'staff')

    MenuItems:
        id: Integer, Primary Key
        name: String
        description: String
        price: Float
        availability: Boolean

    Orders:
        id: Integer, Primary Key
        user_id: Integer, Foreign Key (references Users.id)
        total_cost: Float
        order_date: DateTime

    OrderItems:
        id: Integer, Primary Key
        order_id: Integer, Foreign Key (references Orders.id)
        menu_item_id: Integer, Foreign Key (references MenuItems.id)
        quantity: Integer


### License
MIT License

© 2024 David Maina



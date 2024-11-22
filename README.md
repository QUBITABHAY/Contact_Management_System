# Contact_Management_System
This repo contains python code of managing contacts. 


Contactbook Application
This is a simple Contactbook application built using Python, Tkinter (for the GUI), and MySQL (for storing contact information). The app allows users to manage contacts with options to Add, Edit, Search, Delete, and View all contacts. This project is designed for personal use or as a beginner's project to learn about GUI development and database integration in Python.

Features
Add Contact: Add a new contact with fields for First Name, Last Name, Address, Phone Number, and Email.
Edit Contact: Update an existing contact by searching with the phone number.
Search Contact: Search for contacts by first name or phone number.
Delete Contact: Delete a contact by either first name or phone number.
View All Contacts: View a list of all contacts stored in the database.
Clear Fields: Clear input fields for new data entry.
Requirements
Python: Ensure Python 3.x is installed on your system.
MySQL: A MySQL server should be running, and a database should be created for storing contact information.
Python Libraries
mysql-connector: For connecting to the MySQL database.
tkinter: For creating the graphical user interface.
ttk: For additional styling of widgets.
Install the required Python packages using pip:

bash
Copy code
pip install mysql-connector-python
Setup
Install MySQL (if not already installed):

Follow the installation instructions for MySQL: https://dev.mysql.com/downloads/installer/
Create a Database:

Open MySQL command line or a MySQL client and create the database abhay:

sql
Copy code
CREATE DATABASE abhay;
Set up the Contactbook Table:

The application automatically creates the contactbook table upon startup if it does not already exist. However, if you prefer to create it manually, you can use the following SQL command:

sql
Copy code
CREATE TABLE IF NOT EXISTS contactbook (
    fname varchar(50) primary key, 
    lname varchar(50), 
    address varchar(100),
    number numeric(12) primary key,
    email varchar(20)
);
Configure the MySQL Connection:

In the Python script, update the connection details to match your MySQL setup:

python
Copy code
my = sql.connect(host="localhost", user="root", password="your_mysql_password", database="abhay")
Make sure to replace your_mysql_password with your actual MySQL password.

Running the Application
Clone or download the repository to your local machine.

Navigate to the project directory in the terminal.

Run the contactbook.py script:

bash
Copy code
python contactbook.py
The Contactbook application window will open, allowing you to add, edit, search, delete, or view contacts.

Code Explanation
MySQL Integration: The application uses the mysql.connector library to interact with the MySQL database. It performs operations such as adding, editing, deleting, and searching contacts.
Tkinter GUI: The GUI is built using Tkinter, with different frames and widgets for the operations. Each frame corresponds to an operation (add, edit, search, delete).

Contributing
Feel free to fork the repository, report issues, or submit pull requests. Any contributions to improve the functionality or design of the application are welcome!
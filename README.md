# Contact Management System
A Python-based contact management application with GUI and MySQL database integration.

## Features
- Add, edit, search and delete contacts
- View all contacts in a list
- Store contact details (name, address, phone, email)
- User-friendly Tkinter interface
- MySQL database backend

## Requirements
- Python 3.x
- MySQL Server
- Libraries: mysql-connector-python, tkinter

## Quick Start
1. Install dependencies:
```bash
pip install mysql-connector-python
```

2. Create MySQL database:
```sql
CREATE DATABASE your_database;
```

3. Update MySQL credentials in `contactbook.py`:
```python
my = sql.connect(
    host="localhost",
    user="root", 
    password="your_password",
    database="your_database"
)
```

4. Run the application:
```bash
python contactbook.py
```

## Database Schema
```sql
CREATE TABLE contactbook (
    fname varchar(50) primary key,
    lname varchar(50),
    address varchar(100), 
    number numeric(12) primary key,
    email varchar(20)
);
```

## Contributing
Contributions welcome! Feel free to:
- Report issues
- Submit pull requests
- Suggest improvements

## License
Open source software. Use and modify freely.

Task Monitoring Application
Task Monitoring Application is a Flask-based web application that allows users to sign up, log in, and track tasks. This project uses SQLAlchemy to interact with a MySQL database and PyMySQL as the MySQL connector.

Table of Contents
Features
Tech Stack
Project Setup
Database Setup
Running the Application
Usage
Troubleshooting
Contributing
License
Features
User registration and login functionality
Task creation and management
Secure password storage using hashing
Error handling and validation
Database integration using SQLAlchemy
Tech Stack
Backend: Flask, SQLAlchemy
Database: MySQL with PyMySQL connector
Frontend: HTML, CSS (optional for styling)
Authentication: Password hashing (can add libraries like bcrypt or werkzeug)
Project Setup
Prerequisites
Make sure you have the following installed:

Python 3.x
MySQL database
pip (Python package installer)
Installation Steps
Clone the repository:


git clone https://github.com/ayushraj5514/task-management.git
cd task_monitor
Set up a virtual environment (optional but recommended):


python -m venv venv
source venv/bin/activate   # On Windows use venv\Scripts\activate
Install the required dependencies:


pip install -r requirements.txt
Environment Variables
Create a .env file in the root of the project directory to store sensitive information like database credentials.


FLASK_APP=app.py
FLASK_ENV=development
DATABASE_URI=mysql+pymysql://root:<password>@localhost/<database_name>
SECRET_KEY=<your_secret_key>
Replace <password> and <database_name> with your MySQL credentials.

Database Setup
Make sure MySQL is installed and running.

Create a MySQL database:


CREATE DATABASE task_monitor;
Update the DATABASE_URI in your .env file.

Initialize the database tables:


flask db init
flask db migrate
flask db upgrade
Running the Application
Start the Flask development server:


flask run
The app should now be running on http://127.0.0.1:5000/.

Usage
Open your browser and navigate to http://127.0.0.1:5000/.
Register a new account.
Log in with your new credentials.
Start creating and managing tasks.
Troubleshooting
Common Errors
Error: (pymysql.err.OperationalError) (1045, "Access denied for user 'root'@'localhost')
Solution:

Ensure the database credentials are correct.
Check if your MySQL server is running and accessible.
Error: sqlalchemy.exc.OperationalError
Solution:

Verify your DATABASE_URI in the .env file.
Check if the database and user permissions are set correctly.
Database Authentication Issues
Make sure the user credentials are correct and that the user has the required privileges on the MySQL database. You can test the connection using the MySQL command line.

Contributing
Fork the repository.
Create a new branch (git checkout -b feature/new-feature).
Commit your changes (git commit -am 'Add new feature').
Push to the branch (git push origin feature/new-feature).
Open a Pull Request.
License
This project is licensed under the MIT License. See the LICENSE file for details.

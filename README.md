# LostAndFound
LostAndFound

LostAndFound is a full-stack web application built with Flask that provides a platform for users to report lost items and for others to report items they have found. The system features separate dashboards for users and administrators, enabling efficient management of items and users.
# Features
User Features

    Secure Authentication: Users can register for an account and log in securely.
    User Dashboard: A personalized dashboard where users can view a summary of their reported lost and found items.
    Report Items: A simple form to report a lost or found item, including details like name, description, location, and an optional image upload.
    View Reported Items: Users can see lists of items they have personally reported, separated by 'Lost' and 'Found' status.

Admin Features

    Admin Dashboard: A comprehensive control panel for administrators, showing statistics like total users, total items, and breakdowns by status.
    User Management: Admins can view a list of all registered users, their emails, and their admin status.
    Item Management: Admins have a global view of all items reported on the platform.
    Update & Delete: Admins can edit item details, update an item's status (e.g., mark a 'Lost' item as 'Found'), and delete item reports from the system.

Tech Stack

    Backend: Flask, Flask-SQLAlchemy, Flask-Login, Flask-WTF
    Database: SQLAlchemy (defaulting to SQLite)
    Frontend: HTML, Jinja2, Bootstrap 5
    Deployment: The application is configured to run with a standard Python environment.

# Getting Started

Follow these instructions to get a local copy of the project up and running.
Prerequisites

    Python 3.x
    Git

Installation & Setup

    Clone the repository:

    git clone https://github.com/adityaargade07/LostAndFound.git
    cd LostAndFound

    Create and activate a virtual environment:

    # For macOS/Linux
    python3 -m venv venv
    source venv/bin/activate

    # For Windows
    python -m venv venv
    .\venv\Scripts\activate

    Install the required dependencies: Note: The requirements file in the repo is named requirements.txt.txt. Rename it to requirements.txt before running the command.

    pip install -r requirements.txt

    Configure Environment Variables: Create a .env file in the root directory and add the following variables. A strong SECRET_KEY is crucial for production.

    SECRET_KEY='a_secure_random_string_for_sessions'
    SQLALCHEMY_DATABASE_URI='sqlite:///instance/lost_and_found.db'

    # Optional for email notifications (if feature is enabled)
    # MAIL_USERNAME='your-email@example.com'
    # MAIL_PASSWORD='your-email-password'

    Run the application: The application will create the database and tables on the first run.

    python run.py

    The application will be available at http://127.0.0.1:5003.

# Usage

    Navigate to the Homepage: Open your browser to the application's URL.
    Register/Login:
        New users can create an account using the Register button.
        Existing users can log in via the Login page.
        Administrators should use the Admin Login link for access to the admin panel.
    Report an Item: Once logged in, users can click "Report Item" on their dashboard to fill out the form for a lost or found object.
    Manage Items (Admin): Logged-in admins can access the "Admin Panel" to view all reported items, manage users, and update item statuses as necessary.

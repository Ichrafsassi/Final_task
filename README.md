# Overview 
This API provides user management functionalities, including user registration, login, and admin capabilities, with role-based access control.

### Technologies Used 
- Python 
- Flask 
- Flask-SQLAlchemy 
- Flask-JWT-Extended

### Installation

**Clone the Repository** 
```bash 
git clone https://github.com/Ichrafsassi/Final_task.git 
```

Create a Virtual Environment
```bash
python -m venv venv 
```

Activate the Virtual Environment

On Windows:
```bash
venv\Scripts\activate 
```

On macOS/Linux:
```bash
source venv/bin/activate 
```

Install Dependencies
```bash
pip install -r requirements.txt 
```

Running the Application
Set Environment Variables
Make sure to set your environment variables for the JWT secret key and database URI if necessary.
Run the Application

```bash
flask run 
```

The API will be accessible at http://127.0.0.1:5000/.
API Endpoints

User Registration

    POST /register
        Registers a new user.
        Requires a JSON body with fields: username, first_name, last_name, email, phone_number, password.

User Login

    POST /login
        Authenticates a user and returns a JWT token.
        Requires a JSON body with fields: email, password.

Admin Only Page

    GET /admin_only_page
        Accessible only by admin users.

Create Admin

    POST /create_admin
        Allows admin users to create a new admin account.
        Requires a JSON body with fields: username, first_name, last_name, email, phone_number, password.

All Users

    GET /all_users
        Retrieves a list of all users.

Visitor Page

    GET /visitor
        Accessible by anyone.

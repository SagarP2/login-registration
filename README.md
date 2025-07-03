# Login Registration App

This project is a Flask web application that provides user registration, login, and a dashboard for authenticated users. It uses a MySQL database to store user information and bcrypt for password hashing.

## Project Structure

```
login-registration-app
├── app.py
├── templates
│   ├── index.html
│   ├── register.html
│   ├── login.html
│   └── dashboard.html
├── requirements.txt
└── README.md
```

## Setup Instructions

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd login-registration-app
   ```

2. **Create a virtual environment** (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install the required packages**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up the MySQL database**:
   - Create a database named `flask_app` (or the name specified in `app.py`).
   - Create a `users` table with the following structure:
     ```sql
     CREATE TABLE users (
         id INT AUTO_INCREMENT PRIMARY KEY,
         name VARCHAR(100),
         email VARCHAR(100) UNIQUE,
         password VARCHAR(255)
     );
     ```

5. **Run the application**:
   ```bash
   python app.py
   ```

6. **Access the application**:
   Open your web browser and go to `http://127.0.0.1:5000`.

## Usage

- Navigate to the registration page to create a new account.
- After registering, log in using your credentials.
- Once logged in, you will be redirected to the dashboard.

## Dependencies

- Flask
- Flask-WTF
- Flask-MySQLdb
- bcrypt

## License

This project is licensed under the MIT License.
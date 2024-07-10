# Library Management System - Backend

This is the backend part of the Library Management System, a Flask-based application that allows users to manage books, loans, and user accounts in a library setting.

## Features

### User Management
- User registration with profile photo upload
- User authentication and authorization (JWT)
- View user profile
- Admin functionalities:
  - View all users
  - Update user details
  - Activate/deactivate users

### Book Management
- Add new books (Admin)
- Update book details (Admin)
- Upload book cover images
- View all books
- Loan a book
- Return a book
- Activate/deactivate books (Admin)

### Loan Management
- View all loans (Admin)
- View late loans (Admin)
- User-specific loan management

## Technologies Used

- Flask
- SQLAlchemy (SQLite database)
- Flask-JWT-Extended for authentication
- Werkzeug for password hashing and file uploads

## Setup and Installation

1. Clone the repository
2. Navigate to the backend directory
3. Create a virtual environment:  

       python -m venv venv
4. Activate the virtual environment:
- On Windows: `venv\Scripts\activate`
- On macOS and Linux: `source venv/bin/activate`
5. Install the required packages:    
        
        pip install -r requirements.txt  
6. Run the application:  
       
       python app.py           
       
The application connects to the backend service running at `https://backend-project-library-flask.onrender.com`.  
or  
The application connects to the backend service running at http://127.0.0.1:5057. (local, befor render)  

The `index.html` file references the `script.js` file, which connects to the backend through:  

document.addEventListener("DOMContentLoaded", () => {
    const apiUrl = "https://backend-project-library-flask.onrender.com";
});  

Before deploying to Render, it was:  

document.addEventListener("DOMContentLoaded", () => {
    const apiUrl = "http://127.0.0.1:5057";
});  

(port=5057)


## Usage

### Admin Account
To access admin features, use the following credentials:
- Username: Eva
- Password: eva543

### User Registration and Login
- New users can register by providing a username, password, email, city, and profile photo.
- Registered users can log in to access their profiles and library functions.

### User and Admin Functionality
- Users can:
- View their profile information
- Search for books
- View all available books
- Loan books
- Return books
- View their loan history
- Admins have additional capabilities:
- Add new books with details (title, author, published year, type) and cover images
- Update existing book information
- Remove (deactivate) or reactivate books
- View and manage all users (update info, activate/deactivate accounts)
- Access all loan information
- View reports on late loans

### Book Management
- Books can be added with full details including cover images
- Book information can be updated
- Books can be marked as active or inactive

### Loan System
- Users can loan available books and return them
- The system tracks loan dates and identifies late returns based on book type
- Admins can view all current loans and a separate list of late loans

## File Structure
- `app.py`: Main application file
- `instance/`: Contains the SQLite database
- `media/`: Stores uploaded images (book covers and user profiles)
- `requirements.txt`: List of Python dependencies
- `README.md`: This file

## Frontend

For the frontend part of this application, please refer to [[Frontend Repository Link](http://evafrontlibrary.netlify.app)].       

This project is built to verify users through email before they can log in. When a user registers, an OTP is sent to their Gmail. Only after entering the correct OTP, the account gets verified and the user can log in using JWT authentication.

Features

User Registration with email validation
OTP generation and verification via Gmail SMTP
JWT based Login and Authentication
Secure password handling
Resend OTP option
Clean and simple REST APIs

Tech Stack

Backend: Python, Django, Django REST Framework
Database: SQLite3
Authentication: JWT (Simple JWT)
Email Service: Gmail SMTP
Frontend Testing: Postman

How It Works

1. User registers with name, email and password.
2. System generates a 6-digit OTP and sends it to the user's Gmail.
3. User enters the OTP to verify the account.
4. After successful verification, user can log in.
5. On login, a JWT Access Token and Refresh Token is generated.
6. This token is used to access protected APIs.

API Endpoints
Method Endpoint Description
POST /api/register/ Register a new user
POST /api/verify-otp/ Verify OTP sent to email
POST /api/resend-otp/ Resend OTP
POST /api/login/ Login and get JWT token
 How To Run This Project
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
Server will run on `http://127.0.0.1:8000/`

Future Improvements

- Add Forgot Password using OTP
- Add OTP expiry time
- Add frontend using React

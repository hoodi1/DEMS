# DEMS

This is a simple Flask web application that provides OTP (One-Time Password) generation and login functionality. It allows users to receive an OTP via email and implements login restrictions for certain routes using custom decorators.

## Features

- Generate OTP: Users can request an OTP that will be sent to their registered email address.
- Login Required: Certain routes require users to be logged in to access them.
- Admin Login: Some routes require administrative privileges to access.

## Requirements

- Python 3.x
- Flask
- `random` module (built-in)
- `smtplib` module (built-in)
- `functools.wraps` (built-in)

## Getting Started

1. Clone or download this repository to your local machine.

2. Install the required dependencies using the following command:

   ```
   pip install Flask
   ```

3. Set up your Gmail account credentials in the `generate_otp()` function to enable sending emails.

4. Run the Flask application using the following command:

   ```
   python app.py
   ```

5. Access the application in your web browser by navigating to `http://127.0.0.1:5000/`.

## Usage

### OTP Generation

1. Visit the homepage of the web application.
2. Click on the "Generate OTP" button and enter your registered email address.
3. An OTP will be generated and sent to the provided email address.
4. The generated OTP will also be stored in the session for later use.

### Login and Restricted Routes

1. To access routes protected by the `login_required` decorator, you must first log in.
2. Access the "/employee_login" page and provide the necessary login credentials.
3. After successful login, you will be redirected to the restricted route you attempted to access initially.

### Admin Login and Restricted Routes

1. To access routes protected by the `admin_login_required` decorator, you must first log in as an admin user.
2. Access the "/admin_login" page and provide the admin login credentials.
3. After successful login, you will be redirected to the restricted admin route you attempted to access.

## Note

- This application uses Gmail's SMTP server to send emails. Make sure to set up your Gmail account credentials in the `generate_otp()` function before using the OTP generation feature.

- This is a basic demonstration of OTP generation and login functionality. In a real-world scenario, more robust security measures and user authentication systems should be implemented.

## License

This project is licensed under the [MIT License](LICENSE).

---

Please adjust the contents, formatting, and other details in the `README.md` file to reflect your specific project and implementation. The above template serves as a starting point to provide essential information to users about your Flask web application.

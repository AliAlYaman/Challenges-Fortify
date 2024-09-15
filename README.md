# API Setup for Frontend Testing using Laravel Fortify

This API is created using **Laravel Fortify**. Please note that the `.gitignore` file has been intentionally deleted for simplicity in this development branch. **This should not be done in production** as it poses a security risk by exposing sensitive files.

## Steps to Set Up the Project

### 1. Clone the Repository

To clone this repository to your local machine, open your terminal and run the following command:

  ```bash
  git clone https://github.com/AliAlYaman/Challenges-Fortify.git
  ```
### 2. Change directory and checkout branch

  ```bash
  cd fortify
  git checkout api
  ```

### 3. Setup PostgreSQL
If you do not have PostgreSQL installed, you can install pgAdmin4 for managing PostgreSQL databases:

[Download pgAdmin4](https://www.pgadmin.org/download/pgadmin-4-windows/)

After installing PostgreSQL and pgAdmin4, follow these steps:

Open pgAdmin4 and log in.
Create a new database called fortify.

### 4. Update the .env File:
Now, update your .env file with the PostgreSQL credentials:
```bash
DB_CONNECTION=pgsql
DB_HOST=127.0.0.1
DB_PORT=5432
DB_DATABASE=fortify
DB_USERNAME=your_postgres_username
DB_PASSWORD=your_postgres_password
```
### 5. Migrate the Database:
```bash
php artisan migrate
```
### 6. Mailtrap Setup:
To test email functionality (like email verification and password reset), you need to set up a Mailtrap account.

[Sign up for Mailtrap](https://mailtrap.io/)
Create a new inbox (project) in Mailtrap.
Get the credentials for the SMTP configuration (Mailtrap provides this under your inbox settings).
Update the .env File:
Replace the default mail configuration in the .env file with your Mailtrap credentials:
```bash
MAIL_MAILER=smtp
MAIL_HOST=sandbox.smtp.mailtrap.io
MAIL_PORT=2525
MAIL_USERNAME=your_mailtrap_username
MAIL_PASSWORD=your_mailtrap_password
MAIL_ENCRYPTION=null
MAIL_FROM_ADDRESS=your_email@example.com
MAIL_FROM_NAME="Your App Name"
```

### 7. Run the Laravel Development Server:
```bash
php artisan serve
```

### 8. API Documentation:
This project’s API is documented using Postman. You can find the full API documentation here:

Postman Documentation:[https://documenter.getpostman.com/view/32762986/2sAXqp83bn](https://documenter.getpostman.com/view/32762986/2sAXqp83bn)

Use this documentation to see the available API endpoints and how to test them.

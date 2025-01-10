Laravel CRUD Application


This is a CRUD application built with the Laravel framework, offering a simple stock management system with various routes for managing stock items.


Project Overview
This application is a basic example of a Laravel project that includes user authentication, stock management, and CRUD functionality. The application can create, read, update, and delete stock records.

Features
Stock Management: Create, edit, update, and delete stock items.
User Authentication: Register, log in, and manage user profiles.
Dashboard: View the stock items and manage the application settings.
Maintenance Mode: Ability to put the application into maintenance mode.
Queue and Session Management: Handle job queues and sessions efficiently.


Installation
Prerequisites
PHP 8.2 or higher
Composer
MySQL or any compatible database
Node.js and npm (for frontend assets)
Laravel 11.x
Steps to Install
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/app-crud.git
cd app-crud
Install PHP dependencies using Composer:

bash
Copy code
composer install
Copy .env.example to .env and configure your environment:

bash
Copy code
cp .env.example .env
Update .env for your database, mail, and other settings.

Generate the application key:

bash
Copy code
php artisan key:generate
Run migrations to set up the database:

bash
Copy code
php artisan migrate
Install Node.js dependencies for frontend assets:

bash
Copy code
npm install
Run development server:

bash
Copy code
npm run dev
This will start the Vite development server, which will automatically compile frontend assets.

Serve the application:

bash
Copy code
php artisan serve
The application will be accessible at http://localhost:8000.

Environment Configuration
Ensure that the .env file is properly configured. The essential configuration for the database and application environment can be found below:

ini
Copy code
APP_NAME=Laravel
APP_ENV=production
APP_KEY=base64:uLxjQo4bZ48Rtl3uF6Qc6UtpJkWfIA2ni5aTT1RqtS8=
APP_DEBUG=true
APP_URL=http://localhost

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=app-crud
DB_USERNAME=root
DB_PASSWORD=

SESSION_DRIVER=database
SESSION_LIFETIME=120

MAIL_MAILER=log
Available Routes
Here are the primary routes available in this application:

/: The home page, displays a welcome message.
/stock: View all stock items.
/stock/create: Create a new stock item.
/stock/{stock}/edit: Edit an existing stock item.
/stock/{stock}/update: Update the stock item.
/stock/{stock}/destroy: Delete a stock item.
/dashboard: View the stock dashboard.
/profile: Edit and manage your user profile.
Authentication
The app uses Laravel's built-in authentication system. The login and registration pages are provided by the laravel/breeze package. You can register, log in, and edit your profile once you're authenticated.



Development
You can run the application locally by using:

php artisan serve for the backend server.
npm run dev to compile assets with Vite.
To run database migrations or other commands, use the following:

bash
Copy code
php artisan migrate
php artisan db:seed
php artisan key:generate
Testing
The app uses Pest and PHPUnit for testing. You can run tests with the following command:

bash
Copy code
php artisan test
Contributing
Fork the repository
Create a feature branch
Commit your changes
Push your branch
Create a pull request
License
This project is licensed under the MIT License - see the LICENSE file for details.

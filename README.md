Bug Tracker System
Overview
This repository contains a Bug Tracker System built with PHP and Bootstrap. The system allows users to report, track, and manage software bugs efficiently. It includes a user authentication system to ensure that only authorized users can access the bug tracking features.

Features
User Authentication: Secure login functionality for users.
Bug Reporting: Allows users to submit bug reports.
Bug Tracking: Facilitates tracking of reported bugs.
Real-time Collaboration: Multiple users can work on bug resolution simultaneously.
Responsive Design: Built with Bootstrap for a responsive and modern interface.
Technologies Used
PHP
Bootstrap
jQuery
AJAX
Installation
Clone the Repository:

bash
Copy code
git clone https://github.com/yourusername/bug-tracker-system.git
Navigate to the Project Directory:

bash
Copy code
cd bug-tracker-system
Set Up the Database:

Create a database named bug_tracker in your MySQL server.
Import the SQL file located at db/bug_tracker.sql into your database.
Configure the Database Connection:

Update the DBConnection.php file with your database credentials.
php
Copy code
<?php
class DBConnection {
    private $host = 'your_host';
    private $db = 'bug_tracker';
    private $user = 'your_username';
    private $password = 'your_password';
    
    public function connect() {
        $conn = new PDO("mysql:host=$this->host;dbname=$this->db", $this->user, $this->password);
        $conn->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
        return $conn;
    }
}
?>
Start the Server:

Use a local server such as XAMPP or WAMP, or run a PHP built-in server.
bash
Copy code
php -S localhost:8000
Access the Application:

Open your browser and navigate to http://localhost:8000.
Usage
Login:

Enter your username and password to log in.
If you don't have an account, you need to register (registration implementation is assumed to be present).
Report Bugs:

Once logged in, you can report new bugs by filling out the bug report form.
Track Bugs:

View and manage reported bugs from the dashboard.
Contributing
Fork the repository.
Create a new branch (git checkout -b feature-branch).
Commit your changes (git commit -am 'Add new feature').
Push to the branch (git push origin feature-branch).
Create a new Pull Request.
License
This project is licensed under the MIT License. See the LICENSE file for more details.

Acknowledgements
Bootstrap for the responsive design framework.
jQuery and AJAX for the dynamic interactions.

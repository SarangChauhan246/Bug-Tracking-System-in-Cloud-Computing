# Bug Tracker System

## Overview

This repository contains a Bug Tracker System built with PHP and Bootstrap. The system allows users to report, track, and manage software bugs efficiently. It includes a user authentication system to ensure that only authorized users can access the bug tracking features.

## Features

- User Authentication: Secure login functionality for users.
- Bug Reporting: Allows users to submit bug reports.
- Bug Tracking: Facilitates tracking of reported bugs.
- Real-time Collaboration: Multiple users can work on bug resolution simultaneously.
- Responsive Design: Built with Bootstrap for a responsive and modern interface.

## Technologies Used

- PHP
- Bootstrap
- jQuery
- AJAX

## Installation

1. **Clone the Repository:**

    ```bash
    git clone https://github.com/yourusername/bug-tracker-system.git
    ```

2. **Navigate to the Project Directory:**

    ```bash
    cd bug-tracker-system
    ```

3. **Set Up the Database:**

    - Create a database named `bug_tracker` in your MySQL server.
    - Import the SQL file located at `db/bug_tracker.sql` into your database.

4. **Configure the Database Connection:**

    - Update the `DBConnection.php` file with your database credentials.

    ```php
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
    ```

5. **Start the Server:**

    - Use a local server such as XAMPP or WAMP, or run a PHP built-in server.

    ```bash
    php -S localhost:8000
    ```

6. **Access the Application:**

    - Open your browser and navigate to `http://localhost:8000`.

## Usage

1. **Login:**

    - Enter your username and password to log in.
    - If you don't have an account, you need to register (registration implementation is assumed to be present).

2. **Report Bugs:**

    - Once logged in, you can report new bugs by filling out the bug report form.

3. **Track Bugs:**

    - View and manage reported bugs from the dashboard.

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a new Pull Request.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

## Acknowledgements

- Bootstrap for the responsive design framework.
- jQuery and AJAX for the dynamic interactions.

---

Feel free to explore, modify, and contribute to the project. If you encounter any issues or have suggestions for improvements, please open an issue or submit a pull request. Happy coding!

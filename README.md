Project Title

Campus Event Management System
PHP-based web application for managing campus events – allows users to browse, register, and manage events.

Prerequisites

#PHP (version 7.4+ recommended)

#Web server (e.g. Apache or Nginx, with PHP support)

#MySQL or MariaDB (unless using SQLite or another)

#Enable mod_rewrite if using Apache for clean URLs

#Composer (optional, if you plan to manage packages)

⚙️ Dependencies
- PHP >= 7.4
- MySQL / MariaDB
- Apache or Nginx web server
- PHP extensions:
   - mysqli
   - pdo_mysql
   - mbstring
   - session
- (Optional) Composer for dependency management
- (Optional) Bootstrap / jQuery (already included in project)


🚀 How to Download & Run

# 1. Clone the repository
git clone https://github.com/istiakahasan/Campus_event_management_system.git

# 2. Move into project folder
cd Campus_event_management_system

# 3. Copy project to your web server's root directory
# For XAMPP:
#   Place inside: C:/xampp/htdocs/Campus_event_management_system
# For Linux (Apache default):
#   Place inside: /var/www/html/Campus_event_management_system

# 4. Create the database in MySQL
mysql -u root -p
CREATE DATABASE campus_events;

# 5. Import SQL file (if provided)
mysql -u root -p campus_events < database.sql
# (If there is no database.sql file, manually create tables as per config.php)

# 6. Configure database connection
# Open config.php and set your DB credentials
define('DB_HOST', 'localhost');
define('DB_NAME', 'campus_events');
define('DB_USER', 'root');
define('DB_PASS', 'yourpassword');

# 7. Start Apache & MySQL (via XAMPP or systemctl on Linux)
# XAMPP: Start Apache and MySQL from control panel
# Linux:
sudo systemctl start apache2
sudo systemctl start mysql

# 8. Access the app in browser
http://localhost/Campus_event_management_system/

📂 Project Structure

Campus_event_management_system/
│── config.php         # Database and environment configuration
│── index.php          # Main entry point / homepage
│
├── css/               # Stylesheets (UI design, layout, themes)
├── js/                # JavaScript files (interactivity, dynamic features)
├── images/            # Image assets (logos, banners, event posters)
│
├── includes/          # Shared PHP includes (header, footer, navbar, DB connection)
├── templates/         # View templates (HTML/PHP page structures)
│
├── organizer/         # Organizer-specific modules (create/manage events)
├── user/              # User-facing modules (registration, login, profile, event booking)
│
└── public/            # Publicly accessible files (if separated from core PHP logic)


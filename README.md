# ERP_PRoject_odoo

Odoo Project
Welcome to the Odoo Project! This README file provides all the necessary information to get started, install, and contribute to this project.

This Odoo project is designed to create a odoo erp system for the cilent. It aims to provide Project, Sales, Calendar, Dashboards functionality to the user. Odoo is a suite of open-source business apps that cover various business needs, including CRM, eCommerce, accounting, inventory, and more.

Installation
Prerequisites
Before you begin, ensure you have met the following requirements:

Python 3.9+ installed
PostgreSQL installed and running
wkhtmltopdf with headers for PDF reports
Step-by-Step Installation
Clone the Repository:

sh
Copy code
git clone https://github.com/kaushikbigscal/ERP_PRoject_odoo.git
cd your-odoo-project
Create and Activate a Virtual Environment:

sh
Copy code
python3 -m venv venv
source venv/bin/activate
Install Python Dependencies:

sh
Copy code
pip install -r requirements.txt
Install Node.js Packages:

sh
Copy code
npm install
Setup PostgreSQL Database:

sh
Copy code
sudo -u postgres createuser -s odoo_user
sudo -u postgres createdb odoo_db
sudo -u postgres psql
In the PostgreSQL shell:

sql
Copy code
ALTER USER odoo_user WITH PASSWORD 'your_password';
\q
Update Configuration File:

Copy odoo.conf.example to odoo.conf and update the database configuration:

sh
Copy code
cp odoo.conf.example odoo.conf
Update odoo.conf with your database credentials.

Run Odoo:

sh
Copy code
python odoo-bin -c odoo.conf
Configuration
To configure the project, update the odoo.conf file with the necessary settings such as database connection details, server port, addons paths, etc. Example:

ini
Copy code
[options]
   ; This is the password that allows database operations:
   admin_passwd = admin
   db_host = localhost
   db_port = 5432
   db_user = odoo_user
   db_password = your_password
   addons_path = addons
   logfile = /var/log/odoo/odoo.log
Usage
Once the installation is complete, you can access the Odoo instance by navigating to http://localhost:8069 in your web browser. Use the following default credentials to log in:

Email: admin
Password: admin
Testing
To run tests for your Odoo modules, use the following command:

sh
Copy code
python odoo-bin -c odoo.conf --test-enable --init=module_name
Contributing
Contributions are welcome! Follow these steps to contribute:

Fork the Project
Create your Feature Branch (git checkout -b feature/AmazingFeature)
Commit your Changes (git commit -m 'Add some AmazingFeature')
Push to the Branch (git push origin feature/AmazingFeature)
Open a Pull Request
License
This project is licensed under the [Your License]. See the LICENSE file for details.

Contact
Project Link: https://github.com/kaushikbigscal/ERP_PRoject_odoo.git


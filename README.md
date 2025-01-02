# Connect-A-Web-App-with-Aurora

# Amazon Aurora Web App Integration

## Description
This project connects a simple web application to **Amazon Aurora**, a fully managed relational database service by AWS. The app allows users to interact with a **MySQL** database hosted on Amazon Aurora by adding and updating data through the browser. The web app is built using **PHP** and **MySQLi** for database interactions.

With **Amazon Aurora's** scalability and high availability features, this web app demonstrates how to perform CRUD (Create, Read, Update, Delete) operations seamlessly with minimal administrative overhead.

## Features
- Connect a web app to an **Amazon Aurora MySQL** database.
- Perform CRUD operations directly through the browser.
- View real-time updates in the frontend as the backend database updates.
- Fully hosted on **AWS EC2** instance with **Apache**, **PHP**, and **MySQLi**.
- Easy-to-understand integration between the web app and database.

## Project Setup

### Prerequisites
- An **AWS account** to set up Amazon Aurora and EC2 instances.
- **EC2 instance** with **Apache**, **PHP**, and **MySQLi** installed.
- **Amazon Aurora MySQL** instance configured and accessible from the EC2 instance.

### 1. Set Up Amazon Aurora
- Create an **Amazon Aurora MySQL** instance from the **AWS Management Console**.
- Configure security groups to allow traffic from the EC2 instance to Aurora.
- Get the **Aurora endpoint** for connection.

### 2. Launch and Connect EC2 Instance
- Launch an **Amazon EC2 instance** (Amazon Linux 2023 AMI or similar).
- Set up **Apache web server**, **PHP**, and **MySQLi** on the EC2 instance.
- SSH into the EC2 instance with:
  ```bash
  ssh -i YOUR_PEM_FILE_NAME ec2-user@YOUR_EC2_PUBLIC_IPV4_ADDRESS

### 3. Web App Setup
Create a new PHP file (e.g., SamplePage.php) in the EC2 instance's web directory.
Use PHP and MySQLi to interact with the Aurora database:
php
Copy code
<?php 
define('DB_SERVER', 'YOUR_AURORA_ENDPOINT');
define('DB_USERNAME', 'admin');
define('DB_PASSWORD', 'your_password');
define('DB_DATABASE', 'your_database_name');
?>
Create the necessary HTML and PHP code to interact with the database and display data.
### 4. Test the Web App
Test database interactions by updating records in the Aurora database and viewing real-time changes on the web interface.
Verify that CRUD operations (Create, Read, Update, Delete) are working by manually interacting with the database and ensuring that the changes reflect on the frontend.
Directory Structure
bash
Copy code
/amazon-aurora-web-app
│
├── index.php               # Main landing page of the web app
├── SamplePage.php          # Web page that interacts with Aurora
└── config.php              # Database connection configuration
Technologies Used
Amazon Aurora (MySQL)
Amazon EC2 (Web server hosting)
PHP and MySQLi for database interaction
Apache as the web server
Installation
Clone this repository to your local machine:

bash
Copy code
git clone https://github.com/YOUR_USERNAME/amazon-aurora-web-app.git
Configure your Amazon Aurora MySQL instance and update the connection details in config.php.

Set up your EC2 instance, install Apache, PHP, and MySQLi, and copy the web app files to the web directory (e.g., /var/www/html).

Access the web app by navigating to the EC2 instance's public IP address in a browser.

Contributing
Feel free to submit issues or pull requests if you'd like to contribute to improving this project!

License
This project is licensed under the MIT License.

Acknowledgments
Amazon Web Services (AWS) for providing Amazon Aurora and EC2.
PHP and MySQLi for database interaction in the web app.
markdown
Copy code

---

### Key Sections:

- **Description**: Summarizes the project, its features, and the purpose of using Amazon Aurora.
- **Setup Instructions**: Explains how to set up Amazon Aurora, EC2, and the web app to connect to the database.
- **Directory Structure**: Outlines the basic file structure of the web app.
- **Technologies Used**: Lists the main technologies employed in the project.
- **Installation Instructions**: Provides steps to clone the repository, configure the database, and run the web app.
- **Contributing**: Invites others to contribute to the project.
- **License**: Mentions the licensing terms (MIT in this case). 

This README serves as a detailed guide for setting up, running, and contributing to the **Amazon Aurora Web App Integration** project.


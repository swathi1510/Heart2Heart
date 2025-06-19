# Heart2Heart 
Heart2Heart is a web-based Blood Bank & Donor Management System developed using PHP and MySQL. It connects blood donors with hospitals and individuals in need by allowing users to register as donors, search by blood group and location, and request blood. The system includes an admin dashboard to manage users, requests, and donation records. It also features Gmail SMTP integration using PHPMailer to send email notifications. Built with HTML, CSS, Bootstrap, PHP, and MySQL, the project runs on XAMPP. Heart2Heart offers an efficient, user-friendly solution to streamline blood donation processes.

# Features

 Donor registration and management
 Blood request submission by users
 Admin panel for managing donors and requests
 Gmail API integration to:
 Notify individual donors when blood is requested
 Automatically notify admin when a new request is submitted
 Secure login system for admin
 Real-time email alerts
 Search donors by blood group
 Mobile number and email validations

 ## 📂 Project Structure
BBDMS-Project-PHP-V2.4/                                                                                                                                                                                            
├── bbdms/                                                                                                                                                                                                          
│ ├── admin/                                                                                                                                                                                                     
│ │ ├── blood-requests.php                                                                                                                                                                                           
│ │ ├── notify-donor.php                                                                                                                                                                                             
│ │ ├── get-token.php                                                                                                                                                                                               
│ │ ├── send_email.php                                                                                                                                                                                               
│ │ ├── token.json                                                                                                                                                                                                  
│ │ └── credentials.json                                                                                                                                                                                             
│ ├── includes/                                                                                                                                                                                                      
│ │ ├── config.php                                                                                                                                                                                                   
│ │ ├── header.php                                                                                                                                                                                                   
│ │ └── leftbar.php                                                                                                                                                                                                  
│ ├── index.php                                                                                                                                                                                                      
├── css/                                                                                                                                                                                                             
│ └── style.css                                                                                                                                                                                                      
├── js/                                                                                                                                                             
│ └── script.js                                                                                                                                                     
├── vendor/                                                                                                                                                         
│ └── (Composer dependencies including Google API client)                                                                                                          
├── blood-request.php
└── README.md

## 🛠️ Tech Stack

- **Frontend:** HTML, CSS, Bootstrap
- **Backend:** PHP 7+
- **Database:** MySQL
- **Email:** Gmail API (OAuth 2.0)
- **Composer** for dependency management

## 🔐 Gmail API Setup

1. Go to [Google Cloud Console](https://console.cloud.google.com/).
2. Create a new project and enable **Gmail API**.
3. Create **OAuth 2.0 Credentials** and download `credentials.json`.
4. Place the file at:  
   `bbdms/admin/credentials.json`
5. Run `get-token.php` once to generate `token.json`.

## 🔑 Admin Login

- Default credentials can be set manually in the database or via the admin registration feature.

## 💡 How It Works

- When a user submits a blood request, the admin receives an email.
- The admin can then click "Notify Donor" to send an email to the specific donor.
- Emails are sent via the Gmail API using pre-authorized OAuth tokens.

## 🧪 Test the App

1. Start XAMPP and MySQL.
2. Import the database file (`bbdms.sql`) into phpMyAdmin.
3. Place the project folder in `htdocs/`.
4. Open `http://localhost/BBDMS-Project-PHP-V2.4/bbdms/index.php` in your browser.
5. Submit a blood request and check the email flow.

## 🧑‍💻 Contributors

-  Sushma Patil
-  Swathi C.K
-  Tanushree R K

## 📃 License

This project is open-source and available under the [MIT License](LICENSE).

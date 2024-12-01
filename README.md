# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

# osTicket Installation Guide (Windows)

This repository provides a detailed step-by-step guide for installing osTicket on a Windows environment.

---

## Step 1: Install Prerequisites

Ensure your Windows system has the following software installed:

1. **Web Server**: XAMPP (includes Apache, PHP, and MySQL)
   - [Download XAMPP](https://www.apachefriends.org/download.html)
2. **osTicket**: Latest version from the official website.

### Steps:
1. Download and install XAMPP.
2. During the installation, select components: **Apache**, **MySQL**, and **PHP**.
3. Start the XAMPP Control Panel and start **Apache** and **MySQL** services.

![Step 1 Screenshot](images/step1.png)

---

## Step 2: Download osTicket

1. Visit the [osTicket Releases Page](https://github.com/osTicket/osTicket/releases) and download the latest `.zip` file.
2. Extract the osTicket folder into `C:\xampp\htdocs`.

![Step 2 Screenshot](images/step2.png)

---

## Step 3: Configure MySQL Database

1. Open the XAMPP Control Panel and click **Admin** next to MySQL to open phpMyAdmin.
2. Create a new database:
   - Name: `osticket`
3. Create a new user and grant it privileges:
   - Username: `osticketuser`
   - Password: `yourpassword`

### Steps:
- Navigate to **User Accounts** in phpMyAdmin.
- Add a new user with the credentials and grant permissions to the `osticket` database.

![Step 3 Screenshot](images/step3.png)

---

## Step 4: Configure Apache for osTicket

1. Edit the Apache configuration file:
   - File location: `C:\xampp\apache\conf\extra\httpd-vhosts.conf`
2. Add the following VirtualHost configuration:

```apache
<VirtualHost *:80>
    DocumentRoot "C:/xampp/htdocs/osTicket/upload"
    ServerName localhost
    <Directory "C:/xampp/htdocs/osTicket/upload">
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>


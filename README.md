# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

# osTicket Installation Guide (Windows)

This guide provides a simple, step-by-step process to install osTicket on a Windows environment.

---

## Step 1: Install Required Software
1. Install the following prerequisites:
   - **XAMPP**: Download and install from [https://www.apachefriends.org](https://www.apachefriends.org).
     - Enable Apache and MySQL in the XAMPP Control Panel.
   - **osTicket**: Download the latest version from [https://osticket.com/download](https://osticket.com/download).
2. Extract the osTicket files into the `htdocs` folder in your XAMPP installation directory.

---

## Step 2: Configure MySQL Database
1. Open **phpMyAdmin** (accessible via XAMPP Control Panel).
2. Create a new database:
   - **Database Name**: `osticket`.
3. Create a user and assign privileges to the database:
   - Assign **ALL PRIVILEGES** to the new user.

---

## Step 3: Configure osTicket Files
1. Navigate to the `upload` folder where you extracted osTicket.
2. Rename `sample.config.php` to `config.php`.
3. Move the `config.php` file to the `/include` directory.

---

## Step 4: Run the Installer
1. Open your browser and go to `http://localhost/upload/` or your server’s IP address.
2. Follow the installation wizard:
   - Enter the database credentials (from Step 2).
   - Configure your admin account and helpdesk settings.
3. Complete the installation.

---

## Step 5: Finalize Installation
1. Delete the `setup` folder in the osTicket directory to secure your installation.
2. Log in to the Admin Panel at `http://localhost/upload/scp` using the admin credentials created during installation.
3. Configure your helpdesk as needed.



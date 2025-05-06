# MySQL-Installation
## MySQL Server, MySQL Workbench, MySQL Shell
A comprehensive stepwise guide for the installation of MySQL (MySQL Server, MySQL Workbench, and MySQL Shell) on a Windows PC

### 1. Download the MySQL Installer from this link
> https://dev.mysql.com/downloads/windows/installer/8.0.html

### 2. Open the installer
![Screenshot 2025-05-06 150549](https://github.com/user-attachments/assets/1d99c3be-c755-4976-bb93-7b969dc34169)

![Screenshot (4)](https://github.com/user-attachments/assets/1ecaaf46-9b97-4101-8888-05209f100d20)

### 3. Select MySQL Server, MySQL Workbench, and MySQL Shell
Push the selected products to the "Products to be installed" column with the right-pointing arrow in between the "Available Products" column &  the "Products to be installed" column. When they are all in the "Available Products" column, click on "Next", and then click on "Execute", to download them.

![image](https://github.com/user-attachments/assets/04525905-b62c-4f0d-a367-5421c2384e04)
![image](https://github.com/user-attachments/assets/6fedf320-a2f2-4ef4-aef5-98f5a6baccbc)
![image](https://github.com/user-attachments/assets/cd8b5ce6-24ed-4c56-9b45-99fd44eb08e7)

### 4. Click "Next" to install them, "Next" for "Product Configuration", and then "Next" to complete installation.

![Screenshot 2025-05-06 140949](https://github.com/user-attachments/assets/484410f9-526c-43c7-9b83-66dce5a4af24)

![Screenshot 2025-05-06 141506](https://github.com/user-attachments/assets/99aa7e7d-325d-4acf-be01-58e99d7b39ad)

You should see a window like this populated with the products you are installing.

![Screenshot 2025-05-06 141524](https://github.com/user-attachments/assets/0ffc9601-67f6-4996-a474-642ee7b9e3a5)

In the "Installation Complete window, click "Finish" to finish the installation.
![Screenshot 2025-05-06 142037](https://github.com/user-attachments/assets/e9650184-4b3d-4a64-bb2e-866e94c862c3)


## MySQL Server Installation
In the server installation, leave everything as the default and click "Next" through until **"Accounts and Roles"** where you add users and set root user password.

![Screenshot 2025-05-06 141613](https://github.com/user-attachments/assets/3823b41c-5ed7-4360-9655-e35f69ec68b9)

![Screenshot 2025-05-06 141634](https://github.com/user-attachments/assets/93b58351-06f2-49ac-bb47-c23a93426b66)

### Here you set MySQL root password.
This is the user you will use to connect your MySQL Workbench to your MySQL Shell.
You can add a user by clicking on "Add User" in the tab at the bottom.

![Screenshot 2025-05-06 141652](https://github.com/user-attachments/assets/0decf173-7316-42d8-9b04-09049d8cb933)

### Add User
Here you can add any type of user based on their role. But for the purposes of the documentation (since we are not in production) that would not be necessary.
I gave myself the role of DB admin (this gives me access to everything). ***Again, not necessary, Root user has the same" privileges.***

![Screenshot 2025-05-06 141814](https://github.com/user-attachments/assets/6a7f81da-6bc2-496a-aeff-01f29f91b28a)

### Root password is set. User is created.

![Screenshot 2025-05-06 141832](https://github.com/user-attachments/assets/80f75e6a-6ec0-44fd-933c-ba3da9c458e7)

### Leave everything as default and "Next" through.

![Screenshot 2025-05-06 141850](https://github.com/user-attachments/assets/f4c2b93e-4fdd-42bf-b7b1-859ffbb87a9b)

![Screenshot 2025-05-06 141913](https://github.com/user-attachments/assets/a5f0a1bc-d3bc-4ebd-bf09-04fd7566bdd7)

### Here click on "Execute" to apply all changes.

![Screenshot 2025-05-06 141941](https://github.com/user-attachments/assets/43cd8173-2306-435d-92b7-98975309838b)

### Click "Finish" to end MySQL Server Installation.

![Screenshot 2025-05-06 142005](https://github.com/user-attachments/assets/ddf0470d-0f58-41ac-9bea-9f27870fef7b)

## Connect MySQL Shell to MySQL Workbench
To connect your MySQL Shell to Workbench
### 1. Create a new connection in Workbench
In the home tab of your Workbench, click on the "+" next to **MySQL Connections**
NOTE: I am already connected with my root, so I will use my user account (maazinmm) to show you.

![Screenshot 2025-05-06 163305](https://github.com/user-attachments/assets/3e12492a-bbc9-4725-b883-aaf82df85c2c)

### 2. Enter a "Connection name" and a "Username"
The connection name can be anything. However, the username should be "root" in your case.

![Screenshot 2025-05-06 163533](https://github.com/user-attachments/assets/3e282d64-b1bb-4191-833d-617cc7a5b56c)

### 3. Enter the password for your root user.
You can decide to "Save password in vault" so you do not have to enter the password every time.
Click "OK".

![Screenshot 2025-05-06 163549](https://github.com/user-attachments/assets/5a68f488-e71c-45c8-b7d1-70335d4bde6b)

### 4. Test the connection
Click "Test Connection" to confirm if the connection is successful

![Screenshot 2025-05-06 163611](https://github.com/user-attachments/assets/b60a1878-7fb5-48e5-aeac-35b5413f8ce0)

### 5. Connection Successful
You now have your Workbench connected to your local machine (localhost)

![Screenshot 2025-05-06 163629](https://github.com/user-attachments/assets/bf52a486-41fe-491b-82b1-15691979fffc)


## RUN MySQL Shell
To run MySQL Shell, add your MySQL shell "bin" path to your System Variables Path.

Your MySQL shell "bin" should be at this location. Confirm it.
> C:\Program Files\MySQL\MySQL Shell 8.0\bin

When you have confirmed it, copy and paste it into your System Variables Path.

![Screenshot 2025-05-06 143311](https://github.com/user-attachments/assets/d40711eb-581e-4db3-ad49-5af125611ac9)

### Open the shell 
Open a new Powershell window and run ***mysqlsh***. 

If you see an error, try opening Powershell as administrator.

It opens in JavaScript Mode. 

Run \sql to switch to SQL mode 
> \sql

![Screenshot 2025-05-06 145411](https://github.com/user-attachments/assets/1ec12263-11dd-4c4f-8eb3-700fe9dfa68b)

### Connect your MySQL Shell to Workbench
Here we use the connection we created earlier in Workbench

Run ***mysqlsh --uri root@localhost*** to connect to your MySQL Workbench

Use "root" as the username, though I am using my user account.
> mysqlsh --uri root@localhost

![image](https://github.com/user-attachments/assets/ca8e7e32-7344-422a-8fb9-609d33fd740f)

## You are in!

## Interact and get comfortable with the MySQL Shell

![Screenshot 2025-05-06 173529](https://github.com/user-attachments/assets/5dbc9626-ce13-4ce2-98e7-a92880d13607)
> SHOW DATABASES;

View databases in the server.

![Screenshot 2025-05-06 173600](https://github.com/user-attachments/assets/852a7c2d-6e4e-4262-a655-3acc039a8b21)

> USE world;

Work with a particular database.
> SHOW TABLES;

View the tables in the particular database.

![Screenshot 2025-05-06 173616](https://github.com/user-attachments/assets/1219a554-22e8-43ff-bf48-2155007e3d69)

> SELECT * FROM country;

View all the information in the "country" table within the "world" database.

## Create a database
Create a database and initialize it

![image](https://github.com/user-attachments/assets/09b485aa-d321-44aa-855e-1d7d5b49358a)

![image](https://github.com/user-attachments/assets/742d240c-4020-4212-a1f5-6583e829a6bf)

Create a table

![image](https://github.com/user-attachments/assets/47a2f297-88c6-4429-a5df-0d2f5a10bf7f)

Insert data into the table

![image](https://github.com/user-attachments/assets/867cbec8-679a-43e4-b4ca-7228a79daa88)

View the data in the table

### The MySQL Shell Database and Table from MySQL Workbench
![image](https://github.com/user-attachments/assets/78d9f170-2703-41f9-9474-aedb5c677fd6)

# Employee Leave Management System

## Overview

Employee Leave Management System is a web-based application developed using Core PHP, MySQL, Bootstrap 5, JavaScript, and AJAX.

The system allows:

* Employees to apply for leave and track leave history.
* Managers to approve or reject leave requests.
* Administrators to manage users, leave configurations, dashboards, and reports.

---

# Technology Stack

## Backend

* PHP 8.x
* MySQL

## Frontend

* HTML5
* CSS3
* Bootstrap 5
* JavaScript
* jQuery
* AJAX

---

# Setup Instructions

## Step 1: Install XAMPP

Download and install XAMPP.

Start:

* Apache
* MySQL

from the XAMPP Control Panel.

---

## Step 2: Copy Project

Copy the project folder:

leave_management_system

into:

C:\xampp\htdocs\

Project path:

C:\xampp\htdocs\leave_management_system

---

## Step 3: Create Database

Open phpMyAdmin:

http://localhost/phpmyadmin

Create a database named:

leave_management_system

---

## Step 4: Import Database

Import the provided SQL file:

database.sql

into the leave_management_system database.

---

# Database Configuration

File:

config/database.php

Update database settings if required.

```php
<?php

$host = "localhost";
$user = "root";
$pass = "";
$db   = "leave_management_system";

$conn = new mysqli(
    $host,
    $user,
    $pass,
    $db
);

if($conn->connect_error)
{
    die("Connection Failed");
}

?>
```

Default XAMPP configuration:

* Host: localhost
* Username: root
* Password: (blank)

---

# Steps to Run Application

1. Start Apache and MySQL.
2. Open browser.
3. Navigate to:

http://localhost/leave_management_system

4. System redirects to:

http://localhost/leave_management_system/login.php

5. Login using test credentials.

---

# Test User Credentials

## Administrator

Username: admin@gmail.com

Password: admin123

Role: Administrator

---

## Manager

Username: ak@gmail.com

Password: admin123

Role: Manager

---

## Employee

Username: kalaivanik1401@gmail.com

Password: admin123

Role: Employee

Note:
Passwords are stored using PHP password_hash() and verified using password_verify().

---

# Implemented Modules

## Authentication Module

* Login using Username or Email
* Password Hashing
* Session Management
* Role Based Access
* Logout

---

## User Management

Administrator can:

* Create User
* Edit User
* Activate User
* Inactivate User
* Search Users

---

## Leave Configuration

Administrator can:

* Configure Casual Leave
* Configure Sick Leave
* Configure Earned Leave
* Modify Annual Quotas

---

## Employee Module

* Employee Dashboard
* Leave Application
* Leave History
* Leave Editing (Pending Requests Only)

---

## Leave Approval Module

Manager can:

* View Leave Requests
* Approve Leave
* Reject Leave
* Add Remarks
* Update Leave Balances

---

## Reports Module

Administrator can:

Filter by:

* Employee Name
* Department
* Leave Type
* Status
* Date Range

View:

* Employee Information
* Leave Information
* Approval Information

---

# Business Rules Implemented

1. Start date cannot be earlier than current date.
2. End date cannot be earlier than start date.
3. Leave duration is calculated automatically.
4. Leave balance validation implemented.
5. Overlapping leave requests are prevented.
6. Approved leave requests cannot be edited.
7. Leave balance reduces automatically after approval.
8. Manager remarks are mandatory during rejection.

---

# Assumptions Made During Development

1. One manager can approve leave requests for all employees.
2. Leave balances are allocated automatically when a new employee is created.
3. Leave balances are maintained yearly.
4. Administrators can create Manager and Employee accounts.
5. Inactive users cannot log in.
6. Leave requests are initially created with Pending status.
7. Only Pending leave requests can be modified by employees.
8. Approved leave requests immediately reduce available leave balance.
9. Rejected leave requests do not affect leave balance.
10. The application is intended for internal organizational use.

---

# Future Enhancements

* Email Notifications
* Leave Cancellation Workflow
* Multi-Level Approval
* Role Permissions Management
* PDF/Excel Report Export
* Dashboard Analytics
* Holiday Calendar Integration

---

# Developed By

PHP Full Stack Developer Technical Assessment

Employee Leave Management System

kalaivani.k

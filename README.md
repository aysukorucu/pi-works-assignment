# User Management Screen - UI Notes

## Purpose
This is the main screen for managing users. Admins can use this page to see the user list, add new users, or edit the existing ones.

## First Look (When the page loads)
* **Left Side (User Table):** It automatically shows the current users fetched from the database.
* **Hide Disabled User Checkbox:** It's checked by default. This means we don't see the inactive users right away to keep the list clean.
* **Right Side (Form):** This area waits empty and ready for us to add a new user.

## How things work on the screen

### Top Buttons
* **`+ New User` Button:** When you click this, the form on the right clears out. The title becomes "New User". If you had selected a user from the table before, it simply unselects them.
* **`Hide Disabled User` Checkbox:** If checked, users with "Enabled: false" disappear from the table. If you uncheck it, everybody shows up.
* **`Save User` Button:** It saves the info you typed in the form. It should check if the required fields are filled before saving. We should also show a quick success or error message after clicking it, and the table on the left should update automatically.

### The User Table (Left Panel)
* We have 4 columns here: ID, User Name, Email, and Enabled status.
* **Sorting & Filtering:** You can click the column names or little arrows to sort the data. If you click the funnel icon, a search box opens to filter that specific column.
* **Clicking a row:** If you click on any user, the row gets highlighted (maybe light blue). Then, that user's info immediately goes to the form on the right side so you can edit their details.

### The Form (Right Panel)
This is where we type the actual user details.
* **Username:** Text box. Required field.
* **Display Name:** Text box. Required field.
* **Phone:** Text box for numbers.
* **Email:** Text box. Required, and it needs to check for a valid email format (like name@domain.com).
* **User Roles:** A dropdown menu. You can choose Guest, Admin, or SuperAdmin.
* **Enabled:** Just a simple checkbox to show if the user account is active or not.

## Quick Error Checks
* If someone tries to click "Save User" without filling the required fields (like Username or Email), the empty boxes should turn red and warn the user.
* If the email format is wrong, it should give a quick validation error under the email box.

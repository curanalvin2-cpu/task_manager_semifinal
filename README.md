Project Code: WST21-PM-2026-SF

Student Name: Alvin Curan

Course & Year: BSIT - 2nd Year

Section:10

Database Used: SQLite


Features:

Add Task: Create new task entries with a name, optional description, and due date.
View Tasks: Display all stored tasks in an organized dashboard table.
Edit Task: Modify task details such as name, description, and target completion date.
Delete Task: Remove completed or unwanted tasks from the task list.
Update Status: Toggle task status between Pending and Completed.



Tech Stack & Environment:

Framework: Laravel 10 / 11
Frontend: Bootstrap 5 & Blade Templates
Database: SQLite
Environment: GitHub Codespaces

Setup & Running Instructions:

1. Install Dependencies
composer install
2. Environment Configuration
Ensure .env contains your active Codespaces preview domain and SQLite connection:
APP_URL=[https://your-codespace-name-8000.app.github.dev](https://www.google.com/search?q=https://your-codespace-name-8000.app.github.dev&utm_source=gemini)
DB_CONNECTION=sqlite
3. Run Database Migrations
php artisan migrate
4. Clear Caches & Start Application
php artisan config:clear
php artisan serve
# Personal Task Manager

A web-based personal task manager application built with Laravel, SQLite, and Bootstrap 5.

Technical Details
- Framework: Laravel 10 / 11
- Frontend: Bootstrap 5 & Blade Templates
- Database: SQLite
- Environment: GitHub Codespaces


Dashboard Walkthrough

1. Add a New Task
![Add a Task](add-task.png)

How it works:
- Enter a task title inside the Task Name input field (required).
- Provide additional details or instructions in the Description text area.
- Select a target completion date using the Due Date picker.
- Click Save Task to insert the new record into the SQLite database and return a green success alert.


2. Review and Manage Tasks
![Review and Manage Tasks](review-manage-task.png)

How it works:
- The Task List table displays all stored tasks with columns for Task ID (#), Task Name, Description, Status, Due Date, and Action controls.
- The Status column highlights current progress using color-coded badges (e.g., Pending in yellow).
- Each row features an Edit button to modify task information and a Delete button to remove the record.

3. Edit Existing Task
![Edit a Task](edit-task.png)

How it works:
- Clicking the Edit button loads the task details into an editable form.
- You can update the Task Name, Description, Status (switch between Pending and Completed), or Due Date.
- Click Update Task to submit the PUT request and apply changes, or click Cancel to discard edits and return to the dashboard.


4. Delete Confirmation
![Confirm Task Deletion](delete-task.png)

How it works:
- Clicking the Delete button triggers a browser pop-up prompt asking: "Delete this task?"
- Selecting OK executes the DELETE route action to permanently remove the task row from the database.
- Selecting Cancel stops the process and keeps the task unchanged.

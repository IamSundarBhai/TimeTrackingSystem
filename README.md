# Time Tracking System
Software Requirements Specification (SRS)
Project Title: Time Tracking Management Software
Document Version: 1.0
Date: July 24, 2025

1. Introduction
1.1 Purpose
This document outlines the functional and non-functional requirements for the Time Tracking Management Software. The application is designed to manage user logins, track employee timesheets, and maintain organizational structure through departments, designations, and projects.

1.2 Scope
The software will provide secure login access to employees and administrators, enable timesheet management, and allow the administrator to manage employee details and master entries (departments, designations, and projects).

2. Functional Requirements
2.1 Login Module
2.1.1 User Login (Employee Login)
Employees can log in using their unique credentials (username and password).

Forgot password feature (email recovery).

Successful login redirects to the employee dashboard.

Employees can only access their own timesheets.

2.1.2 Admin Login
Admins log in with a separate credential set.

Admin dashboard provides access to all modules: master entries, user management, and all timesheets.

2.2 Master Entries
2.2.1 Departments
Admin can create, edit, delete, and view departments.

Each department has a unique name and optional description.

2.2.2 Designations
Admin can manage designations within the system.

Each designation is linked to one or more departments.

2.2.3 Projects
Admin can add, update, delete, and view projects.

Each project includes:

Project Name

Description

Start and End Dates

Assigned Employees (optional)

2.3 User Details / Employee Details
2.3.1 Add New User / Employee
Admin can add a new employee with the following fields:

Name

Email

Phone

Department

Designation

Assigned Projects (multi-select)

Joining Date

Password (system-generated or custom)

Automatically assigns default permissions.

2.3.2 View All Users / Employees
Admin can view a list of all employees with filters (by department, designation, project).

Each entry includes basic employee information and current project assignments.

2.3.3 Edit / Delete Users / Employees
Admin can edit any employee's information.

Admin can delete employee records (with confirmation and audit log).

2.4 Timesheet Module
2.4.1 Employee Timesheet
Employees can:

Submit daily/weekly working hours.

Select project worked on.

Add comments/notes per entry.

Entries include:

Date

Project

Start Time / End Time or Total Hours

Description of Work

2.4.2 Timesheet Review (Admin)
Admin can:

View all employees’ timesheets.

Filter by employee, date range, and project.

Approve or reject timesheet entries.

Export timesheet data (CSV, PDF).

3. Non-Functional Requirements
3.1 Security
Role-based access control (Admin vs. Employee).

Passwords stored securely (hashed).

Sessions expire after inactivity.

3.2 Usability
Clean, responsive UI.

Accessible from desktop and mobile browsers.

3.3 Performance
Timesheet loading must support large date ranges and filters efficiently.

Login/authentication within 2 seconds.

3.4 Audit Trail
Changes to master entries and user information logged with timestamps and admin details.

4. User Roles and Permissions
Feature	Employee	Admin
Login	✅	✅
View/Edit Own Timesheet	✅	✅
View All Timesheets	❌	✅
Submit Timesheet	✅	❌
Approve/Reject Timesheets	❌	✅
Manage Users (Add/Edit/Delete)	❌	✅
Manage Departments/Projects	❌	✅

5. Future Enhancements (Optional)
Notifications (email reminders for pending timesheets)

Timesheet approval workflows (e.g., team lead → manager → admin)

Attendance tracking integration

Report generation & analytics

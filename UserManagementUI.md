# User Management Screen Specification

## Overview
The User Management screen is used to view, add, edit, and delete user information. This document explains the components and behavior of the screen.

## Components

### 1. Header
- **Title**: Displays "User Management" at the top of the screen.
- **Add User Button**:
  - Label: `Add User`
  - Action: Opens the "Add User" form.

### 2. Search Bar
- **Placeholder**: `Search users by name, email, or role`
- **Functionality**: Filters the user table dynamically as the user types.

### 3. User Table
- **Columns**:
  - **Name**: Displays the full name of the user.
  - **Email**: Displays the email address.
  - **Role**: Displays the role (e.g., Admin, Viewer).
  - **Status**: Displays the current status (Active or Inactive).
  - **Actions**:
    - **Edit**: Opens the "Edit User" form.
    - **Delete**: Prompts for confirmation before deleting the user.
- **Empty Table Behavior**: If no users exist, display `No users found.`

### 4. Footer
- **Pagination**:
  - Buttons: `Previous`, `Next`, and page numbers.
  - **Summary**: Example: `Showing 1–10 of 50 users`

---

## Behaviors

### 1. Initial State
- The table displays the first 10 users sorted alphabetically by name.
- The search bar is empty.

### 2. Adding a User
- Clicking `Add User` opens a form with fields:
  - Name (Required)
  - Email (Required, must be a valid email)
  - Role (Required)
  - Status (Required: Active or Inactive)
- After successful submission:
  - Show a success message: `User added successfully.`
  - Add the user to the table.

### 3. Editing a User
- Clicking the `Edit` button opens a pre-filled form with the user's current details.
- After saving changes:
  - Show a success message: `User updated successfully.`
  - Update the user in the table.

### 4. Deleting a User
- Clicking the `Delete` button shows a confirmation message: `Are you sure you want to delete this user?`
- If confirmed:
  - Remove the user.
  - Show: `User deleted successfully.`
- If canceled, no changes are made.

### 5. Searching Users
- Filters users in real time as the user types in the search bar.
- If no matches are found, display: `No users match your search.`

### 6. Error Handling
- If an action fails, show a message: `An error occurred. Please try again.`
- If the server is unreachable, display: `Unable to fetch user data.`

---

## Validation Rules
- **Name**: Minimum 2 characters, required.
- **Email**: Must be in a valid email format, required.
- **Role**: Must be selected from a dropdown, required.
- **Status**: Active or Inactive, required.

# User Management Screen Specification

A written UI specification for a User Management screen. It covers layout, component behavior, validation, empty states, and error messages for viewing, searching, adding, editing, and deleting users.

This repository is documentation only. There is no implemented UI in the repo. The full spec is in [UserManagementUI.md](UserManagementUI.md).

## Screen contents

- Header with the title "User Management" and an Add User button
- Search bar that filters the table as the user types (name, email, or role)
- Table columns: name, email, role, status (Active or Inactive), and Edit / Delete actions
- Pagination in the footer (Previous, Next, page numbers, and a summary such as "Showing 1-10 of 50 users")
- Empty and no-match states (`No users found.`, `No users match your search.`)

## Behaviors and validation

- Initial load: first 10 users, sorted alphabetically by name
- Add User and Edit User forms: name, email, role, and status, all required
- Name must be at least 2 characters; email must be a valid email; role is chosen from a dropdown; status is Active or Inactive
- Delete asks for confirmation before removing a row
- Success, generic error, and `Unable to fetch user data.` messages are specified

This is a concise product/UX writing sample rather than a software project.

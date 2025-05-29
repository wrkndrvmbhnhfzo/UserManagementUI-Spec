# User Management Screen – UI Specification

## 1. Purpose
This document describes the UI components and interactions for the user management screen. It will be used by developers to implement the related frontend.

## 2. Initial View
- Empty user list
- “Add User” button visible
- Search bar is enabled but initially empty

## 3. UI Components

### 3.1. Search Box
- Placeholder: “Search by name or email”
- Typing triggers a live filter (not case sensitive)

### 3.2. User Table
- Columns:
  - Full Name
  - Email
  - Role
  - Status (Active/Inactive)
  - Actions (Edit/Delete)
- Table has pagination if rows > 10

### 3.3. Buttons
- Add User → Opens user form modal
- Edit → Opens the user info in modal (fields pre-filled)
- Delete → Asks for confirmation, then removes user

## 4. Form Modal
- Fields:
  - Full Name (required)
  - Email (required, must be email format)
  - Role (dropdown: Admin, Editor, Viewer)
  - Status (toggle: Active/Inactive)
- Save button: Validates and sends data
- Cancel button: Closes modal without changes

## 5. Behaviors
- If email already exists, show error
- Show success message after save
- Show alert on delete confirmation

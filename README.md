﻿# Backend-Assignment-EZ
secure_file_sharing/
├── app/
│   ├── models.py       # Database models
│   ├── routes.py       # API endpoints
│   ├── utils.py        # Helper functions (e.g., encryption)
│   ├── __init__.py     # App initialization
├── migrations/         # Database migrations
├── tests/              # Unit and integration tests
│   ├── test_routes.py
│   ├── test_utils.py
├── .env                # Environment variables
├── requirements.txt    # Python dependencies
├── README.md           # Project documentation
├── Dockerfile          # Docker configuration
├── config.py           # App configurations
└── run.py              # Application entry point

# Secure File Sharing System

This project implements a secure file-sharing system between two types of users: **Operations Users** and **Client Users**. The application is built using a Python framework (Flask/Django) and includes functionalities like user authentication, file uploads, downloads, and secure URL-based access.

---

## Features

### **Operations User (Ops User)**
- Login functionality.
- Upload files (`.pptx`, `.docx`, `.xlsx`).

### **Client User**
- Sign up with an encrypted URL in response.
- Email verification with a verification link sent to the registered email.
- Login functionality.
- Download files via a secure encrypted URL.
- List all uploaded files.

---

## API Endpoints

### **Operations User**
1. **Login**: `/api/ops/login`  
   Authenticate the Ops user to gain access to upload files.

2. **Upload File**: `/api/ops/upload`  
   Upload files of type `.pptx`, `.docx`, `.xlsx` only.

---

### **Client User**
1. **Sign Up**: `/api/client/signup`  
   Registers a new client user and returns an encrypted URL.

2. **Email Verify**: `/api/client/verify`  
   Verifies the email address through a verification link.

3. **Login**: `/api/client/login`  
   Authenticate the client user.

4. **Download File**: `/api/client/download/<file_id>`  
   Generates a secure URL to download the file.

5. **List Files**: `/api/client/files`  
   Retrieves a list of all uploaded files.

---

## Setup Instructions

### **Prerequisites**
- Python 3.8 or above
- A virtual environment tool (`venv` or `virtualenv`)
- Database setup (PostgreSQL/MySQL)

### **Install Dependencies**
1. Clone the repository:
   ```bash
   git clone https://github.com/LASHETTY/EZ-Backend-Assignment.git
   cd EZ-Backend-Assignment

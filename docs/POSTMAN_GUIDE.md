# Postman API Testing Guide

## Introduction

This guide explains how to use the Creator's Platform API Postman collection for testing all endpoints.

---

## Setup Instructions

1. Install Postman desktop app
2. Start your backend server:
   npm run dev

---

## Import Collection

1. Open Postman
2. Click on "Import"
3. Select the file: collection.json
4. The collection will appear in your workspace

---

## Import Environment

1. Go to Environments section in Postman
2. Click "Import"
3. Select the file: environment.json
4. Choose "Local Development" as active environment

---

## Environment Variables

### baseURL

* Stores your API base URL
* Example: http://localhost:5000/api

### authToken

* Stores JWT token automatically after login/register
* Used for authenticated routes

### postId

* Stores created post ID automatically
* Used for update/delete requests

---

## Order of Execution

Run requests in this order:

1. Health Check
2. Register User
3. Login User
4. Get All Posts
5. Create Post
6. Update Post
7. Delete Post

---

## Authentication

* Uses Bearer Token
* Token is automatically saved using Postman test scripts
* All protected routes require:
  Authorization: Bearer {{authToken}}

---

## Test Scripts

* Some requests include test scripts
* These scripts check:

  * Status codes (200, 201)
  * Response structure (token exists, post created, etc.)
* Helps ensure API is working correctly

---

## Notes

* Make sure backend server is running before testing
* Ensure correct API endpoints are used
* If requests fail, check token and environment variables

---

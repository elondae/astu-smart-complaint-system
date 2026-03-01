# 🧪 Backend Verification Guide (For Examiners)

This section explains how to independently verify that the backend system is functional, secure, and properly structured.

---

# 1️⃣ Verify Authentication

### Step 1: Test User Registration
- Send a POST request to the registration endpoint.
- Confirm that a new user record appears in the database.
- Verify password is not stored in plain text.

### Step 2: Test Login
- Send login request with valid credentials.
- Confirm that a JWT token is returned.
- Decode token to verify:
  - User ID
  - User role
  - Expiration time

### Step 3: Test Invalid Login
- Attempt login with incorrect credentials.
- Confirm that access is denied.

---

# 2️⃣ Verify Role-Based Access Control

### Student Role
- Attempt to update complaint status.
- Confirm access is denied.
- Attempt to retrieve another user’s complaint.
- Confirm access is restricted.

### Staff/Admin Role
- Attempt status update.
- Confirm update is successful.
- Verify database reflects status change.

---

# 3️⃣ Verify Complaint Submission

- Submit complaint with required fields.
- Confirm:
  - Record appears in database.
  - Default status is set correctly.
- Submit complaint with missing fields.
- Confirm validation error is returned.

---

# 4️⃣ Verify File Upload Handling

- Submit complaint with file attachment.
- Confirm:
  - File appears in Supabase Storage.
  - File metadata is stored in database.
- Attempt unsupported file type.
- Confirm validation prevents unsafe upload.

---

# 5️⃣ Verify Complaint Retrieval

- Authenticated student retrieves complaints.
- Confirm only their own records are returned.
- Admin retrieves complaints.
- Confirm all records are accessible.

---

# 6️⃣ Verify Status Workflow Logic

- Confirm complaints follow lifecycle:
  Open → In Progress → Resolved
- Confirm invalid status transitions are rejected (if implemented).

---

# 7️⃣ Verify Chatbot Functionality

- Send chatbot request.
- Confirm AI-generated response.
- Send follow-up message.
- Confirm conversation context is maintained (memory working).

---

# 8️⃣ Verify Security Controls

- Send request without JWT token.
- Confirm access is denied.
- Send expired token.
- Confirm authentication failure.
- Attempt unauthorized action.
- Confirm role validation blocks request.

---

# 9️⃣ Verify Database Integrity

Using Supabase Dashboard:
- Confirm user roles stored correctly.
- Confirm complaint records contain:
  - User ID
  - Status
  - Timestamp
- Confirm file URLs are correctly stored.

---

# ✅ Evaluation Summary

The backend should demonstrate:

- Secure authentication
- Role enforcement
- Structured workflow
- Proper data validation
- Secure file handling
- Correct lifecycle management
- AI integration functionality

# 🎓 ASTU Smart Complaint & Issue Tracking System

A full-stack digital complaint management system designed for Adama Science and Technology University (ASTU).

This system provides structured issue tracking, role-based access control, secure file uploads, and AI-powered student assistance.

---

# 📌 Project Overview

The ASTU Smart Complaint & Issue Tracking System addresses the lack of transparency and structured workflow in handling campus-related complaints such as:

- Dormitory maintenance issues  
- Laboratory equipment malfunction  
- Internet connectivity problems  
- Classroom facility damage  

The system ensures accountability, tracking, and secure management of complaints.

---

# 🎯 Project Objectives

- Allow students to submit structured complaints
- Enable department staff to manage and update tickets
- Provide administrators with system-wide oversight
- Implement secure authentication and authorization
- Integrate AI chatbot assistance
- Ensure cybersecurity best practices
  

---

# 🏗️ System Architecture

The system is divided into modular workflows:

## 1️⃣ Authentication & Authorization Layer
- User registration
- Secure login
- JWT token generation
- Role-based access control (Student / Staff / Admin)
- Token expiration validation

## 2️⃣ Complaint Submission Workflow
- Complaint creation endpoint
- File upload handling (binary processing)
- Supabase storage integration
- Complaint metadata storage
- Default status: `Open`
- Each student can submit a maximum of 3 complaints per day.
  
## 3️⃣ Complaint Status Management
- Status lifecycle:
  - Open
  - In Progress
  - Resolved
- Role validation before update
- Timestamp logging

## 4️⃣ Complaint Retrieval
- Students can view only their own complaints
- Staff can view assigned complaints
- Admin can view all complaints
- Database filtering enforced

## 5️⃣ AI Chatbot Assistance
- Explains complaint submission process
- Guides students through categories
- Answers common campus-related questions
- Maintains session memory for conversation context

## 6️⃣ Security Layer
- JWT authentication
- Role-based access enforcement
- Secure file upload validation
- Input sanitization
- Structured API access control

---

# 🔐 Cybersecurity Implementation

The system includes:

- Secure authentication using JWT
- Role-based authorization enforcement
- Prevention of unauthorized ticket access
- Secure file upload handling
- API-level protection
- Separation of privileges
- Structured workflow validation

---

# 🛠️ Technologies Used

- n8n (Workflow Automation)
- Supabase (Database & Storage)
- OpenAI (AI Chatbot Integration)
- JWT (Authentication)
- REST API Architecture
- Postman (API Testing)

---

# 📊 Key Features

- Structured ticket lifecycle management
- Secure file/image upload support
- Complaint categorization
- Real-time status tracking
- AI-powered student support
- Modular workflow design
- Scalable architecture

---

# 📱 Mobile Compatibility

The system supports mobile integration with:

- Authentication
- Complaint submission
- Real-time tracking
- In-app notifications
- Profile & history view

---

# 🚀 Deployment

The system is deployed via n8n Cloud and integrates with Supabase backend services.

---

# 📦 Deliverables

- Complete source code repository
- Deployed backend workflows
- Security implementation report
- API documentation
- System architecture explanation

---

# 👨‍💻 Developed For

3rd & 4th Year Final Project  
Adama Science and Technology University

---

# 📈 Future Improvements

- Analytics dashboard visualization
- Push notifications
- Advanced chatbot with database query integration
- Mobile application frontend
- Performance optimization layer

---

# 📄 License

Academic Project – ASTU

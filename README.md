# university-clearance-system-Unipass
this is a digitalised clearance system
UNIVERSITY DIGITAL CLEARANCE 
SYSTEM (Unipass) – PROJECT 
DOCUMENTATION 
1. Introduction 
Project Overview 
The University Digital Clearance System (UDCS) is a web-based platform designed to digitize 
and automate the student clearance process before and after graduation. 
It replaces the traditional paper-based clearance forms that require physical signatures from 
multiple departments (library, faculty, bursar, dean, etc.), which often leads to: 
➢ Delays due to unavailable staff 
➢ Congestion in offices 
➢ Loss of forms 
➢ Forgery of signatures 
➢ Corruption (especially for urgent transcript certification) 
The system ensures a secure, fast, and transparent clearance process. 
Objectives 
➢ Eliminate paper-based clearance forms 
➢ Reduce delays caused by unavailable staff 
➢ Prevent forgery through digital verification 
➢ Minimize corruption via transparent workflows 
➢ Enable students to complete clearance within minutes instead of days 
Target Users 
➢ Students 
➢ Department Officers 
➢ Faculty Dean 
➢ Dean of Students 
➢ Bursar 
➢ Academic Registrar (AR) 
➢ System Administrators 
2. Problem Statement 
Current manual clearance system issues: 
➢ Students move physically across offices 
➢ Officers may be absent or busy 
➢ Forms are signed without proper verification 
➢ Some signatures are forged 
➢ Students pay unofficial fees for faster services 
Thus resulting into ineffenciency,unfaireness in signature delivery and unaccountability 
3. Proposed Solution 
A web-based clearance system that: 
➢ Assigns clearance tasks digitally to each department 
➢ Tracks progress in real time 
➢ Uses secure authentication instead of signatures 
➢ Allows officers to approve/reject clearance online 
➢ Logs all actions to prevent fraud 
4. System Requirements 
Functional Requirements 
4 Student Module 
➢ Students log in using university email 
➢ View clearance status (all departments) 
➢ Submit clearance request 
➢ Receive notifications on approval/rejection 
Department Clearance Module 
Each department (Library, Faculty, Bursar, etc.): 
➢ Views assigned students 
➢ Approves or rejects clearance 
➢ Adds comments (e.g., “Return borrowed book”) 
Clearance Workflow 
Clearance follows this order: 
1. Department(s) 
2. Library 
3. Faculty Dean 
4. Dean of Students 
5. Bursar 
6. Academic Registrar (Final Approval) 
Admin Module 
➢ Manage users and roles 
➢ Monitor clearance progress 
➢ View logs and reports 
➢ Configure departments 
Transcript Request Module 
Students request certified transcripts 
➢ System logs request time 
➢ Officers process requests transparently 
➢ No manual shortcuts allowed 
5. Non-Functional Requirements 
Usability 
➢ Simple dashboard with status indicators (✔ Approved / ✖ Pending) 
➢ Students complete process within 3 minutes 
➢ Minimal navigation (no more than 3 clicks per action) 
Performance 
➢ System loads within 8 seconds 
➢ Dashboard loads within 3 seconds 
➢ Efficient database queries 
Security 
➢ Role-based access control 
➢ Password hashing (bcrypt) 
➢ No manual signatures (digital approval only) 
➢ Unique login credentials for each officer 
➢ Activity logging (who approved what and when) 
Transparency and Anti-Corruption 
➢ Timestamp for every approval 
➢ No bypassing steps 
➢ Audit logs visible to admin 
➢ No hidden approvals 
6. System Architecture 
Technology Stack 
➢ Frontend: HTML, CSS, JavaScript 
➢ Backend: PHP 
➢ Database: MySQL 
➢ Server: WAMP/XAMPP 
Architecture Design 
➢ Client Browser (User Interface) 
➢ PHP Backend (Business Logic) 
➢ MySQL Database (Data Storage) 
7. System Modules 
Authentication Module 
➢ Email-based login 
➢ Role detection (Student, Officer, Admin) 
➢ Secure session handling 
Clearance Management Module 
➢ Tracks clearance status per department 
➢ Displays progress bar 
➢ Prevents skipping steps 
Approval Module 
➢ Officers approve/reject requests 
➢ Add comments 
➢ Digital record stored 
Notification Module 
➢ Alerts for: 
➢ Approval 
➢ Rejection 
➢ Pending action 
Audit and Logging Module 
➢ Logs: 
➢ Login attempts 
➢ Approvals 
➢ Rejections 
➢ Prevents forgery and corruption 
8. Database Design 
Main Tables 
➢ Users (id, email, password, role) 
➢ Departments (id, name) 
➢ Clearance Requests (id, student_id, status) 
➢ ClearanceSteps (id, request_id, department_id, status, comment) 
➢ Logs (id, user_id, action, timestamp) 
➢ TranscriptRequests (id, student_id, status) 
9. User Interface Design 
Student Dashboard 
➢ Clearance progress bar 
➢ Department status list 
➢ Submit request button 
Officer Dashboard 
➢ List of students to clear 
➢ Approve/Reject buttons 
➢ Comment field 
Admin Dashboard 
➢ Total students cleared 
➢ Pending requests 
➢ Logs and reports 
10. System Workflow 
1. Student logs in 
2. Submits clearance request 
3. System assigns departments 
4. Each officer approves/rejects 
5. Status updated in real-time 
6. Final approval by Academic Registrar 
7. Clearance completed 
11. Key Innovations 
No Physical Movement 
➢ Entire process online 
Anti-Forgery System 
➢ No handwritten signatures 
➢ Digital approvals with user accounts 
Anti-Corruption Measures 
➢ Transparent logs 
➢ No hidden processing 
➢ Equal processing order 
Bulk Processing (Class Clearance) 
➢ Admin can upload class list 
➢ Officers can clear multiple students at once 
12. Performance Optimization 
➢ Optimized SQL queries 
➢ Indexed database tables 
➢ Minimal page reload  
➢ Compressed assets 
13. Testing Strategy 
Test Cases 
➢ Student submits request → Visible to all departments 
➢ Officer approves → Status updates correctly 
➢ Unauthorized user → Access denied 
➢ Skipping steps → Not allowed 
14. Future Enhancements 
➢ Mobile App 
➢ SMS notifications 
➢ Integration with student records system 
➢ Online payment for transcripts (mobile money ) 
15. Conclusion 
The Digital Clearance System solves major challenges in the traditional process by: 
➢ Eliminating delays 
➢ Preventing forgery 
➢ Reducing corruption 
➢ Improving efficiency 
It ensures a fast, secure, and transparent clearance process suitable for modern universities. 

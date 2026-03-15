# SmartEdu – Use Case Description

## 1. Actors

| # | Actor | Description |
|---|-------|-------------|
| 1 | Student | A learner who enrolls in courses, consumes learning materials, takes quizzes/exams, and interacts with the AI Tutor and forum. |
| 2 | Instructor | An educator who creates and manages courses, uploads content, builds question banks, grades essays, monitors student progress, and participates in the forum. |
| 3 | Administrator | A platform operator who manages user accounts, reviews instructor profiles, moderates content, handles financial transactions, and monitors system statistics. |
| 4 | AI System | An intelligent subsystem that recommends learning paths, auto-grades quizzes, analyzes learning data, provides AI Tutor responses, and performs exam proctoring. |
| 5 | Payment Gateway | An external payment service integrated for processing student tuition payments. |

## 2. Use Cases

| # | Use Case | Description | Actor(s) |
|---|----------|-------------|----------|
| 1 | Log In | Authenticate and access the system | Student, Instructor, Administrator |
| 2 | Manage Personal Profile | View and update personal information | Student, Instructor |
| 3 | Search Courses | Search and browse available courses | Student |
| 4 | Recommend Learning Path | AI suggests courses based on search history, skills, and career goals | AI System, Student |
| 5 | Register for Course | Enroll in a selected course | Student |
| 6 | Pay Tuition | Process tuition payment through the payment gateway | Student, Payment Gateway |
| 7 | Watch Lecture Videos | View course video content | Student |
| 8 | Download Documents | Download course materials and documents | Student |
| 9 | Take Quiz | Complete multiple-choice quizzes during a course | Student |
| 10 | Interact with AI Tutor | Ask questions and receive basic AI-generated answers | Student, AI System |
| 11 | Participate in Forum | Post and discuss topics with instructors and other students | Student, Instructor |
| 12 | Create and Manage Course | Create courses, upload videos, write documents, and configure course settings | Instructor |
| 13 | Manage Question Bank | Create, edit, and organize test questions | Instructor |
| 14 | Track Student Progress | Monitor individual student learning progress and engagement | Instructor |
| 15 | Auto-Grade Quiz | AI automatically grades multiple-choice quizzes | AI System, Instructor |
| 16 | Analyze Learning Data | AI analyzes skipped videos and frequently wrong answers to provide insights | AI System, Instructor |
| 17 | Grade Essay | Manually evaluate and score student essay submissions | Instructor |
| 18 | Take Final Exam | Complete a proctored final examination | Student |
| 19 | Proctor Exam with AI | AI monitors webcam/microphone for cheating behaviors during exams | AI System |
| 20 | Report Violation | AI records cheating logs, warns the student, and sends violation reports | AI System, Student, Instructor, Administrator |
| 21 | Manage User Accounts | Create, update, disable, or delete user accounts | Administrator |
| 22 | Review Instructor Profile | Approve or reject new instructor applications before they can create courses | Administrator |
| 23 | Moderate Content | Remove copyright-violating courses or inappropriate forum posts | Administrator |
| 24 | Manage Financial Transactions | Review tuition revenue, calculate commissions, and process instructor payouts | Administrator |
| 25 | Track System Statistics | Monitor active students, user engagement, and system stability | Administrator |

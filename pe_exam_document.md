# PROGRMMING EXAM (PE) - SPRING BOOT & THYMELEAF

**Exam Code:** PE_HSF302_SP26_000001  
**Term:** SPRING 2026  
**Subject:** Java Web Application Development (HSF302)  
**Duration:** 90 minutes  

---

### **1. INSTRUCTIONS**

*   **Materials:** No external materials, documents, or internet access allowed (except for official documentation if provided).
*   **Sharing:** Any form of communication or sharing of code between students is strictly prohibited.
*   **Required Tools:** IntelliJ IDEA, SQL Server Management Studio (SSMS), JDK 21+, Maven.
*   **Frameworks & Technologies:**
    *   Spring Boot (3.x)
    *   Thymeleaf Template Engine
    *   Spring Data JPA
    *   SQL Server
    *   N-Layer Architecture (Controller -> Service -> Repository)
*   **Requirements:**
    *   The Repository layer MUST be used for all database access.
    *   Database connection settings MUST be configured in [application.properties](file:///d:/Documents/FPT_Education/SP26/HSF302/project/SE1910_CE192048_RMS/src/main/resources/application.properties).
    *   Hardcoded database connections in Java code are NOT allowed.
*   **Grading Rule:** Any project that fails to compile will receive **0 points**.

---

### **2. PROJECT SETUP**

*   **Project Name:** `SE1910_CE192048_RMS`
*   **Base Package:** `com.ce192048.mvc`
*   **Package Structure:**
    *   `entity`: Contains JPA entities.
    *   `repository`: Contains Spring Data JPA repositories.
    *   `service`: Contains business logic services.
    *   `controller`: Contains Spring MVC controllers.
*   **Database Name:** `HSF302_2026_PE`
*   **Login Default URL:** `http://localhost:8080/`
*   **Initial Account:** Staff (Email: `admin@fpt.edu.vn` / Password: `123`)

---

### **3. DATABASE DESCRIPTION**

The system manages tour information for a travel agency. The primary entity is **Tour**.

#### **3.1 Table: tours**
| Column | Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| tour_id | INT | PK, Identity(1,1) | Unique ID for the tour |
| tour_name | NVARCHAR(200) | Not Null | Name of the tour |
| destination | NVARCHAR(200) | Not Null | Travel destination |
| capacity | INT | Not Null | Maximum number of people |
| duration | INT | Not Null | Number of days |
| start_date | DATE | Not Null | Departure date |
| price | FLOAT | Not Null | Cost of the tour |
| status | NVARCHAR(10) | Not Null | Current status (e.g., Active, Closed) |

---

### **4. EXAM TASKS**

#### **TASK 1: GUI DESIGN (Thymeleaf) - [2.5 Points]**

**1.1 Login Page:**  
*   Create a login form with "Email" and "Password" fields.
*   Center the form on the page.
*   Display an error message if authentication fails.

**1.2 Tour Management Page:**  
*   Display a table containing all tours with columns: ID, Tour Name, Destination, Capacity, Duration, Start Date, Price, and Status.
*   Add an "Add New Tour" button above the table.
*   Include "Edit" and "Delete" links for each row.
*   Provide a search bar to filter tours by name.

#### **TASK 2: DATABASE IMPLEMENTATION - [2.5 Points]**

*   **2.1 JPA Mapping:** Implement the [Tour](file:///d:/Documents/FPT_Education/SP26/HSF302/project/SE1910_CE192048_RMS/src/main/java/com/ce192048/mvc/entities/Tour.java#8-118) entity with appropriate JPA annotations mapping to the SQL Server table described in section 3.
*   **2.2 Initial Data:** Insert at least 3 sample records into the `tours` table using an SQL script or `data.sql`.

#### **TASK 3: CRUD & AUTHENTICATION - [5.0 Points]**

**3.1 Authentication:**  
*   Implement login functionality. If the user enters `admin@fpt.edu.vn` and `123`, redirect to the Tour List page.
*   Store user sessions to prevent unauthorized access to management pages.

**3.2 Tour Listing & Search:**  
*   Fetch and display all tours from the database.
*   Implement search functionality: when a user enters a keyword in the search bar, the list should filter tours whose names contain the keyword.

**3.3 Add New Tour:**  
*   Implement the "Add New Tour" functionality with the following validation rules:
    *   **Tour Name:** Required, max 200 characters.
    *   **Destination:** Required, max 200 characters.
    *   **Capacity:** Must be a positive integer (> 0).
    *   **Price:** Must be a positive number (> 0).
    *   **Start Date:** Must be a valid date.

**3.4 Update Tour:**  
*   Allow users to edit existing tour details. Same validation rules as Task 3.3 apply.

**3.5 Delete Tour:**  
*   Implement the delete functionality. Before deleting, display a confirmation page showing the tour details.

---

### **5. SCORING SUMMARY**

| Category | Task | Points |
| :--- | :--- | :--- |
| **GUI** | Task 1.1 + 1.2 | 2.5 |
| **Database** | Task 2.1 + 2.2 | 2.5 |
| **Business Logic** | Task 3.1 (Auth) | 1.0 |
| | Task 3.2 (List/Search) | 1.5 |
| | Task 3.3 (Add) | 1.0 |
| | Task 3.4 (Update) | 0.5 |
| | Task 3.5 (Delete) | 1.0 |
| **Total** | | **10.0** |

---
**END OF EXAM**

# Phase III: Software Design and Modeling

## 1. Software Architecture
### System Architecture
The Residential Management System (RMS) follows a three-tier architecture, which consists of:

•	Frontend → what users see and interact with 

•	Backend → processes logic and rules 

•	Database → stores all system data 

All parts work together to handle user actions such as login, payments, bookings and notifications.

**Example 1:**
-	Resident enters username and password (Frontend) 
-	Request is sent to Backend with login credentials
-	Backend checks users table in the Database
-	Searches for a record where username matches the input and retrieves user data: id, username, password_hash, role, is_active
-	Backend verifies credentials by comparing entered password with password_hash
-	Backend sends result back to Frontend: If valid → success response with user session or if invalid → error message 
-	Resident is redirected to Resident Dashboard if login is successful
-	Resident session is created → stored and managed by Backend used for authentication in future requests

**Example 2:**
-	Resident selects a handyman service and fills booking form (Frontend) 
-	Request goes to Backend containing booking data
-	Backend checks Database, bookings table and users table in order to verify resident_id, handyman_id, apartment_id and availability
-	Backend inserts a new record into the bookings table in the Database
-	Backend sends confirmation back to Frontend, confirms that booking has been created and returns booking status as “pending” 


### Component Diagram (UML)
![UML Diagram](images/UML%20Diagram.png)

**Left Side Components**

Residential Management System (RMS): Represents the main system that manages all operations such as payments, bookings, announcements and user management.

System Admin of RMS: Controls and supervises the entire system, ensuring proper management of users, buildings and system functionality.


**Middle Components**

Resident: Manages user information and allows residents to view payments, book handyman services, check announcements and receive notifications.

Admin: Handles building management, resident monitoring, payment tracking and announcement posting.

Handyman: Manages maintenance requests by accepting, rejecting, updating and completing tasks.

Apartment: Represents residential units and connects residents with buildings, payments and bookings.

Payment: Handles rent, parking and maintenance payments, including tracking and confirmation.

Booking: Processes handyman service requests and stores booking details such as date, time and status.

Data Access: meaning it reads/writes data from the database.


**Right Side Components**

Security: Ensures authentication, authorization and role-based access control for all users.

Persistence: Handles saving and retrieving data from the database to ensure data consistency.

Database: Stores all system data such as users, payments, apartments, bookings and announcements.

## 2. Detailed Design
### Class Diagram
![Class Diagram](images/Class%20Diagram.png)

### Sequence Diagrams
![Sequence Diagram 1](images/Sequence%20Diagram%201.png)

![Sequence Diagram 1](images/Sequence%20Diagram%202.png)

## 3. Modeling
### Use Case Diagram
![Use Case Diagram](images/Use%20Case%20Diagram.png)

### Activity Diagrams
![Activity Diagram 1](images/Activity%20Diagram%201.png)

![Activity Diagram 2](images/Activity%20Diagram%202.png)


### State Diagrams
![State Diagram 1](images/State%20Diagram%201.png)

![State Diagram 2](images/State%20Diagram%202.png)

![State Diagram 3](images/State%20Diagram%203.png)

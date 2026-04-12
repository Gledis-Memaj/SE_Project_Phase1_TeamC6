# Phase II: User Requirements and Application Specifications
# Residential Management System (RMS)



## 1. Chosen Development Model
We chose the Agile development model because it allows flexibility and continuous improvement throughout the development process. Since the Residential Management System includes multiple features, requirements may evolve during development. This model was selected because:
- While building the system it allows us to work in small parts, not all at once.
- It helps the team to work, share ideas and solve problems.
- When plans or ideas change, they can be easily changed.
- Helps in testing often by checking the work and feedback. 
- Provides faster problem detection and better system quality.

This model is suitable because our team is working in parallel on different modules and Agile helps us integrate and improve them at the same time.



## 2. User Requirements
### a. Stakeholders (WHO is involved)

#### Stakeholder: Administrators
Role: Administrators are responsible for managing and monitoring payments within their assigned buildings. They can view all residents assigned to a building, their payments, verify who has made payments and confirm them once received. Administrators also maintain records of all payments (paid or pending), filter payment data based on criteria such as date, status, building. Additionally, administrators can post announcements for residents and assign a priority level to each announcement (Low, Normal, High, Urgent) to indicate its importance

Interests: Efficient payment tracking, easy filtering of data leading to better organization and simpler management.


#### Stakeholder: Residents	
Role: Residents use the system to track their financial obligations, including rent, parking and maintenance fees. They can view which payments are completed or pending, apply filters based on type and status, as well as mark payments as paid. Residents can also view announcements made by administrators, book handyman services by selecting a preferred date and time and track all booked services along with their status as well as receive real-time notifications about important updates such as payments, bookings and annucments.

Interests: Quick access to information, easy payment tracking, convenient service booking and faster problem-solving.	


#### Stakeholder: Handymen
Role: Handymen are responsible for responding to and managing maintenance requests submitted by residents. They can view incoming requests, accept or reject them based on their availability and update the status of accepted tasks. Once the work is completed, they can mark the request as completed.	

Interests: Clear task management, efficient scheduling, and the ability to manage workload based on availability.


#### Stakeholder: Super Admin
Role: The Super Admin has full control over the system. They are responsible for managing all users and system data, including creating, editing and deleting Admins, Residents and Handymen. The Super Admin also manages buildings and apartments and assigns users to specific apartments.

Interests: Ensuring the system is well-organized, secure and efficiently managed.


#### Stakeholder: Developers
Role: Responsible for designing, developing, testing and maintaining the system. They ensure the system works correctly, is secure and meets user requirements.

Interests: Building a reliable, efficient and user-friendly system, as well as ensuring system performance and security.


### b. User Stories (WHAT they need and WHY)

#### 1. Administrator stories
- As an Administrator, I want to view all residents assigned to my buildings so that I can manage them efficiently. 
- As an Administrator, I want to view and track all payments so that I know who has paid and who has not. 
- As an Administrator, I want to confirm payments once they are received.
- As an Administrator, I want to filter payments by date, status, and building so that I can quickly find specific information. 
- As an Administrator, I want to apply multiple filters at the same time so that I can perform advanced searches. 
- As an Administrator, I want to post announcements with priority levels (Low, Normal, High, Urgent) so that residents understand the importance of each message. 

#### 2. Resident stories
- As a Resident, I want to view all my payments (rent, parking, maintenance) so that I can track what I have paid and what is pending. 
- As a Resident, I want to filter my payments by type and status so that I can quickly find specific payment information. 
- As a Resident, I want to mark payments as paid so that I can notify the administrator. 
- As a Resident, I want to receive notifications about payment due dates so that I do not miss deadlines. 
- As a Resident, I want to receive notifications when my payment is confirmed so that I know it has been approved. 
- As a Resident, I want to view announcements so that I stay informed about building updates. 
- As a Resident, I want to receive notifications about new announcements so that I don’t miss important information. 
- As a Resident, I want to book a handyman by selecting a date and time so that I can schedule maintenance easily. 
- As a Resident, I want to view all my booked services so that I can track their status. 
- As a Resident, I want to receive notifications when my booking is accepted or completed so that I know the progress of my request. 

#### 3. Handyman stories
- As a handyman, I want to see all tasks assigned to me in dashboard so that I can manage my workload efficiently. 
- As a Handyman, I want to accept or reject requests based on my availability so that I can manage my workload efficiently. 
- As a Handyman, I want to update the status of tasks (Accepted, Completed) so that residents can track progress. 
- As a Handyman, I want to mark tasks as completed so that the system reflects finished work. 

#### 4. Super Admin stories
- As a Super Admin, I want to create, edit and delete user accounts (Admins, Residents, Handymen) so that I can manage system access and maintain control over all users. 
- As a Super Admin, I want to create and manage buildings and apartments so that the system structure is well organized. 
- As a Super Admin, I want to assign users to apartments so that each resident is properly linked to their living unit. 



## 3. Functional Requirements (what the system must do)
### a. Description
- The system should allow Super Admin to create, edit and delete user accounts (Admins, Residents, Handymen).
- The system should allow users to log in using their credentials. 
- The system should identify the user role (Super Admin, Admin, Resident, Handyman) and display the appropriate dashboard.
- The system should restrict access based on user roles (role-based access control). 
- The system should allow the Super Admin to create and manage buildings. 
- The system should allow the Super Admin to create and manage apartments. 
- The system should allow the Super Admin to assign residents to apartments. 
- The system should allow administrators to view buildings and apartments assigned to them.
- The system should allow administrators to view and manage residents within their assigned buildings. 
- The system should store and display resident information.
- The system should allow administrators to view all resident payments. 
- The system should allow administrators to confirm payments. 
- The system should store payment records (Paid, Pending). 
- The system should allow residents to view their payments (rent, parking, maintenance). 
- The system should allow residents to mark payments as paid. 
- The system should allow administrators to filter payments by: Date, Status, Building. 
- The system should allow residents to filter payments by: Type (rent, parking, maintenance) and Status 
- The system should allow multiple filters to be applied at the same time.
- The system should allow administrators to create and post announcements. 
- The system should allow administrators to assign priority levels (Low, Normal, High, Urgent) to announcements. 
- The system should allow residents to view announcements. 
- The system should allow residents to book handyman services by selecting date and time.
- The system should allow handymen to view maintenance requests. 
- The system should allow handymen to accept or reject requests based on availability. 
- The system should allow handymen to update request status (Completed). 
- The system should allow residents to view the status of their maintenance requests.
- The system should generate notifications for residents when: A new payment is created; A payment is confirmed; A new announcement is posted; A booking is accepted or completed. 
- The system should display notifications with title, message and timestamp. 
- The system should store notification history for each user. 


### b. Acceptance Criteria (When we know it WORKS correctly)
#### User Login Acceptance Criteria:
- User enters valid username and password 
- System verifies credentials from the database
- User is redirected to the correct dashboard based on role
- System denies access for invalid credentials
- Error message is displayed for incorrect login attempts
- Unauthorized users cannot access restricted pages
- System identifies user role (Super Admin, Admin, Resident, Handyman) 

#### User Management Acceptance Criteria:
- Super Admin can create new users (Admin, Resident, Handyman)
- Super Admin can edit user details
- Super Admin can delete user accounts
- Changes are saved in the database
- Users can log in using created credentials
- Only Super Admin can access user management panel 

#### Building & Apartment Management Acceptance Criteria:
- Super Admin can create and delete buildings
- Super Admin can create apartments inside buildings
- Super Admin can assign users to apartments
- Data is stored correctly in the database 

#### Payment Management (Admin + Resident) Acceptance Criteria:
- Residents can view all their payments
- Payments display correct type, amount, due date, status
- Admin can view all payments per building
- Admin can confirm payments
- Payment status updates correctly in the system
- Payment history is stored and visible 

#### Payment Filtering Acceptance Criteria:
- Admin can filter payments by date
- Admin can filter payments by status
- Admin can filter payments by building
- Admin can apply multiple filters at the same time
- System displays correct filtered results
- Filters can be reset to show all data 

#### Announcements Acceptance Criteria:
- Admin can create announcements
- Admin can assign priority level (Low, Normal, High, Urgent)
- Announcements are stored in the system
- Residents can view announcements
- Announcements are displayed in correct order
- High priority announcements are clearly visible 

#### Maintenance & Handyman System Acceptance Criteria:
- Residents can book handyman services with date and time
- Booking is saved in the system
- Handyman can view all assigned requests
- Handyman can accept or reject requests
- Handyman can update request status after accepted (Completed)
- Residents can view status updates
- Residents receive updates when status changes 

#### Notifications System Acceptance Criteria:
- Resident receives notification when a payment is created
- Resident receives notification when payment is confirmed
- Resident receives notification for new announcements
- Resident receives notification when booking is accepted/rejected or completed
- Notifications display title, message and timestamp
- Notifications are stored and appear in correct order (latest first) 



## 4. Non-Functional Requirements (How well the system should work)
### a. Description
- The system should load quickly and respond to user actions within a few seconds.
- The system should be user-friendly and easy to navigate for all user types.
- The system should be secure and protect user data from unauthorized access.
- The system should ensure role-based access control for all users.
- The system should ensure data accuracy and consistency across all modules.
- The system should provide a responsive design that works on different devices (desktop, tablet, mobile).
- The system should ensure reliable storage of all data including payments, bookings and notifications.
- The system should maintain system stability even under heavy usage.
- The system should ensure notifications are delivered in real time.
- The system should protect passwords using encryption and secure authentication methods.

### b. Acceptance Criteria
#### Speed Acceptance Criteria:
- Pages load in under 2 seconds
- Dashboard actions (viewing payments, announcements, bookings) should respond within 2 seconds.
- Booking process completes in under 5 seconds

#### Usability Acceptance Criteria:
- New users should be able to navigate the system without training within 5 minutes.
- All dashboards should have a clear and consistent layout across all user roles.
- Key features (payments, announcements, bookings) should be accessible within 2 clicks from the dashboard. 

#### Reliability Acceptance Criteria:
- The system should always be available with minimal interruptions.
- The system should not lose data during transactions (payments, bookings, notifications).
- System errors should be handled without crashing the application

#### Security Acceptance Criteria:
- All passwords must be stored using encryption (hashing). 
- Unauthorized users should not be able to access restricted pages. 
- Role-based access control must prevent users from accessing unauthorized features 100% of the time. 

#### Scalability & Performance Under Load Acceptance Criteria:
- The system should support at least 50–100 concurrent users. 
- System response time should remain stable under multiple simultaneous requests

#### Responsiveness Acceptance Criteria:
- The system should display correctly on desktop, tablet and mobile devices.
- All pages should adapt to different screen sizes without breaking layout.

#### Notifications Acceptance Criteria:
- Notifications should appear within 5 seconds after the event. 
- Users should be able to view all notifications instantly without page reload delays. 

 #### Data Integrity Acceptance Criteria:
- All system data must be stored correctly in the database.
- Updates must reflect immediately in all related views. 



## 5. Application Specifications (How the system is built technically)
### a. Architecture
The system follows a three-tier architecture consisting of a frontend (user interface), backend (business logic) and database (data storage).
The frontend provides different dashboards for Super Admin, Admin, Residents and Handymen, allowing users to interact with the system. The frontend sends requests to the backend when users perform actions such as logging in, managing payments, booking maintenance services or viewing announcements.
The backend processes all business logic, including authentication, role-based access control, payment management, notification handling and maintenance request processing. It also ensures that all rules of the system are correctly applied.
The backend communicates with the database to store and retrieve all system data, such as users, buildings, apartments, payments, announcements, bookings and notifications. The database ensures that all information is stored securely and consistently.

### b. Database Model	
The database includes tables such as Users, Buildings, Apartments, Payments, Bookings, Announcements, and Notifications.
Each building contains multiple apartments and each apartment is assigned to a resident. Users have different roles such as Super Admin, Admin, Resident and Handyman. Payments are linked to both residents and apartments and include details such as type, amount, due date and status. Bookings are linked to residents and handymen and store service date, time and status information. Announcements are linked to buildings and include priority levels such as low, normal, high and urgent. Notifications are linked to users and store system updates like payments, bookings and announcements.
The email field and username in the Users table is unique and foreign key constraints ensure that all relationships between users, apartments and buildings remain valid.

### c. Technologies Used (po jua lej juve)
The system is developed using Python for backend development due to its simplicity and flexibility in handling business logic and APIs. The frontend uses HTML, CSS and JavaScript to create a responsive and user-friendly interface for all system users. Bootstrap is used to improve the design and ensure mobile responsiveness.
MySQL is used as the database for efficient and structured data management, including users, payments, bookings and notifications.

### d. User Interface Design
The interface includes a login page and separate dashboards for Super Admin, Admin, Residents and Handymen. Each dashboard is designed according to the user role and provides access to relevant features such as payments, announcements, bookings and maintenance requests.
The design is simple and user-friendly, with clear navigation menus and structured layouts. Key actions such as viewing payments, confirming requests, booking services and posting announcements are accessible through buttons and dashboard sections for easy use.

### e. Security Measures
The system uses user authentication with secure login credentials to ensure that only authorized users can access the platform. Passwords are stored using encryption (hashing) to protect user data. The system implements role-based access control to ensure that each user can only access features allowed for their role. The system also protects data by ensuring secure communication between the frontend and backend and by validating all user inputs to prevent unauthorized actions.

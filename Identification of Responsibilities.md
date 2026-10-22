# Dormitory System : Core features and responsibilities
___

##  - Features : Automated invoicing and payment alerts for Admin 

As an admin, I want the system to automatically generate monthly invoices for residents and send payment reminders, so that rent is billed on schedule and collected on time, without requiring manual effort each month.

### Feature breakdown
1. Admin has to authenticate on the application
2. Admin sets the invoice generation date in the system
3. Admin sets the payment due window
4. System schedules invoice generation
5. When the configured invoice date starts:

    a. System queries all residents that were active during the previous month

    b. Calculates payment information for every resident

    c. Generates a downloadable PDF invoice

    d. Sends emails with invoice and payment reminder to the residents

### Responsibilities

#### Configuring invoice generation responsibilities 
- Validate input parameters
- Persist configuration settings in the database

#### Schedule invoice generation responsibilities
- Register/Update background schedule job
- Monitor the availability and health of the scheduling worker

#### Generating payment information responsibilities
- Calculate total invoice amount per resident
- Determine payment due date based on the configured due window
- Store invoice records with status Unpaid
- Generate payment link

#### Generate a downloadable PDF invoice
- Render standardized PDF document from invoice data

#### Send emails with invoice and payment reminder
- Compose personalized invoice notification message
- Dispatch email with PDF attachment via mail provider
- Handle email delivery retries on failure

___

##  - Features : Laundry machine booking for Student

As a student, they can check machine availability from their room to avoid waiting in the laundry area.

### **Feature breakdown**

1. Student has to authenticate on the application
2. System checks for available machines
3. If there are available machines : 

   3.1. System shows them to the student

   3.2. Student picks the desired machine

   3.3. If student has money on the account :
   1. System proceeds with the payment
   2. Student can start the machine
   3. After cycle and unload, machine locks again

   3.4. If student doesn’t have money on the account : 

   1. System shows message about insufficient balance
   2. System redirects student towards the payment system
   3. Once student has enough money, goes back to part 3.3.
4. System says no washing machine are available, eta on the closest one 

### Responsibilities

#### Assign an available machine to the user

- Find an available machine
- Unlock its doors

#### User Management 

- Manage credit card transactions and the virtual balance
- Allow a user to book a machine for a specific time
- Display the history of completed cycles and payment receipts

#### Maintenance System

- Allow the user to report a broken machine
- Send alerts to the manager

#### Tracking System

- Show which machines are free, in use, or out of order
- Display the remaining time for the current machine
- Send an alert When the cycle is finished

___

## - Features : Registering a student for Administrator

As an administrator, I want to register a student in the system and verify their application, so that the student can be officially registered and receive their contract.

### Feature breakdown

1. Administrator has to authenticate on the application
2. Administrator enters the student registration page
3. Administrator collects and fills in credentials about the student
4. System checks whether the student ID already exists in the student database
5. If the student ID already exists:

   a. System fails the operation and informs the administrator

   b. System redirects the administrator back to the main page

6. If the student ID does not exist, system displays the student registration form
7. System checks the documents sent by the student during the application process
8. If documents are missing:

   a. System sends an email request for the missing documents

   b. System saves the current state of the application in the platform

9. If all required documents have been sent:

   a. System validates the application

   b. System sends the contract to the student for signature

### Responsibilities

#### Administrator access responsibilities

- Authenticate and authorize the administrator
- Display the student registration interface

#### Student identification responsibilities

- Collect and validate the student's registration information
- Check whether the student ID already exists
- Reject duplicate registrations and inform the administrator

#### Document verification responsibilities

- Retrieve and check the student's application documents
- Identify missing required documents
- Send an email requesting missing documents

#### Application processing responsibilities

- Save the current state of the application
- Validate the complete application and send the contract for signature

___








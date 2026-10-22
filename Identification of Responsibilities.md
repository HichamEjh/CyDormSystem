# **Dormitory System** : Core features and responsibilities

##  - Features : Automated invoicing and payment alerts for Admin 

As an admin, I want the system to automatically generate monthly invoices for residents and send payment reminders, so that rent is billed on schedule and collected on time, without requiring manual effort each month.

### **Feature breakdown**
1. Admin has to authenticate on the application
2. Admin sets the invoice generation date in the system
3. Admin sets the payment due window
4. System schedules invoice generation
5. When the configured invoice date starts:

    a. System queries all residents that were active during the previous month

    b. Calculates payment information for every resident

    c. Generates a downloadable PDF invoice

    d. Sends emails with invoice and payment reminder to the residents

### **Responsibilities**

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









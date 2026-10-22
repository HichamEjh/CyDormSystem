# **Dormitory System**
## Core features and responsibilities

## <u> - Features : Automated invoicing and payment alerts for Admin </u>

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

#### <u>Configuring invoice generation responsibilities </u>
- Validate input parameters
- Persist configuration settings in the database

#### <u>Schedule invoice generation responsibilities</u>
- Register/Update background schedule job
- Monitor the availability and health of the scheduling worker

#### <u>Generating payment information responsibilities</u>
- Calculate total invoice amount per resident
- Determine payment due date based on the configured due window
- Store invoice records with status Unpaid
- Generate payment link

#### <u>Generate a downloadable PDF invoice</u>
- Render standardized PDF document from invoice data

#### <u>Send emails with invoice and payment reminder</u>
- Compose personalized invoice notification message
- Dispatch email with PDF attachment via mail provider
- Handle email delivery retries on failure









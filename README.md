# Building-first-RPA-process

1. This workflow retrieves all unread emails, from the Outlook account in uset, that have 'Course Invoices' in the subject line. 
2. Emails retrieved are saved under the 'CourseEmails' list MailMessage type of variable. 
3. Afterwards, attachments for each mail message retrieved are saved in a new  project folder. titled "Invoices". 
4. It then identifies and copies the client code from each attachment and stores it under the 'ClientCode' variable. 
5. Next, using the Edge browser, it access the "https://acme-test.uipath.com/first-automation" webpage, clicks 'Part 2' and types in the client code to get the discount value. 
6. The discount value is stored under the 'DiscountValue' variable (this operation is repeated for all stored client codes).
7. If the discount value contains the "$" character, the value will be typed in the 'Invoice' sheet, in the 'E18' cell. Otherwise, the value "$0" will be added.
8. Next, the "RPA Dev, DeGreenguy- abegundeosamuel@gmail.com" signature is added in each of the invoice sheets.
9. Finally, write the text to be used to prepare an Outlook draft email containing the updated invoices (the draft email can be found inside the 'Drafts' folder of the Outlook account in use).

#### Date: 09/03/2017

#### Description: This document explains the code flow of Contact in new create job invitees.

#### Step 1:

Function **controlNewCreateFlow** will be called first from index.php to controller which takes the inputs from the user, when user enters data in contact in new create job invitees. click on save this function will call and using the wsdl it will create the new contact.

- Inputs given by user to create a contact is first name, last name, contact type,contact number, email type, email id.
- Function **createNewContactListInputVO** takes the inputs array and send to data file and prepares the list object. It prepares the input to create new contact.
- In action, first we will call user id and append to input array by function **getUserID**.
- Function **createNewContactListInputVO** from ContactsData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepares the query and required input to create new contact.
- The result will be returned to controller.

#### Step 2:

- Function **createNewContact** takes the input value object and passes to the wsdl call to create a new Contact.
- In action, first ws client connection will be set by function **setWSDLHandle**.
- Function **createNewContact** from ContactsWS.php is used create a new contact or edit contact.
- Creating parameters for wsdl using object and passing the parameters to ws call **set_contacts_acc**.

#### Step 3:

The result will be returned to controller, header loaction will be redirected to detail view based on the contact id.

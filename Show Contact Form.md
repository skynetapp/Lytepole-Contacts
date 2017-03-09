#### Date: 09/03/2017

#### Description: This document explains the code flow of Contacts.

#### Step 1:

Function **showNewContactForm** will be called first from index.php to controller. when user clicks on add new contact button in contacts it calls this function and this function redirect to the create form of new contact.

- Function **showContactCreateForm** will be called in controller from action which gives the contact create form.
- In action, we will call the view page to show the contact create form by calling function **showNewContactForm** from ContactsView.php.
- The display tpl page will be **CreateNewContactForm.tpl** which is in views folder.

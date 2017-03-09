#### Step 1:

Function **controlContactEditFlow** will be called first which takes the inputs from the user, when user clicks on edit contact it will call this function. From this function we call the wsdl to edit contact.

- Function **createContactListInputVO** will create the value objects from controller to action.
- In action, user id will be set by function **getUserID**.
- Function **createContactListInputVO** will be called in action from ContactsData.php which gets the values from input array and sets the values for list value object to pass for WSDL call. It will prepare the query and required input to create contact.
- The list value object array result will be returned to controller.

#### Step 2:

- Function **getContactsList** is used to call the wsdl call for getting the contacts list from controller to action.
- In action, first ws client connection will be set by function **setWSDLHandle**.
- Function **getListArray** in ContactsWS.php which is used send data to wsdl for getting the contacts list array using the ws call **get_entry_list_con**.
- The contacts list array result will be returned to controller.

#### Step 3:

- Function **createContactListDataObjectArr** in controller will create the object array for list data.
- In action, Function **createContactListDataObject** will be called from ContactsData.php which gets the values from input array and sets the values for list data object.
- The contact data object array will be returned to controller.

#### Step 4:

- Function **showContactEditView** which takes the input data object and gives to the contacts Detail view.
- The list data object array will be user id, first name, last name, email, home phone, mobile, work phone.
- In action, function **showContactEditView** will be called which displays the tpl page.
- The display tpl page will be **ContactsEditForm.tpl** in views folder.

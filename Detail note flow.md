#### Step 1:

Function **controlDetailNoteFlow** takes the inputs from the user, when user clicks on note detail view it will call this function. From this function we call the wsdl to get the note detail view and displays.

- Function **createContactNotesListInputVO** will create the value objects from controller to action.
- In action, user id will be called and append to input array by function **getUserID**.
- Function **createContactListInputVO** will be called in action from ContactsData.php which gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to create contact note.
- The parameters input data array are user id,Module name and Action name,query,sub action, offset.
- The list value object array result will be returned to controller.

#### Step 2:

- Function **getContactsNotesList** is used to take the input value object and passes to the wsdl call to notes list from controller to action.
- In action, first ws client connection will be set by function **setWSDLHandle**.
- Function **getContactNotesListArray** in ContactsWS.php which is used to send data to wsdl for getting the notes list array using the ws call **get_entry_list**.
- The parameters are session id, module name, query, orderby, offset, max result, deleted.
- The notes list array result will be returned to controller.

#### Step 3:

- Function **createContactNotesListDataObjectArr** in controller will takes the inputs array and send to data file and prepares the list object.
- In action, Function **createContactNotesListDataObject** will be called from ContactsData.php which gets the values from input array and sets the values for list data object to pass to create note data.
- The parameters are name, id, date, createdby, description, status, type, parentid, duration, startdate
- The contact data object array will be returned to controller.

#### Step 4:

- Function **showContactNotesDetailView** which takes the input data object and gives to the notes detail view.
- The list data object array will be user id,name, description,contact id.
- In action, function **showContactNotesDetailView** from ContactsView.php will be called which displays the tpl page.
- The display tpl page will be **NotesDetailView.tpl** in views folder.

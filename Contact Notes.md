#### Date: 09/03/2017

#### Description: This document explains the code flow of Contact Notes.

#### Step 1:

Function **controlContactNotes** will be called first from index.php to controller which takes the inputs from the user, when user clicks on contacts notes or logevents in contact detail it will call this function. From this function we call the wsdl to get the notes or logevent of related contact.

- Function **createContactNotesListInputVO** takes the inputs array and send to data file and prepares the list object to get the note list. Its pepare the input to note wsdl.
- In action, user id will be called and append to input array by function **getUserID**.
- Function **createContactNotesListInputVO** from ContactsData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to create contact note.
- Returns the result as contact note list value object array to controller.

#### Step 2:

- Function **getContactsNotesList** in controller takes the input value object and passes to the wsdl call to notes list.
- In action, first ws client connection will be set by function **setWSDLHandle**.
- Function **getContactNotesListArray** in ContactsWS.php which is used send data to wsdl for getting the notes list array using the ws call **get_entry_list**.

#### Step 3:

- Function **createContactNotesListDataObjectArr** in controller, takes the inputs array and send to data file and prepares the list object.
- In action, Function **createContactNotesListDataObject** gets the values from input array and sets the values for list data object to pass and create contacts note data.
- The contact note data object array will be returned to controller.

#### Step 4:

- Function **showContactNotesList** which takes the input data object and gives to the note List.
- The list data object array will be user id, name, description, contact id.
- In action, function **showContactNotesListView** from ContactsView.php will be called which displays the tpl page.
- The display tpl page will be **ContactsDetailView.tpl** in views folder.

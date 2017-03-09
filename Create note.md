#### Step 1:

Function **controlCreateNoteFlow** will be called first from index.php to controller which takes the inputs from the user. when user enters data in note new create form and click on save, this function will call and using the wsdl it will create the new note.

- function **createNewContactNotesListInputVO** takes the inputs array and send to data file and prepares the list object.
- In action, user id will be called and append to input array by function **getUserID**.
- Function **createNewContactNotesListInputVO** from ContactsData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to create contact note.
- Returns the result as contact note list value object array to controller.

#### Step 2:

- Function **createNewNote** takes the input value object and passes to the wsdl call to create a new note.
- In action, first ws client connection will be set by function **setWSDLHandle**.
- Function **createNewNote** in ContactsWS.php which is used to create a new note by calling the ws call **set_entry** and passing the created parameters to wsdl object .
- The result will return the note id.

#### Step 3:

- Header location will be redirected to contact note view.

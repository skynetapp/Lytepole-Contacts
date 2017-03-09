#### Step 1:

Function **controlCreateLogevent** will be called first from index.php to controller which takes the inputs from the user. when user enters data in logevent new create form and click on save this function will call and using the wsdl it will create the new logevent.

- function **createNewContactLogeventListInputVO** takes the inputs array and send to data file and prepares the list object. It pepares the input to create logevent wsdl.
- In action, user id will be called and append to input array by function **getUserID**.
- Function **createNewContactLogeventListInputVO** from ContactsData.php gets the values from input array and sets the values for list value object to pass for WSDL call. It prepare the query and required input to create contact logevent.
- Returns the result as contact logevent list value object array to controller.

#### Step 2:

- Function **createLogevent** takes the input value object and passes to the wsdl call to create a new logevent.
- In action, first ws client connection will be set by function **setWSDLHandle**.
- Function **createNewNote** in ContactsWS.php which is used to create a new logevnt by calling the ws call **set_entry** and passing the created parameters to wsdl object .
- The parameters are name,status, direction, assigned_user_id, date_start, duration_hours, duration_minutes, parent_id, parent_type, deleted, description
- The result will return the logevent id.

#### Step 3:

- Header location will be redirected to contact logevnt.


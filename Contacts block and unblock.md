#### Step 1:

Function **controlContactBlock** will be called first in index.php to controller which takes the inputs from the user, when user clicks on block contact it will call this function. From this function we call the wsdl to block the selected contact.

- Function **contactBlock** will take the input value object and passes to the wsdl call to block contact.
- In action, first ws client connection will be set by function **setWSDLHandle**.
- Function **contactBlock** will be called in ContactsWS.php and will create the parameters by ws call **set_entries**.

#### Step 2:
- If the action is **Block**, the value will be 1 and the contact will be blocked.
- The return result will get the contact record id and passed to controller which redirects to contact detail view. 

#### Step 3:
- If the action is **Unblock**, the value will be 0 and the contact will be blocked.
- The return result will get the contact record id and passed to controller which redirects to contact detail view. 

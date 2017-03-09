#### Step 1:

Function **getChatContactsDirect** will be called first from index.php to controller which gets the contacts directly from DB without using the WS call.

- Function **getContactsDirect** takes the input data and gives the contacts list directly from DB without using WSDL.
- In action, user id will be called and append to input array by function **getUserID**.
- Calling DB call to get contact list from Meetings/DBConnection.php which will get the data using function **getContactsDirect**.
- Based on the sql query the array list of contacts will be returned.


#### Date: 08/03/2017

#### Description: This document explains the code flow of Contacts.

#### The Folder Structure is as follows:

 Root Directory | Sub Directory 
------------ | -------------
index.php | 
Global | LytepoleWSConnection
Lib | Smarty,nusoap
Modules | Contacts
Views | ContactsViewForm, ContactsViewPaginationForm, ContactsDetailView, ContactsDetailViewblank, ContactNewAdd, ContactsEditForm, AccountLocationsViewForm, AccountEmployetypeViewForm, AccountCompanyViewForm, CreateNewContactForm, NotificationsViewForm, ContactsNotesViewForm, NotesCreateForm, LogeventCreateForm, NotesDetailView, ContactBulkUpload, ContactBulkUploadInvalid, ContactBulkUploadProcess

#### Step 1:

Function **controlContactsListFlow** will be called first when we click on left menu after login.

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

- If **$post_data['ajaxcall'] == 'yes'**, funtion **showContactPaginationList** which takes the input data object and gives to the contacts pagination list view.
- In action, function **showContactListPaginationView** will be called from ContactsView.php which displays the tpl view page.
- The tpl page will be in views -> ContactsViewPaginationForm.tpl

#### Step 5:

- If **$post_data['ajaxcall'] != 'yes'**, function **showContactList** will takes the input data object and gives to the contacts list view.
- In action, function **showContactListView** will be called from ContactsView.php which displays the tpl view page.
- The display tpl page will be in views -> ContactsViewForm.tpl




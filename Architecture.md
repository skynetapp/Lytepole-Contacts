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

#### Architecture

- After login in lytepole, we can see Contacts in the side menu. when user clicks on contacts, function **controlContactsListFlow** will take the input from user and from this function we call wsdl to get and display the contact list.
- If it is ajaxcall, contacts list will be shown in pagination by function **showContactPaginationList** else function **showContactList** will be called to show contact list.
- When user clicks on add new contact button in contacts it calls the function **showNewContactForm** which redirects to contact create form.
- When user clicks on any of the contact name or right arrow, function **controlContactDetailViewFlow** will be called which displays the detail view of the contact.
- On the top right we can edit the contact which calls the function **controlContactEditFlow** and shows the edit form.
- When we update the details of the contact it will redirect to the detail view page.
- When user clicks on note or logevents in contact detail, it will call the function **controlContactNotes** which will get the logevent or notes of that related contact.
- When we click on Add log event , function **showCrateLogeventForm** will be called which shows the log event create form. 
- Function **controlCreateLogevent** will be called which will create the log event and redirect to logevent page. 
- When we click on Add Note , function **showNewNoteForm** will be called which shows the note form.
- Function **controlCreateNoteFlow** will be called which creates the note.
- Function **controlDetailNoteFlow** will be called which takes to the detail note view.
- When user clicks on the Block Contact in detail view, function **controlContactBlock** will be called which calls the wsdl as **action == Block** and blocks the selected contact.
- If we want to UnBlock that contact, function **controlContactBlock** will be called which calls the wsdl as **action == UnBlock** and unblocks the selected contact.

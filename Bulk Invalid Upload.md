#### Date: 09/03/2017

#### Description: This document explains the code flow of Bulk Upload invalid form using csv file.

#### Step 1:

Function **controlBulkInvalidUpload** will be called first from index.php to controller. when user adds not csv file or empty and click on submit button in bulk upload.

- In action, function **showcontrolBulkUploadInvalidForm**, takes the input data object and gives to the bulk upload invalid form.
- Function **showcontrolBulkUploadInvalidForm** from ContactsView.php will display the tpl page.
- The display tpl page will be **ContactBulkUploadInvalid.tpl** in views folder.




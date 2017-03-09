#### Date: 09/03/2017

#### Description: This document explains the code flow of Bulk Upload Contacts form.

#### Step 1:

Function **controlBulkUpload** will be called first from index.php to controller. when user clicks on bulk upload button in left side bar its call this function and this function redirect to the upload contacts form.

- Function **showcontrolBulkUploadForm** will be called in action from controller which takes the input data object and gives to the bulk upload loading form.
- In action, function **showcontrolBulkUploadForm** will be called from ContactsView.php which displays the tpl form page.
- The display tpl page will be **ContactBulkUpload.tpl** in views folder.

#### Date: 09/03/2017

#### Description: This document explains the code flow of Bulk upload Processing of Contacts using csv file.


#### Step 1:

Function **controlBulkUploadProcessing** will be called first from index.php to controller which is used for uloading csv file for bulk uploading of contacts.

- First it checks whether the file is csv or not with function **readCSV**.
- Next it checks the csv format header. If it is not correct header location will be redirected to ContactInvalidList with message **>Invalid template - please use the template and upload the file as a CSV**.
- Next, It checks the count of contacts in uploaded csv, if less than 100 - header location will be redirected to ContactInvalidList **Contats more than 100 - please use the template and upload the file as a CSV minimum of 100 contacts**.
- Next it checks the empty record in the uploaded csv file for first name, last name, contact, email.

#### Step 2:

- In action, function **showcontrolBulkProcessForm** takes the input data object and gives to the bulk upload contacts form.
- Function **showcontrolBulkProcessForm** in ContactsView.php which displays the tpl page.
- The display tpl page will be **ContactBulkUploadProcess.tpl** which is in views folder.

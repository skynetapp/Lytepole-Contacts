#### Step 1:

Function **showCrateLogeventForm** will be called first from index.php to controller. when user clicks on log event in contact deatil view its call this function and this function redirect to the log event list related to that contact

- Function **showCrateLogeventForm**, takes the input data object and gives to the logevent create form.
- In action, function **showCrateLogeventForm** will be called from ContactsView.php which displays the tpl page.
- The display page will be **LogeventCreateForm.tpl** in views folder.

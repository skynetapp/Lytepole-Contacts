#### Step 1:

Function **showNewNoteForm** will be called first from index.php to controller. when user clicks on notes in contact deatil view its call this function and this
*function redirect to the note list related to that contact.

- Function **showNewNoteForm** takes the input data object and gives to the note create form.
- In action, Function **showNewNoteForm** will be called from ContactsView.php which displays the tpl page.
- The display tpl page will be **NotesCreateForm.tpl** in views folder.


# Evernote assistant
This app helps working with evernote notebook.  
You can see all your notebooks, clone notes and get dump of choosen notebook.

## How to install
clone repo, you should have python of 2 generation (created with version 2.7), create virtualenv and load dependencies:
```
git clone https://github.com/ilyashirko/evernote_review
cd evernote_review
virtualenv -p /path/to/python2.7 env2.7
source env2.7/bin/activate
pip install -r requirements.txt
```
Create `.env` file:
```
EVERNOTE_CONSUMER_KEY=
EVERNOTE_CONSUMER_SECRET=
EVERNOTE_PERSONAL_TOKEN=
JOURNAL_TEMPLATE_NOTE_GUID=
JOURNAL_NOTEBOOK_GUID=
INBOX_NOTEBOOK_GUID=
SANDBOX=
```
`EVERNOTE_CONSUMER_KEY` & `EVERNOTE_CONSUMER_SECRET` you can get [here](https://dev.evernote.com/#apikey)  
`EVERNOTE_PERSONAL_TOKEN` get [here](https://sandbox.evernote.com/api/DeveloperToken.action)  
`JOURNAL_NOTEBOOK_GUID` - any notebook  
`JOURNAL_TEMPLATE_NOTE_GUID` - default note from `JOURNAL_NOTEBOOK_GUID`  
`INBOX_NOTEBOOK_GUID` - default notebook (you can set up it in the notebook settings)  
`SANDBOX` - True or False  

## list_notebooks.py
returns list of user notebooks in the format:
```
{first_notebook_uuid} - {first_notebook_title}
{second_notebook_uuid} - {second_notebook_title}
...
{last_notebook_uuid} - {last_notebook_title}
```
## add_note2journal.py
Take title of the default note, adding date and day of the week and create new note in format:
```
{default note title} YYYY-MM-DD friday
```

## dump_inbox.py
return all notes of choosen notebook

the application was created by [DEVMAN](https://dvmn.org) team for educational purposes

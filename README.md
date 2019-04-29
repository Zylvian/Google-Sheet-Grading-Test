# py_googlesheets_grading

## Installation
Install:

`$ pip install py_googlesheets_grading`
This will also install gsheets and its dependencies, notably httplib2 and oauth2client, as required dependencies.

## Quickstart
Log into the Google Developers Console with the Google account whose spreadsheets you want to access. Create (or select) a project and enable the Drive API and Sheets API (under Google Apps APIs).

Go to the **Credentials** for your project and create **New credentials > OAuth client ID >** of type **Other**. In the list of your OAuth 2.0 client IDs click Download JSON for the Client ID you just created. Save the file as `client_secret.json` in your home directory (user directory).

Upon initial exectuion, follow the prompted terminal instructions.


Then run this in a Python script or terminal:

```
from py_googlesheets_grading import Grader

Grader().grade_students()

```

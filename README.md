# py_googlesheets_grading

## Installation
Install:

`$ pip install py_googlesheets_grading`
This will also install gsheets and its dependencies, notably gsheets (httplib2 and oauth2client), as required dependencies.

## Quickstart

To run this script, it needs access to your Google Sheets. To get this, it needs a `client_secret.json` file. Follow the tutorial below:
https://pygsheets.readthedocs.io/en/latest/authorization.html

Save your `client_secret.json` file in the same directory as where you're going to run your script.

Then run this in a Python script or terminal:

```
from py_googlesheets_grading import Grader

Grader().grade_students(spreadsheet_url="YOUR_URL")

```

### Options:

The `grade_students` function has some parameters.

- `DO_GRADE=[]`: if you want to JUST grade one or two students, add this argument with a list of all the student IDs you want to grade. It will skip everybody else.
I.e `Grader().grade_students(spreadsheet_url="YOUR_URL", DO_GRADE=["jwa015","asd069"])`

- `DONT_GRADE=[]`: if there is anyone in your sheets you **don't** want to grade. It will grade everybody but those students. I.e
`Grader().grade_students(spreadsheet_url="YOUR_URL", DONT_GRADE=["xdo033"])`

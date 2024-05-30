# Django ToDo list

This is a todo list web application with basic features of most web apps, i.e., accounts/login, API, and interactive UI. To do this task, you will need:

- CSS | [Skeleton](http://getskeleton.com/)
- JS  | [jQuery](https://jquery.com/)

## Explore

Try it out by installing the requirements (the following commands work only with Python 3.8 and higher, due to Django 4):

```
pip install -r requirements.txt
```

Create a database schema:

```
python manage.py migrate
```

And then start the server (default is <http://localhost:8000>):

```
python manage.py runserver
```

Now you can browse the [API](http://localhost:8000/api/) or start on the [landing page](http://localhost:8000/).

## Task

Create a GitHub Actions workflow for this project. The workflow should:

1. Run on every push to the `main` branch and pull requests to the `main` branch.
2. Run name should contain information about user triggering the workflow.
3. Run name should contain information about hash of the commit that triggering the workflow.
4. Run should have a `python-ci` job with above steps:
    1. step that runs the tests. (Tests are included in the app.)
    1. step that generates a coverage with `coverage`
    1. step that displays the coverage report in the console
    1. step that checks the code style. (Code style is checked with `flake8`.) - this should not be a blocker for the workflow.
    1. step that that checks complexity of the code. (Code complexity is checked with `flake8`.) - this should not be a blocker for the workflow.
    1. step that uploads python code as an artifact
    1. Python version should be controlled from the variable
5. Create a PR to this repository with the changes.
6. PR workflow should be triggered and should pass all the checks.

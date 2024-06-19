# Django ToDo list

This project is an advanced to-do list web application with the basic features of most web apps, such as accounts/login, API, and interactive UI. 

To complete this task, you will need:

- CSS | [Skeleton](http://getskeleton.com/)
- JS  | [jQuery](https://jquery.com/)

## Explore

Try it out by installing the requirements (the following commands work only with Python 3.8 and higher due to Django 4):

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

You can now browse the [API](http://localhost:8000/api/) or start on the [landing page](http://localhost:8000/).

## Task

In this task, you have to create a GitHub Actions workflow to automate testing and quality checks for this project. The workflow should adhere to the following specifications:

1. Run on every push to the `main` and `develop` branches and on pull requests to the `main` branch.
2. The run name should contain information about the user triggering the workflow.
3. The run name should contain information about the commit hash that triggered the workflow.
4. The run should have a `python-ci` job with steps as follows:
    1. step that runs the tests. (Tests are included in the app.)
    2. step that generates a coverage with `coverage`.
    3. step that displays the coverage report in the console.
    4. step that checks the code style. (Code style is checked with `flake8`.) This should not be a blocker for the workflow.
    5. step that checks the complexity of the code. (Code complexity is checked with `flake8`.) This should not be a blocker to the workflow.
    6. step that uploads Python code as an artifact.
    7. The Python version should be controlled from the variable.
5. Create a PR to this repository with the changes.
6. PR workflow should be triggered and should pass all the checks.

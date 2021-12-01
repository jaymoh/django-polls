#Django Tutorial Polls App

This repository contains the complete code for the <a href="https://www.djangoproject.com/">Django </a> Framework's <a href="https://docs.djangoproject.com/en/3.2/intro/tutorial01/"> Polls App</a> tutorial. 

It includes minor configurations in the `settings.py` file to use `PostgresSQL` database installed locally instead of the `SQLite` database used in the Django tutorial. 

Everything else should match the code you have if you followed the tutorial up to <a href="https://docs.djangoproject.com/en/3.2/intro/tutorial07/"> Part 7 <a/>

The SECRET_KEY variable in `mysite/settings.py` has been removed, and you should generate yours with the command below, then set it in the file: 

`python -c 'from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())'`

### Startup instructions
Polls is a basic Django app to conduct Web-based polls. The user interface is not that great because this repo was just meant for a demo tutorial, however, the functionalities work as expected. 

For each question, visitors are allowed to choose from defined answers.

1. Add `polls` to the INSTALLED_APPS section in the `settings.py` as shown below:

``
INSTALLED_APPS = [
   ...
   'polls',
   ]
``
2. Include the polls `URLconf` in your project `urls.py` like this:

```path('polls/', include('polls.urls')),```

3. To create the polls models, run the command below: 

```python manage.py migrate```

4. To start the development server, run the command below: 

```python manage.py runserver```

5. Once your server is up, visit the admin interface at <a href="http://127.0.0.1:8000/admin/">http://127.0.0.1:8000/admin/ </a> to create a poll.


6. Visit <a href="http://127.0.0.1:8000/polls/">http://127.0.0.1:8000/polls/ </a> to place a vote. 
# restapi

Clone into an empty github repository. Move inside 
Run this line into terminal: django-admin startproject mysite
Run this line into terminal while inside restapi/mysite: python manage.py startapp myapi
Install django-heroku.
Add these lines to settings.py: import django_heroku        
                                django_heroku.settings(locals())
Run these line into terminal: heroku login
                              heroku create
In terminal, in restapi/mysite, run pip freeze > requirements.txt
Then run these lines: git add .
                      git commit -m "Deploying into heroku"
                      git push origin master
To connect with heroku: heroku git:remote <name created while running heroku create>
                        git push heroku main
Run this line into terminal: pip install gunicorn
Create a file named Procfile in the same level as manage.py and put this line inside of the file: web: gunicorn <app name put while running python manage.py startapp>.wsgi
Run this line into terminal: pip freeze > requirements.txt
Push into git and then run: git push heroku master
If you get this error:
remote:        SyntaxError: invalid syntax
remote:  !     Error while running '$ python manage.py collectstatic --noinput'.
remote:        See traceback above for details.
remote:
remote:        You may need to update application code to resolve this error.
remote:        Or, you can disable collectstatic for this application:
remote:
remote:           $ heroku config:set DISABLE_COLLECTSTATIC=1
remote:
remote:        https://devcenter.heroku.com/articles/django-assets
Run into terminal: heroku config:set DISABLE_COLLECTSTATIC=1
Run: heroku open
If it works, follow this link: https://medium.com/swlh/build-your-first-rest-api-with-django-rest-framework-e394e39a482c
Run: pip freeze > requirements.txt before pushing into heroku.

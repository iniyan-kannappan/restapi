# restapi

Clone into an empty github repository. Move inside the directory.</br>
Run this line into terminal: pip install django</br>
Run this line into terminal: django-admin startproject mysite</br>
Run this line into terminal while inside restapi/mysite: python manage.py startapp myapi</br>
Install django-heroku.</br>
Add these lines to settings.py: import django_heroku    </br>    
                                django_heroku.settings(locals())</br>
Run these line into terminal: heroku login</br>
                              heroku create</br>
In terminal, in restapi/mysite, run pip freeze > requirements.txt</br>
Then run these lines: git add .</br>
                      git commit -m "Deploying into heroku"</br>
                      git push origin master</br>
To connect with heroku: heroku git:remote name created while running heroku create</br>
                        git push heroku main</br>
Run this line into terminal: pip install gunicorn</br>
Create a file named Procfile in the same level as manage.py and put this line inside of the file: web: gunicorn project name put while running django-admin startproject.wsgi</br>
Run this line into terminal: pip freeze > requirements.txt</br>
Add and commit edited file and push into git and then run: git push heroku master</br>
If you get this error:</br>
remote:        SyntaxError: invalid syntax</br>
remote:  !     Error while running '$ python manage.py collectstatic --noinput'.</br>
remote:        See traceback above for details.</br>
remote:
remote:        You may need to update application code to resolve this error.</br>
remote:        Or, you can disable collectstatic for this application:</br>
remote:</br>
remote:           $ heroku config:set DISABLE_COLLECTSTATIC=1</br>
remote:</br>
remote:        https://devcenter.heroku.com/articles/django-assets</br>
Run into terminal: heroku config:set DISABLE_COLLECTSTATIC=1</br>
Run: heroku open</br>
If it works, follow this link: https://medium.com/swlh/build-your-first-rest-api-with-django-rest-framework-e394e39a482c</br>
Run: pip freeze > requirements.txt before pushing into heroku.</br>

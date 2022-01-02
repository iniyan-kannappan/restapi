# restapi

1. Clone into an empty github repository. Move inside the directory.</br>
2. Run this line into terminal: pip install django</br>
3. Run this line into terminal: django-admin startproject mysite</br>
4. Run this line into terminal while inside restapi/mysite: python manage.py startapp myapi</br>
5. Install django-heroku.</br>
6. Add these lines to settings.py: import django_heroku    </br>    
                                django_heroku.settings(locals())</br>
7. Run these line into terminal: heroku login</br>
                              heroku create</br>
8. In terminal, in restapi/mysite, run pip freeze > requirements.txt</br>
9. Then run these lines: git add .</br>
                      git commit -m "Deploying into heroku"</br>
                      git push origin master</br>
10. To connect with heroku: heroku git:remote name created while running heroku create</br>
                        git push heroku main</br>
11. Run this line into terminal: pip install gunicorn</br>
12. Create a file named Procfile in the same level as manage.py and put this line inside of the file: web: gunicorn project name put while running django-admin startproject.wsgi</br>
13. Run this line into terminal: pip freeze > requirements.txt</br>
14. Add and commit edited file and push into git and then run: git push heroku master</br>
15. If you get this error:</br>
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
16. Run: heroku open</br>
17. If it works, follow this link: https://medium.com/swlh/build-your-first-rest-api-with-django-rest-framework-e394e39a482c</br>
18. Run: pip freeze > requirements.txt before pushing into heroku.</br>

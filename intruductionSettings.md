# Creat environment of Django

1. Create directory for General Project Storage
cd Desktop
mkdir fileName
cd fileName

2. Create Virtual Environment

virtualenv -p python3 .
source bin/activate
pip freeze               for test install

3. install Django & start project

pip install django       newest version
mkdir src && cd src
django-admin.py stratproject resturants .

4. Create new setting module

build a file under project file 
cd resturants && mkdir settings
cd settings && create file __init__.py create base.py
copy past old.settings.py to base.py
BASE_DIR  go one level down
in __init_.py ( from .base import *
                from .production import *
             try:
                from .local import *
             except:
                pass)
cd ..

in 
create old_settings.py

5. some other common installations

# for a postgresql database
pip install psycopg2
# for a mysql database
pip install MySQL-python
# for use on heroku
pip install gunicorn dj-database-url
pip install django-crispy-forms
pip install pillow

6. create requirements.txt file
pip freeze > requirements.txt

7. Run Migration & Createsupreuser

python manage.py migrate
python manage.py createsuperuser

8. create production.py and local.py copy base.py to there and change DEBUG = false in Production Secret_key as well

# Init Local Dev
python3.6 -m venv venvTaiga
source ../venvTaiga/bin/activate

pip install -r requirements.txt

./init.sh
添加admin用户

python manage.py migrate --noinput
python manage.py loaddata initial_user
python manage.py loaddata initial_project_templates

python manage.py compilemessages

CommandError: Can't find msgfmt. Make sure you have GNU gettext tools 0.15 or newer installed.
```brew install gettext```
```brew link gettext --force```

python manage.py collectstatic --noinput
python manage.py sample_data



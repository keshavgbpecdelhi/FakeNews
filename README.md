# FAKENEWS
FAKENEWS is a news rating plateform in which users can rate the News while keeping themselves aware of fake News. In addition to this user can also post News.

### Installation
Install Python3 and above versions
Install git & run this command :-
```
git clone https://github.com/keshavgbpecdelhi/FakeNews.git
```

After cloning open cmd/bash to this location.

Next, Install virtualenv, command ```pip install virtualenv```.

Incase of PermissionDeniedError, reinstall the package again should make it work.
To uninstall any pip installed package, use command ```pip uninstall <package-name>```

Now create an enviroment in the same project folder using the command ```virtualenv env```
Then activate the created enviroment using the command :-

For Windows ->
```. ./env/Scripts/activate```

For Linux ->
```source ./env/bin/activate```

In case of virtualenv disability issues in windows, use ```Set-ExecutionPolicy Unrestricted -Force``` command in PowerShell (admin-mode)

Next, use this command ```pip install -r requirements.txt``` to install all the dependencies required for this project to run properly.
After this process is finished, use command ```python``` or ```python3``` to open python CLI in the terminal & then enter this 2 lines to install nltk package :-
```
import nltk
nltk.download("punkt")
exit()
```
```exit()``` will get you out of your Python CLI to where you were.

If you've reached this step, the installation of this project should be completed by now.

DB migrations are needed for any kinda backend to work properly, so use this set of commands :- 

```
python manage.py makemigrations
python manage.py migrate
python manage.py migrate --run-syncdb
python manage.py createsuperuser
python manage.py shell_plus
>> user = User.objects.first()
>> UserDataModel.objects.create(user=user)
```
Note :- For linux users, use python3 instead of python

At last change directory to *fake_news_classifier* :
```cd fake_news_classifier```

then, run this command -

Windows -> 
```python manage.py runserver```

Linux -> 
```python3 manage.py runserver```

This will run the django backend server. Now, you can visit the link "localhost:8000" to view the project :grin:

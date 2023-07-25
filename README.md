# App.py
* I must create an id variable for the table when I am creating the database but I must delete later when I do the POST and PATCH

# helper.py 
* I use it to populate the database

* I must check what is wrong when I print the excel. I got an extra column on the left with the index number. I solved by adding no index:
    with pd.ExcelWriter('Amet_data.xlsx') as writer:
        df1.to_excel(writer, index=False, sheet_name='paintingsData')
        df2.to_excel(writer, index=False, sheet_name='customers')
        df3.to_excel(writer, index=False, sheet_name='fans')


# Deploy app in azure

1. Create a github repository

2. install dependencies: 

python3 -m venv .venv
source .venv/bin/activate

pip install -r requirements.txt // give me an error so I ran this:
pip freeze > requirements.txt

3. Run the app:
flask run


# Delpoy in azure intructions

https://learn.microsoft.com/en-us/azure/app-service/quickstart-python?tabs=flask%2Cmac-linux%2Cazure-portal%2Clocal-git-deploy%2Cdeploy-instructions-azportal%2Cterminal-bash%2Cdeploy-instructions-zip-azcli



# requirenments.txt list:
attrs==22.2.0
autopep8==2.0.0
azure-common==1.1.28
azure-communication-email==1.0.0
azure-core==1.28.0
azure-mgmt-core==1.4.0
bcrypt==4.0.1
certifi==2023.5.7
charset-normalizer==3.2.0
click==8.1.3
commonmark==0.9.1
et-xmlfile==1.1.0
flake8==6.0.0
Flask==2.2.2
Flask-Bcrypt==1.0.1
Flask-Cors==3.0.10
Flask-Login==0.6.2
flask-marshmallow==0.14.0
Flask-SQLAlchemy==3.0.3
Flask-WTF==1.1.1
greenlet==2.0.1
idna==3.4
iniconfig==1.1.1
isodate==0.6.1
itsdangerous==2.1.2
Jinja2==3.1.2
MarkupSafe==2.1.1
marshmallow==3.19.0
marshmallow-sqlalchemy==0.29.0
mccabe==0.7.0
msrest==0.7.1
numpy==1.24.1
oauthlib==3.2.2
openpyxl==3.1.1
packaging==22.0
pandas==1.5.2
peewee==3.15.4
pluggy==1.0.0
plyer==2.1.0
pycodestyle==2.10.0
pyflakes==3.0.1
Pygments==2.13.0
pyodbc==4.0.35
pypyodbc==1.3.6
pytest==7.2.0
python-dateutil==2.8.2
pytz==2022.7
requests==2.31.0
requests-oauthlib==1.3.1
rich==12.6.0
six==1.16.0
SQLAlchemy==1.4.46
tomli==2.0.1
typing_extensions==4.7.1
urllib3==2.0.3
Werkzeug==2.2.2
WTForms==3.0.1
xlrd==2.0.1


pip install azure-communication-email

This is not working. I need to check it out later
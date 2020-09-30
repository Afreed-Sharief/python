Openshift quickstart: Django
This is a Django project that you can use as the starting point to develop your own and deploy it on an OpenShift cluster.

NOTE: This version contains obsolete Django 1.11.x LTS which works with RHEL/Centos 7. Consider switching to RHEL/Centos 8 with Django 2.2.x LTS in branch 2.2.x.

The steps in this document assume that you have access to an OpenShift deployment that you can deploy applications on.

What has been done for you
This is a minimal Django 1.11 project. It was created with these steps:

Create a virtualenv
Manually install Django and other dependencies
pip freeze > requirements.txt
django-admin startproject project .
Update project/settings.py to configure SECRET_KEY, DATABASE and STATIC_ROOT entries
./manage.py startapp welcome, to create the welcome page's app
From this initial state you can:

create new Django apps
remove the welcome app
rename the Django project
update settings to suit your needs
install more Python libraries and add them to the requirements.txt file
Special files in this repository
Apart from the regular files created by Django (project/*, welcome/*, manage.py), this repository contains:

openshift/         - OpenShift-specific files
├── scripts        - helper scripts
└── templates      - application templates

requirements.txt   - list of dependencies

# FLASK_SQLALCHEMY_BASICS 
## Creating an environment first ##
 ## Install the python3-venv package ##
  sudo apt install python3.10-venv
 ## Recreate your virtual environment ## 
  python3 -m venv env
 ## Activare the environment ## 
  source env/bin/activate


## Install Libraries ##
 pip install flask flask-sqlalchemy

## Create app.py file ## 
 touch app.py

 ## Create Models ##

 ## Create relationships ##

 ## Create a Database ##
  flask shell
  from app import db
  db.create_all()

  exit()

  ## Opening The Database ##
  sqlite3 db.sqlite3
  cd instance
  .tables
  .schema

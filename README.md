# LAP 4 W2 D1 To do list app 

# ENV SETUP 
- `pipenv install virtualenv`
- `virtualenv env`
- `source env/bin/activate`

# Install:
- `pipenv install flask `
- `pipenv install flask flask-sqlalchemy`
- create app.py :
```
from distutils.log import debug
from flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
    return "Hello Igor"

if __name__ == "__main__":
    app.run(debug=True)

```
- python app.py (see page)
- create static , templates(index.html) folders
- import render_template
- create base.html
- add h1
- create css in static + main.css + add some stylesheet
 
## Database
- import `from flask_sqlalchemy import SQLAlchemy`
 ```
 app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///test.db'
db = SQLAlchemy(app) # Initialize database 
``` 
(3x/ relative vs 4x/ absolue)

 - create class Todo and import `from datetime import datetime`
 - adding :
 ```
  def __reor__(self):
        return'<Task %r>' % self.id
```
- Setup Database: 
-- python 
-- from app import db 
-- db.create_all()
--exit()

- index.html add div and table 
- modify app route adding if else statement
- import request
- add redirect and new_task


## HEROKU 
- heroklu cli - donwloan 
- heroku login 
- git init 
- pipenv install gunicorn
- pipenv freeze > requirements.txt 
- heroku create <name>
- git remote -v 

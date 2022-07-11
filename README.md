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


## What is Flask?

- A micro web-framework written in Python.
  - Does not require particular tools or libraries
- Helps combine multiple aspects: Python, SQL, routing...
- Simplifies scaling from start-up --> complex applications
- Offers suggestions, but doesn't enforce any dependencies or project layout
  
  
## How to set-up

- Installed using the project interpreter
- File > Settings > Project: ______ > Project Interpreter > + > Flask  
- Will use local host to display:   http://127.0.0.1:5000/

## setup.py

- Holds flask code
- Controls methods for redirecting and connection control

### route('/url')

- Tells browser what to display when at '/url'

- html and css files should be contained in respective directories

```python
from flask import Flask, render_template


app = Flask(__name__)

@app.route("/")
def home():
    return render_template("index.html")
```

- index.html will only be a template in this state

- hrefs for other html files / websites within index will need changing in order to be recognised:

```python
href="location.html"

href="{{ url_for('location') }}"
```

- hrefs for css files must be added to the file hierarchy under directories 'static' and then 'css'

- They will still not be loaded by your html files though as the href once again needs to be changed.

```python
href = "styles/style.styles"

href="{{ url_for('static', filename='styles/style.styles') }}"
```
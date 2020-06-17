
## What is Flask?

- A micro web-framework written in Python.
  - Does not require particular tools or libraries
- Helps combine multiple aspects: Python, SQL, routing...
- Simplifies scaling from start-up --> complex applications
- Offers suggestions, but doesn't enforce any dependencies or project layout
  
  
## How to set-up

- Installed using the project interpreter
- File > Settings > Project: ______ > Project Interpreter > + > Flask  


- Project root:   setup.py     &    todo dir
    - todo holds source code
       - Contains __init__.py, app.py
            - __init__.py   allows you to import from todo, treats it like package
            - app.oy        application root
    
- setup.py file example:
```python
from setuptools import setup, find_packages

requires = [
    'flask',
    'flask-sqlalchemy',
    'psycopg2',
]

setup(
    name='flask_todo',
    version='0.0',
    description='A To-Do List built with Flask',
    author='<Your actual name here>',
    author_email='<Your actual e-mail address here>',
    keywords='web flask',
    packages=find_packages(),
    include_package_data=True,
    install_requires=requires
)
```
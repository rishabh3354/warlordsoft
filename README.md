## This is simple package just to open warlordsoft website:

### How to import this package:
```
Step1: Open your python3 shell
Step2: Import main function using cmd

➜  warlordsoft python3
Python 3.8.10 (default, Mar 15 2022, 12:22:08) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from warlordsoft import main

Done!
 
```

## :: PSY ::
### How to upload python package:

### Make sure you have upgraded version of pip
Linux/MAC OS
```
python3 -m pip install --upgrade pip
```

### Create a project with the following structure
```
packaging_tutorial/
├── LICENSE
├── pyproject.toml
├── README.md
├── setup.cfg
├── src/
│   └── example_package/
│       ├── __init__.py
│       └── example.py
└── tests/

## create dir structure using cmd
```
touch LICENSE && touch pyproject.toml && touch setup.cfg && mkdir -p src/warlordsoft && touch src/warlordsoft/__init__.py && touch src/warlordsoft/main.py && mkdir tests

```

# Running the build
### Make sure your build tool is up to date
```
Linux/MAC OS
```
python3 -m pip install --upgrade build
```

### Create the build
```
python3 -m build
```


### Install twine
```
python3 -m pip install --upgrade twine
```


### upload to pypi
```
for testpypi (test env)
python3 -m twine upload --repository testpypi dist/*

for revison upload to latest
python3 -m twine upload --repository testpypi --skip-existing dist/*

for pypi (prod)
python3 -m twine upload dist/*
```

### Install same package from test env
```
pip install -i https://test.pypi.org/simple/ warlordsoft==0.0.1


https://test.pypi.org/project/warlordsoft/

```



### References
https://packaging.python.org/tutorials/packaging-projects/
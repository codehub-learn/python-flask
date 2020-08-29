# Flask


## Getting started

This document will provide information about what is needed to have installed for the Flask course.
Overall we will need:
- an IDE
- Python (preferrably 3.3+) and Flask  
- Postman

### IDE

This is up to personal preference. We recommend although either VS code, either PyCharm. Both are highly configurable to each one's taste but also their default installation provides everything that you will need initially. 


### Flask Installation

#### Prerequisites

Before installing Flask (and other useful modules) make sure you have Python and pip installed in your machine.
Simply for Python tyle in a command line:

```cmd
$ python --version
```

This should return something like `3.8.1`

And for pip:

```cmd
$ pip --version
```

Should return something like `pip 20.0.2 from /usr/lib/python3/dist-packages/pip (python 3.8)`

If any of those does not work please check their installation options:
- [Python](https://www.python.org/downloads/)
- [pip](https://pip.pypa.io/en/stable/installing/)


#### Flask

[Flask](https://flask.palletsprojects.com/en/1.1.x/) is a microframework. It provides complete functionality at its core and will allow your applications to run in a single file (Do not do that tho). In a nutshell, Flask aims to be everything that you need and nothing you do not. 

You can install Flask as any other python package. 

```cmd
$ pip install Flask
```

Flask, as the vast majority of the external modules/libraries/frameworks that we will install in our environment, depends on some other modules. When we install Flask we will also install a list of other modules including but not limited to [Jinja](https://palletsprojects.com/p/jinja/) (template language) and [Werkzeug](https://palletsprojects.com/p/werkzeug/) (Python interface between applications and servers).

There are several other useful packages that we typically need when we are building a web application with Flask such as [python-dotenv](https://github.com/theskumar/python-dotenv#readme) which allows us to use and read environmental variables from files and [simplejson](https://simplejson.readthedocs.io/en/latest/)

```cmd
$ pip install python-dotenv
$ pip install simplejson
```

#### Virtual Environments

[Virtual environmets](https://docs.python.org/3/library/venv.html#) are Python environments that include Python interpreter and modules independently and isolated from the ones that are installed in a system or other virtual environments. 
To keep it sort, a virtual environment allows us to handle dependencies individually for each one of our projects. The more projects we build the more dependencies/modules we will need and in several cases, we will need a different version of those modules for different projects and this may cause compatibility issues. 

While it is not mandatory to use them, it is highly recommended to do so. If we are using any version before Python 3.3 we need to manually install the `virtualenv` toolkit. 

```cmd
$ pip install virualenv
```

For any other Python version, `venv` is included in the standard library. 

To develop using a virtual environment (assuming that we have any Python version > 3.3):


```cmd
$ mkdir my_app
$ cd my_app
$ python -m venv venv
```

This will create a virtual environment in a directory called my_app. We will also need to activate it.

```cmd
$ . venv/bin/activate
```
From this point and onwards, we can use pip to install any library we need for a particular project.
e.g:
```cmd
$ pip install Flask
```

### Flask Extentions

As mentioned earlier, Flask is a microframework. When we want to add extra functionality to our applications like connecting to databases or building production REST APIs, we will need to add some extensions that will allow us to support this.

List of available Flask extensions can be found [here](https://pypi.org/search/?c=Framework+%3A%3A+Flask).


### Postman

Postman is a tool that allows us to test our APIs. You can find it [here](https://www.postman.com/downloads/) to download it.



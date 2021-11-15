# Google for Education - Python

## Notes for Google's Python Online Tutorial
For more information: [Google for Education - Python](https://developers.google.com/edu/python) 


### Language Introduction
- Python is dynamic, interpreted lanaguage.
- NO TYPE DECLARATIONS OF VARIABLES, PARAMETERS, FUNCTIONS, OR METHODS IN SOURCE CODE.
    - Allows code to be short and flexiable.
- Python is case sensitive
- Does not require a semicolon

```
$ python3           ## Run the Python interpreter
>>> a = 6           ## Set a Variable
>>> a               ## Entering an Expression prints
6
>>> a + 2
>>> a
8
>>> a = 'hi'        ## 'a' can hold a string
>>> a
'hi'
>>> len(a)          ## call the len() function on a str
2
>>> a + len(a)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate str (not "int") to str
>>> a + str(len(a))
'hi2'
>>> foo
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'foo' is not defined
>>> ^D               ## type CTRL-d to exit  
```

### Python Source Code
Python source files use the ".py" extension and are called "modules".

With a Python module `hello.py`, run with the shell command `python hello.py Alice` which calls the Python interpreter to execute the code in `hello.py`, passing it the command line argument 'Alice'.

View Example: [hello.py](hello.py)

To run the program: 
```
$ python hello.py Guido
Hello there Guido
```

### User-defined Functions

```py
# Defines a "repeat" function that takes 2 arguments.
def repeat(s, exclaim):
    
    #Returns the string 's' repeated 3 times.
    #If exclaim is true, add exclamation marks.

    result = s + s + s # can also use "s * 3" which is faster (Why?)
    if exclaim:
        result = result + '!!!'
    return result
```
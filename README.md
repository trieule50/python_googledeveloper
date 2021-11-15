# Google for Education - Python

## Notes for Google's Python Online Tutorial
For more information: [Google for Education - Python](https://developers.google.com/edu/python) 


### Language Introduction
- Python is dynamic, interpreted lanaguage.
- NO TYPE DECLARATIONS OF VARIABLES, PARAMETERS, FUNCTIONS, OR METHODS IN SOURCE CODE.
    - Allows code to be short and flexiable.

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
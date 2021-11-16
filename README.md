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

```py
def main():
    print repeat('Yay', False)      ## YayYayYay
    print repeat('Woo Hoo', True)   ## Woo HooWoo HooWoo Hoo!!!
```

### Indentation

One unusual Python feature is that the whitespace indentation of a piece of code affects its meaning.

### Code Checked at Runtime

Python does very little checking at compile time. 

```py
def main():
    if name == 'Guido':
        print repeeeet(name) + '!!!'
    else:
        print repeat(name)
```

The funny thing in Python ... this code compiles and runs fine so long as the name at runtime is not 'Guido'.

### Variable Names

Python prefers the underscore method but guides developers to defer to camelCasing if integrating into existing Python code. 

### More on Modules and their Namespaces

These are collectively known as the "Python Standard Library." Commonly used modules/packages include:

- sys — access to exit(), argv, stdin, stdout, ...
- re — regular expressions
- os — operating system interface, file system

### Online help, help(), and dir()

Below are some ways to call help() and dir() from the interpreter:

- `help(len)` — help string for the built-in `len()` function; note that it's "len" not "len()", which is a call to the function, which we don't want

- `help(sys)` — help string for the sys module (must do an import sys first)
dir(sys) — dir() is like `help()` but just gives a quick list of its defined symbols, or "attributes"

- `help(sys.exit)` — help string for the exit() function in the sys module

- `help('xyz'.split)` — help string for the split() method for string objects. You can call `help()` with that object itself or an example of that object, plus its attribute. For example, calling `help('xyz'.split)` is the same as calling `help(str.split)`.

- `help(list)` — help string for list objects

- `dir(list)` — displays list object attributes, including its methods

- `help(list.append)` — help string for the `append()` method for list objects

### String Slices

The slice s[start:end] is the elements beginning at start and extending up to but not including end. 

Example: 

Hello

- s[1:4] is 'ell' -- chars starting at index 1 and extending up but not including index 4
- s[1:] is 'ello' -- omitting either index defaults to the start or end of the string
- s[:] is 'Hello' -- omitting both always give us a copy of the whole thing
- s[1:100] is 'ello' -- an index that is too big is truncated down to the string length

- s[-1] is 'o'
- s[-4] is 'e'
- s[:-3] is 'He'
- s[-3:] is 'llo'

### String %

Python has a printf()-like facility to put together a string. The % operator takes a printf-type format string on the left (%d int, %s string, %f/%g floating point), and the matching values in a tuple on the right:

```py
text = (
    "%d little pigs come out, "
    "or I'll %s, and I'll %s, "
    "and I'll blow your %s down."
    % (3, 'huff', 'puff', 'house'))
```

### If Statement

Python does not use {} to enclose blocks of code if/loops/functions etc.. Instead Python use the colon(:) and indentation/whitespace to group statements. 

The 'zero' values all count as false: None, 0, empty string, empty list, empty dictionary.

Python has the usual comparison operations: ==, !=, <, >, <=, >=

The boolean operators are spelled out words *and*, *or*, *not*

Example: 

```py
  if speed >= 80:
    print 'License and registration please'
    if mood == 'terrible' or speed >= 100:
      print 'You have the right to remain silent.'
    elif mood == 'bad' or speed >= 90:
      print "I'm going to have to write you a ticket."
      write_ticket()
    else:
      print "Let's try to keep it under 80 ok?"
```


# Google for Education - Python

## Notes for Google's Python Online Tutorial
For more information: [Google for Education - Python](https://developers.google.com/edu/python) 

### Python Strings

Python has a built-in string class named "str" with many handy features.

Python strings are "immutable" which means they cannot be changed after they are created. 
    - Since strings can't be changed, we construct "new" strings as we go to represent computed values. 

Characters in a string can be accessed using the standard [] syntax. 
    - Python uses a zero-basing indexing

```py
  s = 'hi'
  print s[1]          ## i
  print len(s)        ## 2
  print s + ' there'  ## hi there
```

Unlike Java, the '+' does not automatically convert numbers or other types to string form.

str() function converts values to a string form

```py
  pi = 3.14
  ##text = 'The value of pi is ' + pi      ## NO, does not work
  text = 'The value of pi is '  + str(pi)  ## yes
```

For numbers, the standard operators, +, /, * work in the usual way. 

If you want integer division, it is most correct to use 2 slashes -- e.g. 6 // 5 is 1

```py
raw = r'this\t\n and that'

  # this\t\n and that
print raw

multi = """It was the best of times.
  It was the worst of times."""

  # It was the best of times.
  #   It was the worst of times.
print multi
```
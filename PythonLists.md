# Google for Education - Python

## Notes for Google's Python Online Tutorial
For more information: [Google for Education - Python](https://developers.google.com/edu/python) 

### Python Lists

Lists work similarly to strings -- use the len() function and square brackets [] to access data, with the first element at index 0. 

Ex.

```py
colors = ['red', 'blue', 'green']
print colors[0] ## red
print colors[2] ## green
print len(colors) ## 3
```

Assignment with an = on lists does not make a copy. Instead, assignment makes the two variables point to the one list in memory.

The 'empty list' is just an empty pair of brackets []. The '+' works to append two list, so [1,2] + [3,4] yeilds [1,2,3,4]
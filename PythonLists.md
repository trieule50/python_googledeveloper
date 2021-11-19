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

Ex.
```py
b = colors ## Does not copy the list
```

The 'empty list' is just an empty pair of brackets []. The '+' works to append two list, so [1,2] + [3,4] yeilds [1,2,3,4]

### FOR and IN

Python's *for* and *in* constructs are extremely useful, the first use of them we'll see is with list. The *for* construct -- `for var in list` -- is an easy way to look at each element in a list. Do not add or remove from the list during iteration.

Ex.
```py
squares = [1, 4, 9, 16]
sum = 0
for num in squares:
    sum += num
print sum ## 39
```

The  *in* construct on its own is an easy way to test if an element appears in a list -- `value in collection` -- tests if value is in the collection, returning True/False.

Ex. 

```py
list = ['larry', 'curly', 'moe']
if 'curly' in list:
    print 'yay'
```

for/in can work on strings. The string acts like a list of its chars, so `for ch in s: print ch` prints all the chars in a string.

#### Range

The range(n) function yields the numbers 0, 1, ... ,n-1 and range(a,b) returns a, a+1, ... , b-1 -- up to but not including the last number. The combination of the for-loop and the range function allow you to build a traditional numeric loop.

Ex. 

```py
## print the numbers from 0 to 99
for i in range(100):
    print i
```

#### While Loop

Python also has the standard while-loop, and the *break* and *continue* statements work as in Java and C++, altering the course of the innermost loop. While loop gives you total control over the index numbers. 

Ex.

```py
## Access every 3rd element in a list

i=0
while i < len(a):
    print a[i]
    i = i + 3
```

#### List Methods

Common list methods

- list.append(elem) -- adds a single element to the end of the list. Common error: does not return the new list, just modifies the original.

- list.insert(index, elem) -- inserts the element at the given index, shifting elements to the right.

- list.extend(list2) -- adds the elements in list2 to the end of the list. Using + or += on a list is similar to using extend()

- list.index(elem) -- searches for the given element from the start of the list and returns its index

- list.remove(elem) -- searches for the first instance for the given element and removes it

- list.sort() -- sorts the list in place (does not return it)

- list.reverse() -- reverses the list in place (does not return it)

- list.pop(index) -- removes and returns the element at the given index. Returns the rightmost element if index is omitted.

```py
list = ['larry', 'curly', 'moe']
list.append('shemp')         ## append elem at end
list.insert(0, 'xxx')        ## insert elem at index 0
list.extend(['yyy', 'zzz'])  ## add list of elems at end
print list  ## ['xxx', 'larry', 'curly', 'moe', 'shemp', 'yyy', 'zzz']
print list.index('curly')    ## 2

list.remove('curly')         ## search and remove that element
list.pop(1)                  ## removes and returns 'larry'
print list  ## ['xxx', 'moe', 'shemp', 'yyy', 'zzz']
```

Common error:

```py
list = [1, 2, 3]
print list.append(4)   ## NO, does not work, append() returns None
## Correct pattern:
list.append(4)
print list  ## [1, 2, 3, 4]
```

##### List Build Up
One common pattern is to start a list a the empty list [], the use append() or extend() to add elements to it.

```py
list = []
list.append('a')
list.append('b')
```

##### List Slices

Slices work on list just as with strings, and can also be used to change sub-parts of the list.

```py
list = ['a', 'b', 'c', 'd']
print list[1:-1]  ## ['b', 'c']
list[0:2] = 'z'   ## replace ['a', 'b'] with ['z']
print list        ## ['z', 'c', 'd']
```
# Python Interview Questions
 _Due 4/29/2022_

### Questions
##### 1. What is Python?
Python is an interpreted (meaning the written code isn't translated to a computer-readable format at runtime), object oriented, high-level programming language that's intended for general purposes such as app or web development.

Here is an example of a line of python code!
```sh
print("Hello World!")
```

##### 2. What is a variable?
Variables are containers for storing data values and are created the moment you assign its first value. They don't need to be declared as a specific type of value, and their type can be changed after they've been set.

General Variable Example
```sh
x = ""Hello"
y = "World!"
print(x,y)
```

Changed Variable Example
```sh
x = 4
x = "Hello World!"
print(x)
```

##### 3. What is a namespace?
A namespace is an organizational system/region for a program that provides identifiers (e.g. the names of types, functions, variables, etc.). They organize code into logical groups to prevent name collisions that can occur when the code base has multiple libraries.

##### 4. What is the difference between list and tuple?
A **list** is declared in other langauges and **do not** always need to be homogenous. In Python, it's a type of container used to store multiple data simultaneously.
```sh
list_data = ["an", "example", "of", "a", "list"]
```


A **tuple** is also a sequence data type that contains elements of different data types, but these are immutable. Tuples are separated by commas and faster than a list.

```sh
tuple_data = ("this", "is", "an", "example", "of", "tuple")
```
**Differences Between List & Tuples in Python**
| Lists | Tuples |
| ----- | ----- |
| Lists are mutable | Tuples are immutable |
| Implication of iterations is time consuming | Implication of iterations is comparatively faster |
| Lists are better for performing operations (e.g. insertion & deletion) | Tuple data type is appropiate for accessing the elements |
| Lists consume more memory | Tuples consume less memory compared to lists |
| Lists have several built-in methods | Tuples don't have many built-in methods |
| Unexpected changes & errors are more likely to occur | Harder to take place |

##### 5. How can you convert a number to a string?
There are **four** methods for converting integer data types to string data types:

**str() Method**
```sh
str(integer)
```

**"% s" % Keyword**
```sh
"% s" % integer
```

**f- String Conversion**
```sh
f"{integer}"
```

**.format() Method**
```sh
"{}".format(integer)
```

##### 6. What are the rules for local and global variables?
**Global variables** are variables that aren't defined inside any function & have a global scope.

**Local variables** are variables defined only inside a function & its scope is limited to only that function.

##### 7. Explain how to generate random numbers.
There are several ways to generate random numbers in Python. You first choose your range and then choose your function.
> Note: `import random` is required for most of these functions.

**Lists of Functions to Generate Random Numbers**

**Function**
```sh
random.randint()
```

**Syntax Example**
```sh
import random
a = random.randint(1,10)
print(a)
```

**Function**
```sh
random.randrange()
```

**Syntax Example**
```sh
import random
a = random.randrange(1,10)
print(a)
lst = [random.randrange(1,10) for i in range(0,10)]
print(1st)
```

**Function**
```sh
random.sample()
```

**Syntax Example**
```sh
import random
a = random.sample(range(1,10),1)
print(a)
1st = random.sample(range(1,10),5)
print(1st)
```

**Function**
```sh
random.uniform()
```

**Syntax Example**
```sh
import random
a = random.uniform(1,10)
print(a)
```

##### 8. What is a dictionary?
Dictionaries are used to store data values in key:value pairs. It's a collection which is ordered and changeable, but it doesn't allow duplicates. They're written with curly brackets, and have keys and values.

**Syntax Example**
```sh
thisdict = {
  "fruit": "apple",
  "age": "2 weeks",
  "color": "red"
}
print(thisdict)
```

**Result**
```sh
{'fruit': 'apple', 'age': '2 weeks', 'color': 'red'}
```

##### 9. What is the **self** keyword?
It's used to represent the instance of class. It's also used to access the attributes &  methods of the class in python. Self also binds attributes with given arguments.

##### 10. What are loop interruption statements?
They're used to return and pass statements to stop/skip iterations. Two examples are "break" & "continue".

##### 11. Explain List, Tuple, Set, and Dictionary and provide at least one instance where each of these collection types can be used.
**Lists** are used to store multiple items in a single variable. They're written inside square brackets. Lists can be used when you need your items ordered, duplicated, or changed.

**Tuples** are used to store multiple items in a single variable. They're written inside round brackets. Tuples can be used when you need your collection ordered and to be unchangeable. 

**Sets** are used to store multiple items in a single variable. They're written inside curly brackets. Sets can be used when you need your collection to be unordered, unchangeable, & indexed. 

**Dictionaries** are used to store data values in key:value pairs. They're written inside curly brackets, & have keys & values. Dictionaries can be used when you need your collection ordered, changeable, and unduplicated.

##### 12. How is Exception Handling done?
Exceptions are events used to modify the flow of control through a program when the error occurs. Exceptions are triggered automatically when errors are made in Python. 

**Several examples of exception statements**
1. **try/except** _(catches error & recovers from exceptions hoist by programmers or Python)_
2. **try/finally** _(automatically performs clean-up action)_
3. **assert** _(triggers exception conditionally in the code)_
4. **raise** _(manually triggers exception in the code)_
5. **with/as** _(implement context managers)_

##### 13. What does "#" symbol do?
The "#" symbol adds a comment.

##### 14. Write the command to get all keys from a dictionary.
```sh
dict.keys()
```

##### 15. What is range()? Give an example to explain it.
The range() function returns the sequence of the given number between the given range.

**Example Syntax**
```sh
for i in range(10):
    print(i, end=" ")
print()
```

**Result**
```sh
0 1 2 3 4 5 6 7 8 9
```

This function prints variables in the index range of 0-10.

##### 16. What does the // arithmetic operator do?
It provides the quotient value from a division operation.

##### 17. What is a data type?
A data type is a classification that dictates what a variable or object can hold. It specificies what type of mathematical, relational, or logical operations can be applied to it without causing an error. 

##### 18. What are the basic data types that are supported by the language?

**Data Type Categories for Python**
| Category | Examples |
| ---- | ---- |
| **Text Type** | str |
| **Numeric Types** | int, float, complex |
| **Sequence Types** | list, tuple, range |
| **Mapping Type** | dict |
| **Set Types** | set, frozenset |
| **Boolean Type** | bool |
| **Binary Types** | bytes, bytearray, memoryview |
| **None Type** | NoneType |

##### 19. How do you check whether the two variables are pointing to the same object?
Use _is_ to check. For example, if we look at the code:

```sh
x = ['a', 'b', 'c']
y = x        
z = ['a', 'b', 'c']
```

We could try _x is y_ and when it returns _True_, we know it points to the same object. When we try _"x is z"_ and it returns _"False"_, we know it points to a different object. 

##### 20. What is for-else and while-else?
The **else** keyword in a **for** loop specifies a block of code to be executed when the loop finishes.

The **while** keyword in a **for** loop executes a set of statements as long as a condition is true.

##### 21. What does immutable mean in the context of programming?
It means it can't be changed after it has been created.

##### 22. What is a **list** in Python?
**Lists** are used to store multiple items in a single variable. They're written inside square brackets. Lists can be used when you need your items ordered, duplicated, or changed.

##### 23. What is a **tuple** in Python?
**Tuples** are used to store multiple items in a single variable. They're written inside round brackets. Tuples can be used when you need your collection ordered and to be unchangeable. 

##### 24. When do you choose a list over a tuple?
You choose a **list** over a **tuple** you need your items to be mutable, have more space, need specific built-in methods, and need to perform operations such as insertion or deletion.

##### 25. How do you get the last value in a list or a tuple?
You can access the index
```sh
data[len(data)-1]
```

##### 26. What is Index Out Of Range Error?
This error occurs when there's an attempt to access elemenets out of range.

##### 27. Why should a program close a file when it is finished using it?
If a program isn't closed after usage, it can occupy memory and potentially cause the program to become very slow. 

##### 28. Assume the names variable references a list of strings. Write code that determines whether 'Dale' is in the names list. If it is, display the message 'Hello Dale'.  Otherwise, display the message 'No Dale'.

```sh
names = ['Dasher', 'Dancer', 'Prancer', 'Vixen', 'Comet', 'Dale', 'Cupid']

if 'Dale' in names:
    print('Hello Dale.')
else:
    print('No Dale.')
```

##### 29. Write a program that opens a specified text file then displays a list of all the unique words found in the file. Hint: Store each word as an element of a set.

```sh
import string
def unique_words(input_filename):

    input_file = open(input_filename, 'r')
    words = list()
 
    for line in input_file:
        line = line.strip()
        line = line.lower()
        line = line.translate(line.maketrans("", "", string.punctuation))
        
        words += line.split(" ")
        uniques = set(words)

        for word in uniques:
            print(str(word))

    input_filename = "file.txt"
    unique_words(input_filename)
```

##### 30. Write a program that reads the contents of a text file. The program should create a dictionary in which the keys are the individual words found in the file and the values are the number of times each word appears. For example, if the word "the" appears 128 times, the dictionary would contain an element with 'the' as the key and 128 as the value. The program should either display the frequency of each word or create a second file containing a list of each word and its frequency.

```sh
import string
def freq_of_words(input_filename):

    input_file = open(input_filename, 'r')
    d = dict()

    for line in input_file:
        line = line.strip()
        line = line.lower()
        line = line.translate(line.maketrans("", "", string.punctuation))
        words = line.split(" ")
  

        for word in words:
            if word in d:
                d[word] = d[word] + 1
            else:
                d[word] = 1
  
    for key in list(d.keys()):
        print(key, ":", d[key])

input_filename = "file.txt"
frequency_of_words(input_filename)
```

# Programming Resources

### Python

+ #### Books

  https://en.wikibooks.org/wiki/Python_Programming

  [How to think like a computer scientist with Python 3][https://www.ict.ru.ac.za/Resources/cspw/thinkcspy3/thinkcspy3.pdf]

  [Python for UNIX/C Programmers][http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=2C4D4757B47E498E04CB1DDDBD4DC9D4?doi=10.1.1.47.4180&rep=rep1&type=pdf]

+ #### Mutable vs Immutable objects

  Super confusing topic that will stay confusing for a while. Go through [this](https://medium.com/@meghamohan/mutable-and-immutable-side-of-python-c2145cf72747) first and then test yourself [here][https://pythonprogramming.net/mutability-learn-python-3-tutorials/?completed=/function-parameters-learn-python-3-tutorials/].

+ #### Search up requirements.txt for python

  ​	TODO

+ #### Global variables in python

  ```python
  a = 15
  
  def change():
      
      # increment a by 5
      a = a + 5
      print(a)
  
  change()
  ```

  This code return an error `UnboundLocalError: local variable 'a' referenced before assignment`. This is because the the variable `a` is not in the scope of the function `change()`. We can mitigate this by using the `global` keyword to access the global variable inside the function.

  ```python
  a = 15
    
  # function to change a global value 
  def change(): 
    
      global a
      
      # increment value of a by 5 
      a = a + 5 
      print(a) 
    
  change() 
  ```

  ***Using `global` is frowned upon in the Python community!***

  Try avoiding it :

- #### Counters

  ```python
  from collections import Counter
  ```

  - subclass of dictionary which stores elements as keys and counts as values
  - does not return key error when key doesn't exist, instead returns 0
  - https://docs.python.org/2/library/collections.html
  
- #### Mulitprocessing

  - https://medium.com/@urban_institute/using-multiprocessing-to-make-python-code-faster-23ea5ef996ba
  - 

### C++

+ #### Namespaces

  Basically defines the scope of the variables/ functions being used. For example:

  ```c++
  using namespace std
      
  int main(){
      cout<<"using the cout function from the std namespace";
      std::cout<<"using the cout function from the std namespace"
  }
  ```

  Here no error is thrown on the first ```cout``` because the ``` namespace std``` was being used. If it wasn't being used, the ```cout``` statement would have to include the `::` operator. 

  Some cool things include - not needing to define the namespace in one file. The same name for a namespace can be used in different parts of the program and they will all be combined together into a single namespace.

  **Useful Links**

  - https://www.tutorialspoint.com/cplusplus/cpp_namespaces.htm
  - https://www.geeksforgeeks.org/namespace-in-c/

+ #### `extern` in C++

  https://www.geeksforgeeks.org/extern-c-in-c/

+ #### exception handling try and catch

  https://www.geeksforgeeks.org/exception-handling-c/

+ #### Google Style Guide

  Should go through this at some point.

  https://google.github.io/styleguide/cppguide.html

### Git

- https://kbroman.org/github_tutorial/pages/init.html

- Oh shit Git

  https://ohshitgit.com/

- **Amazing resource!!**

  https://kiwidamien.github.io/prevent-big-commits.html

  https://kiwidamien.github.io/big-commits-in-github.html

- gitignore

  - https://linuxize.com/post/gitignore-ignoring-files-in-git/
  - 

### Regex

- https://www.debuggex.com/#cheatsheet

## Web Dev

https://css-tricks.com/dom/


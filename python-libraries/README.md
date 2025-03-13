# Python Libraries

A Python library is a collection of pre-written code that you can use to perform specific tasks without writing everything from scratch. Think of a library as a toolbox full of ready-made tools (functions, classes, and modules) that help you build programs more efficiently.

#### Why Use Libraries?

* **Save Time** – Instead of writing everything yourself, you can use libraries that have already been written by experts.
* **Efficient** & Readable– Libraries optimize tasks, making your code run faster and smoother.
* **Easy to Use** – You just need to install and import a library to start using its functions.

#### Types of Python Libraries

1. **Built-in Libraries**

* math – Provides mathematical functions.
* random – Helps in generating random numbers.
* datetime – Handles date and time operations.

2. **External Libraries (Need to be installed separately)**

* numpy – For numerical and scientific computations.
* pandas – For working with datasets.
* matplotlib – For creating graphs and visualizations.
* requests – For making HTTP requests to websites.

#### How to Use a Library?

1. **Import the library** before using it

The format for calling a function from a library follows this structure:

```
library_name.function_name(arguments) #arguments is the input values required by the function 
```

```
#importing nad using the math lib
import math #telling python to install its pre-built library
print(math.sqrt(16)) #output: 4.0

#importing the random lib
import random 
random_number = random.randint(1,10) #calling randint() to get a random number between 1 and 10 
print(random_number)

 #importing datetime lib
import datetime
current_time = datetime.datetime.now() #calling now() function to get current date & time
print(current_time)


```

2. Install external libraries using pip(python package manager). It is a package manager for Python that helps you install, upgrade, and manage external python libraries.&#x20;

```
pip install library_name
```

Libraries can be installed by using the syntax above. Whether the library has been installed can be checked using the below syntax:

* python calls the python interpreter
* -c stands for command mode which allows executing a python command directly from the terminal of the system
* import library\_name imports the library
* print(library\_name.\_\_version\_\_) prints the installed version of the library

```
python -c "import library_name; print(library_name.__version__)"

Example: python -c "import pandas; print(pandas.__version__)"
```

#### Difference between Module, Package and Libraries

1. Module&#x20;

A module is a single python file (.py) containing functions, classes or variables that you can import and use in another python program. A module is just one python file that contains reusable code.&#x20;

```
# math_utils.py (a module)
def add(a, b):
    return a + b

def multiply(a, b):
    return a * b
    
#To use this module in another python file:
import math_utils

print(math_utils.add(3, 5))  # Output: 8
print(math_utils.multiply(4, 6))  # Output: 24
```

2. Package&#x20;

A package is a collection of multiple modules stored in a directory. A package contains  an \_\_init\_\_.py file (which can be empty) to tell python that the folder should be treated as a package.&#x20;

Below example is the package structure (my\_package)

```
my_package/         # Package directory
│── __init__.py     # Defines the package
│── math_utils.py   # A module inside the package
│── string_utils.py # Another module inside the package
```

Modules inside the package: Consider the below packages written together as different python files

<pre><code><strong>#Module 1 - math_utils.py
</strong><strong>def square(n):
</strong>    return n * n
    
#Module 2 - string_utils.py
def greet(name):
    return f"Hello, {name}!"
    
#How to use these different modules in a package
from my_package import math_utils, string_utils

print(math_utils.square(4))  # Output: 16
print(string_utils.greet("Alice"))  # Output: Hello, Alice!
</code></pre>

3. Library

A library is a collection of multiple packages and modules that provide extensive functionalities for different tasks. Libraries can be built-in or external. (Designed for specific functionalities)

### Libraries for PMs

As PMs, having a basic understanding of python libraries can help in analyzing data, automate tasks and make data-driven decisions. The following libraries can be useful:

* Pandas and NumPy are single-purpose libraries which are used for  data processing, whereas matplotlib is a big library with many submodules and since we don't need the whole matplotlib package every time, we import only .pyplot

# Lecture notes for "Programming for Analytics", "Python for Analytics" and "Advanced Python For Data Science." 
This repository contains lecture notes for classes offered by Shahbaz Chaudhary at the University Of Chicago's Masters in Analytics program.

## Class setup
Please follow the instructions below to get your computer ready for this class.

_Note Mac users: Once software is downloaded, if you double click to launch it, you may get permission errors. Try to right click on the downloaded software, pick "open" and continue. (Apple is trying to protect you from accidentally starting malware/virus)_

#### Install Python (anaconda distribution)
Please install Python from this website: https://www.anaconda.com/distribution/
(modern computers are 64 bit so please pick that option)

Mac users:
Accept all default prompts

Windows users:
Accept all default prompts

Anaconda's distribution of Python is widely used in the industry, particularly among data scientists. This distribution makes it easy to use many libraries and packages for data analysis, building models, visualization, etc.

Once installed, please start jupyter notebook and execute code provided below
1. Start `Anaconda Navigator` and click `Launch` on the panel labeled `Jupyter Notebook`
2. Create new notebook from the web interface
3. Execute this code:
```
%%timeit
sum(range(1_000_000))
```
4. Execute this code:
```
from psutil import virtual_memory, disk_usage, cpu_count, os

bytes_in_gb = 1024**3

print("Memory:\t",round(virtual_memory().total/bytes_in_gb,4), "Gigabytes")
print("Disk:\t",round(disk_usage(os.path.abspath(os.sep)).total/bytes_in_gb,4), "Gigabytes")
print("CPUs:\t", cpu_count())
```

#### Clone this repository
1. Visit this web page: https://github.com/falconair/ProgrammingForAnalytics
2. Click "Clone or download" and pick the "Download ZIP" option (unless you already have a GitHub account)

### The following steps are optional
#### Install Git and Git Bash
Please intall Git, a version control sotware, from this website: https://git-scm.com/downloads (you are ok to use default settings)

Note that this is a command-line tool. Once installed, you may not see a new icon to click. We will install a Desktop client to remedy this.

Although we don't make heavy use of version control, you will be introduced to the concept. Installing Git also installs "Git Bash," and comand line environment which simulates Unix/Linux. We will do several exercises which will require this environment.

###### Additional steps:
1. Install a _Graphical_ interface to Git from this website: https://desktop.github.com/
2. [Windows users only] 
  a. type `cd` (this will take you to your home directory)
  b. type `echo cd >> .profile` (this will make sure your home directory is loaded when you start Git Bash)

#### Install Visual Studio Code
Please install Visual Studio Code from https://code.visualstudio.com/

#### Additional steps:
Install Python extensions from https://marketplace.visualstudio.com/items?itemName=ms-python.python (visit that page and click "Install")

========
# Table of Contents
|                           | Module                                                                                                                                  | Class                                                                                                                                                                                             | Description                                                                                                         |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
|                           | [Intro to consoles](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/005_intro_to_consoles)                    | [Intro to consoles](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/005_intro_to_consoles/intro_to_consoles.ipynb)                                                      | This lectures introduces the concept of a console, such as dos cmd or mac terminal, to students                     |
|                           | [Programming vs calculators](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/010_programming_vs_calculator)   | [Programming vs calculator](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/010_programming_vs_calculator/programming_vs_calculator.ipynb)                              | Helps novices understand what features need to be added to a calculator to make it a  fully programming environment |
|                           | [First programs](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/015_first_programs)                          | [First programs](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/015_first_programs/first_programs.ipynb)                                                               | Several examples of small, but full programs which use all common programming constructs and data structures        |
|                           | [Intro to Jupyter](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/020_intro_to_jupyter)                      | [Intro to Jupyter - not technical](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/020_intro_to_jupyter/10%20-%20Intro%20To%20Jupyter%20(not%20technical).ipynb)        | Provides hsitorical context for Jupyter                                                                             |
|                           |                                                                                                                                         | [Intro type Jupyter - technical](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/020_intro_to_jupyter/20%20-%20Intro%20To%20Jupyter%20(technical).ipynb)                | Provides a practioner specific intro to Jupyter                                                                     |
|                           | [All of Python](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/025_all_of_python_basics)                     | [All of Python - faster basics](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/095-all_of_python_faster_basics.ipynb)                         | An overview of Python for computer programmers (multi-week lecture)                                                 |
|                           |                                                                                                                                         | [All of Python - basics](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/100-all_of_python_basics.ipynb)                                       | An overview of Python for novice or non-programmers: teaches programming constructs                                 |
|                           |                                                                                                                                         | [All of Python - variables and tuples](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/110-all_of_python_variable_assignment_and_tuples.ipynb) | Teaches multiple variable assignment                                                                                |
|                           |                                                                                                                                         | [All of Python - basic functions](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/120-all_of_python_basic_functions.ipynb)                     | Introduces functions                                                                                                |
|                           |                                                                                                                                         | [All of Python - numbers](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/130-all_of_python_numbers.ipynb)                                     | Overview of numbers and related operations                                                                          |
|                           |                                                                                                                                         | [All of Python - strings](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/140-all_of_python_basic_strings.ipynb)                               | Overview of strings and related operations                                                                          |
|                           |                                                                                                                                         | [All of Python - Boolean algebra](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/145-all_of_python_basics_boolean_algebra.ipynb)              | Dives deeper into the world of comparisons, and/or/not                                                              |
|                           |                                                                                                                                         | [All of Python - basic plotting](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/150-all_of_python_basic_plotting.ipynb)                       | General matlab intro (not recommended for novices)                                                                  |
|                           |                                                                                                                                         | [All of Python - dictionaries](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/170-all_of_python_dictionaries.ipynb)                           | Introduces Python dictionaries (aka maps, associative arrays)                                                       |
|                           |                                                                                                                                         | [All of Python - lists](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/180-all_of_python_lists.ipynb)                                         | Teaches lists                                                                                                       |
|                           |                                                                                                                                         | [All of Python - comprhensions](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/190-all_of_python_comprehensions.ipynb)                        | Teaches list and dictionary comprehensions (useful but intermediate feature)                                        |
|                           |                                                                                                                                         | [All of Python - basic classes](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/200-all_of_python_basic_classes.ipynb)                         | Introduces classes and the very basics of object oriented programming                                               |
|                           |                                                                                                                                         | [All of Python - loops](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/210-all_of_python_loops.ipynb)                                         | Describes while and for loops                                                                                       |
|                           |                                                                                                                                         | [All of Python - conditionals and None](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/220-all_of_python_basic_conditonals_and_None.ipynb)    | Deeper dive into if/else conditions and Python's None type                                                          |
|                           |                                                                                                                                         | [All of Python - function arguments](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/230-all_of_python_functions_argument_types.ipynb)         | Deeper dive into functions, including optional parameters                                                           |
|                           |                                                                                                                                         | [All of Python - lambda functions](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/240-all_of_python_functions_lambda.ipynb)                   | Introduces anaonymous functions (aka lambda functions)                                                              |
|                           |                                                                                                                                         | [All of Python - recursive functions](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/250-all_of_python_functions_recursion.ipynb)             | Introduces the world of functions themselves                                                                        |
|                           |                                                                                                                                         | [All of Python - regexes](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/260-all_of_python_regexes.ipynb)                                     | A very basic intro to regular expressions                                                                           |
|                           | [Intro to Numpy](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/045_intro_to_numpy)                          | [Numpy quick start](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/045_intro_to_numpy/intro_to_numpy.ipynb)                                                            | A broad overview of Numpy                                                                                           |
|                           | [Intro to Pandas](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/030_intro_to_pandas)                        | [Pandas - quick start](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/100-pandas_quick_start.ipynb)                                                | A broad overview of Pandas                                                                                          |
|                           |                                                                                                                                         | [Pandas - Series](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/110-pandas-overview-series.ipynb)                                                 | A deeper dive into Pandas Series                                                                                    |
|                           |                                                                                                                                         | [Pandas - Dataframes](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/120-pandas-overview-dataframes.ipynb)                                         | Build up a dataframe using a collection of Series or a Numpy matrix, shows basic functioanality                     |
|                           |                                                                                                                                         | [Pandas - general operations](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/130-pandas-dataframes-operations.ipynb)                               | Introduces additional dataframe operations                                                                          |
|                           |                                                                                                                                         | [Pandas -  combining: merge, join, concat](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/140-pandas-dataframes-combining.ipynb)                   | Shows how to combine multiple dataframes, similar to SQL joins                                                      |
|                           |                                                                                                                                         | [Pandas - groupby](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/150-pandas-groupby.ipynb)                                                        | Show how to break a population into subgroups and find aggregates for those subgroups                               |
|                           |                                                                                                                                         | [Pandas - Index](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/160-pandas-index.ipynb)                                                            | Does a deep dive into Pandas indexes, a topic often not known to casual Pandas users                                |
|                           |                                                                                                                                         | [Pandas - reshape, pivot, melt, stack](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/170-pandas-reshape-with-pivot-melt-stack.ipynb)              | Shows how to convert columns to rows and back, features similar to Excel's pivot table or cub rollup analysis       |
|                           |                                                                                                                                         | [Pandas - operations: str, dt, apply](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/180-pandas-operations_str_dt_apply.ipynb)                     | Shows how to apply string or date functions to Pandas series                                                        |
|                           | [Scikit learn](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/070_scikit_learn)                              | [Scikit Learn - method behind the madness](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/070_scikit_learn/100-scikit-learn-method_behind_the_madness.ipynb)           | Describes Scikit learn's architecture and introduces pipes                                                          |
|                           |                                                                                                                                         | [Scikit Learn - Run saved models](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/070_scikit_learn/110-scikit-learn-run_saved_model.ipynb)                              | Shows how to connect SKLearn models to the web (very basic)                                                         |
|                           | [Secret lives of text files](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/065_secret_lives_of_text_files)  | [Secret lives of text files](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/065_secret_lives_of_text_files/Secret%20Lives%20of%20Text%20Files.ipynb)                   | Describes encodings (UTF, ASCII), multi-byte characters, special characters such as \\n and \\t, etc.               |
|                           | [How to read technical docs](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/035_how_to_read_technical_docs)  | [How to read technical docs](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/035_how_to_read_technical_docs/how_to_read_technical_docs.ipynb)                           |                                                                                                                     |
|                           | [Basic computer archtecture](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/040_basic_computer_architecture) | [Basic computer architecture](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/040_basic_computer_architecture/basic_computer_architecture.ipynb)                        | Provides a broad overview of a CPU, registers, floating points vs integers, disk vs memory speed differences        |
|                           |                                                                                                                                         |                                                                                                                                                                                                   |                                                                                                                     |
|                           |                                                                                                                                         |                                                                                                                                                                                                   |                                                                                                                     |
| Python for Analytics      | [First programs](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/015_first_programs)                          | [First programs](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/015_first_programs/first_programs.ipynb)                                                               | Several examples of small, but full programs which use all common programming constructs and data structures        |
|                           | [Intro to Jupyter](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/020_intro_to_jupyter)                      | [Intro to Jupyter - not technical](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/020_intro_to_jupyter/10%20-%20Intro%20To%20Jupyter%20(not%20technical).ipynb)        | Provides hsitorical context for Jupyter                                                                             |
|                           |                                                                                                                                         | [Intro type Jupyter - technical](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/020_intro_to_jupyter/20%20-%20Intro%20To%20Jupyter%20(technical).ipynb)                | Provides a practioner specific intro to Jupyter                                                                     |
|                           | [All of Python](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/025_all_of_python_basics)                     | [All of Python - faster basics](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/095-all_of_python_faster_basics.ipynb)                         | An overview of Python for computer programmers (multi-week lecture)                                                 |
|                           | [Intro to Numpy](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/045_intro_to_numpy)                          | [Numpy quick start](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/045_intro_to_numpy/intro_to_numpy.ipynb)                                                            | A broad overview of Numpy                                                                                           |
|                           | [Intro to Pandas](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/030_intro_to_pandas)                        | [Pandas - quick start](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/100-pandas_quick_start.ipynb)                                                | A broad overview of Pandas                                                                                          |
|                           |                                                                                                                                         | [Pandas - Series](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/110-pandas-overview-series.ipynb)                                                 | A deeper dive into Pandas Series                                                                                    |
|                           |                                                                                                                                         | [Pandas - Dataframes](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/120-pandas-overview-dataframes.ipynb)                                         | Build up a dataframe using a collection of Series or a Numpy matrix, shows basic functioanality                     |
|                           |                                                                                                                                         | [Pandas - general operations](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/130-pandas-dataframes-operations.ipynb)                               | Introduces additional dataframe operations                                                                          |
|                           |                                                                                                                                         | [Pandas -  combining: merge, join, concat](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/140-pandas-dataframes-combining.ipynb)                   | Shows how to combine multiple dataframes, similar to SQL joins                                                      |
|                           |                                                                                                                                         | [Pandas - groupby](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/150-pandas-groupby.ipynb)                                                        | Show how to break a population into subgroups and find aggregates for those subgroups                               |
|                           |                                                                                                                                         | [Pandas - Index](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/160-pandas-index.ipynb)                                                            | Does a deep dive into Pandas indexes, a topic often not known to casual Pandas users                                |
|                           |                                                                                                                                         | [Pandas - reshape, pivot, melt, stack](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/170-pandas-reshape-with-pivot-melt-stack.ipynb)              | Shows how to convert columns to rows and back, features similar to Excel's pivot table or cub rollup analysis       |
|                           |                                                                                                                                         | [Pandas - operations: str, dt, apply](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/180-pandas-operations_str_dt_apply.ipynb)                     | Shows how to apply string or date functions to Pandas series                                                        |
|                           | [Scikit learn](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/070_scikit_learn)                              | [Scikit Learn - method behind the madness](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/070_scikit_learn/100-scikit-learn-method_behind_the_madness.ipynb)           | Describes Scikit learn's architecture and introduces pipes                                                          |
|                           |                                                                                                                                         | [Scikit Learn - Run saved models](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/070_scikit_learn/110-scikit-learn-run_saved_model.ipynb)                              | Shows how to connect SKLearn models to the web (very basic)                                                         |
|                           |                                                                                                                                         |                                                                                                                                                                                                   |                                                                                                                     |
|                           |                                                                                                                                         |                                                                                                                                                                                                   |                                                                                                                     |
| Programming for Analytics | [Programming vs calculators](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/010_programming_vs_calculator)   | [Programming vs calculator](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/010_programming_vs_calculator/programming_vs_calculator.ipynb)                              | Helps novices understand what features need to be added to a calculator to make it a  fully programming environment |
|                           | [First programs](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/015_first_programs)                          | [First programs](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/015_first_programs/first_programs.ipynb)                                                               | Several examples of small, but full programs which use all common programming constructs and data structures        |
|                           | [Intro to Jupyter](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/020_intro_to_jupyter)                      | [Intro to Jupyter - not technical](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/020_intro_to_jupyter/10%20-%20Intro%20To%20Jupyter%20(not%20technical).ipynb)        | Provides hsitorical context for Jupyter                                                                             |
|                           |                                                                                                                                         | [Intro type Jupyter - technical](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/020_intro_to_jupyter/20%20-%20Intro%20To%20Jupyter%20(technical).ipynb)                | Provides a practioner specific intro to Jupyter                                                                     |
|                           | [All of Python](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/025_all_of_python_basics)                     | [All of Python - basics](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/025_all_of_python_basics/100-all_of_python_basics.ipynb)                                       | An overview of Python for novice or non-programmers: teaches programming constructs                                 |
|                           | [Secret lives of text files](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/065_secret_lives_of_text_files)  | [Secret lives of text files](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/065_secret_lives_of_text_files/Secret%20Lives%20of%20Text%20Files.ipynb)                   | Describes encodings (UTF, ASCII), multi-byte characters, special characters such as \\n and \\t, etc.               |
|                           | [How to read technical docs](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/035_how_to_read_technical_docs)  | [How to read technical docs](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/035_how_to_read_technical_docs/how_to_read_technical_docs.ipynb)                           |                                                                                                                     |
|                           | [Basic computer archtecture](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/040_basic_computer_architecture) | [Basic computer architecture](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/040_basic_computer_architecture/basic_computer_architecture.ipynb)                        | Provides a broad overview of a CPU, registers, floating points vs integers, disk vs memory speed differences        |
|                           | [Intro to Numpy](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/045_intro_to_numpy)                          | [Numpy quick start](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/045_intro_to_numpy/intro_to_numpy.ipynb)                                                            | A broad overview of Numpy                                                                                           |
|                           | [Intro to Pandas](https://github.com/falconair/ProgrammingForAnalytics/tree/master/lectures/030_intro_to_pandas)                        | [Pandas - quick start](https://github.com/falconair/ProgrammingForAnalytics/blob/master/lectures/030_intro_to_pandas/100-pandas_quick_start.ipynb)                                                | A broad overview of Pandas                                                                                          |
|                           | Lectures on R omitted                                                                                                                   |                                                                                                                                                                                                   |                                                                                                                     |

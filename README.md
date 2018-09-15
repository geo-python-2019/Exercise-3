# Exercise-3

The exercise for this week is meant to help you to understand `for` loops and conditional statements in Python.
Below you have a series of problems in which you are asked to edit the notebook files and write the code necessary to produce the desired results.

After making your changes to the Notebook, you will need to upload it to GitHub.

- **Exercise 3 is due by the start of lecture on 26.9**.

- Don't forget to check out the [hints for this week's exercise](https://geo-python.github.io/2018/lessons/L3/exercise-3-hints.html) if you're having trouble.

- Scores on this exercise are out of **20 points** that you get by finishing all 3 problems.

### Contents

1. [Preparations before starting](#before-starting)
2. [Problem 1 - Batch processing data files with a for loop](#problem-1---batch-processing-data-files-with-a-for-loop-4-points)
3. [Problem 2 - Classifying temperatures](#problem-2---classifying-temperatures-8-points)
4. [Problem 3 - Allocating locations](#problem-3---allocating-locations-8-points)
5. [Problem 4 (optional) - Nested `for` loops](#extra-problem---nested-for-loops-optional-does-not-affect-grading)


## Before starting

### Test that your IPython is up-to-date

Our automatic grading system requires to have IPython version which is higher than 3. Test your version by running following cell (shift + Enter) in JupyterLab:

```python

import IPython
assert IPython.version_info[0] >= 3, "Your version of IPython is too old, please update it. Ask help, if you don't know how."
print("Your system is okay, you can continue! :) ")

```

### Clone Exercise repository to JupyterLab

Before starting to work with the actual problems for this week, you should start a new JupyterLab instance and clone your own Exercise 3 repository (e.g. htenkanen-exercise-3) into the instance using Git as we saw in the [**lecture**](https://geo-python.github.io/2018/lessons/L2/git-basics.html#clone-a-repository-from-github) during week 2.


## Problem 1 - Batch processing data files with a for loop (*4 Points*)

### Overview

This problem is meant to simulate a common problem dealing with data files: batch processing.

Batch processing involves using scripts to process many data files, and one common task is generating a list of filenames that will be processed, or saved to disk.

### Start assignment

Start working on Problem 1 by opening [**Exercise-3-problem-1.ipynb**](Exercise-3-problem-1.ipynb) in JupyterLab. 

#### Your score on this problem will be based on following criteria:

 - Creating and using variables to produce the desired text format
 - Successfully using for loop to iterate over desired set of numbers
 - Successfully producing the desired filename
 - Including comments that explain what most lines in the code do
 - Replying to a couple of questions we ask at the end of the assignment
 - Uploading your notebook to your GitHub repository for this week's Exercise

## Problem 2 - Classifying temperatures (*8 points*)

### Overview

This problem is meant to introduce you to a very commonly used and useful concept of data classification.
In this problem your aim is to classify daily temperatures stored in `temperatures` list into four different classes:

  1. **Cold** ==> temperatures below -2 degrees (Celsius)
  2. **Slippery** ==> temperatures warmer or equal to -2 degrees and up to +2 degrees (Celsius)
  3. **Comfortable** ==> temperatures warmer or equal to +2 degrees and up to +15 degrees (Celsius)
  4. **Warm** ==> temperatures warmer or equal to +15 degrees (Celsius)

To solve this problem, you should modify and fill in the missing parts in the cells.
In total, there are three tasks that you should solve according the directions. In addition, there is
one additional task (Task 4) that is **optional** for the students that are quicker (*does not affect grading*).

### Start assignment

Start working on Problem 2 by opening [**Exercise-3-problem-2.ipynb**](Exercise-3-problem-2.ipynb) in JupyterLab. 

#### Your score on this problem will be based on following criteria:

 - Using for loop to iterate over the temperature values
 - Using conditional statements to find out if a value is within certain value range
 - Printing information for the user
 - Including comments that explain what most lines in the code do
 - Replying to a couple of questions we ask at the end of the assignment
 - Uploading your Notebook to your GitHub repository for this week's Exercise.
 
 
## Problem 3 - Allocating locations (*8 points*)


### Overview 
Following map shows the locations of the weather stations (as blue points) in Finland that are more than 70 years old [1].
In this problem we are interested to find out whether the station network was equally distributed across Finland
seventy years ago. We have divided Finland into four geographical zones (i.e. North West, North East, South West, South East)
according the approximate center point of Finnish mainland located at `26.3, 64.5` (lon-lat in decimal degrees).

![](img/FMI_stations_70_years_older.png)

[1]: The locations and the age of weather stations were obtained from: http://en.ilmatieteenlaitos.fi/observation-stations

Below, we have given you the coordinates of 34 weather stations.
The location of a single station is determined with a pair of latitude and longitude coordinates.
The coordinates of all the stations are separated into two lists (`lat` and `lon`) and the names of the stations are in `stations` list. From these lists, you would get e.g. the location of the first station by combining the latitude and longitude coordinates from coordinate lists, and the name of that station from `stations` list at index[0]:

### Problem statement

In this problem your job is to print the names of weather stations located in different zones. **Optionally** you should also report the share of weather stations that allocated to each zone that could be used to evaluate if certain zone was over/under-represented seventy years ago (optional task, does not affect on grading).

To solve this problem, you should modify and fill in the missing parts in the code cells below.

### Start assignment

Start working on Problem 3 by opening [**Exercise-3-problem-3.ipynb**](Exercise-3-problem-3.ipynb) in JupyterLab. 

#### Your score on this problem will be based on following criteria:

 1. Create four lists for geographical zones in Finland (i.e. `nort_west`, `north_east`, `south_west`, `south_east`)
 2. Iterate over values and determine to which geographical zone the station belongs
    1. Hint: You should create a loop that iterates `N` -number of times. Create a variable *`N`* that should contain the number of stations we have here.
    2. You should use a conditional statement to find out if the latitude coordinate of a station is either North or South of the center point of Finland (`26.3, 64.5`) **AND** if the longitude location is West or East from that center point.
    3. You should insert the name of the station into the correct geographical zone list (step 1)
 3. Print out the names of stations at each geographical zone
 4. Reply to a couple of questions we ask at the end of the assignment
 5. **Optional:** Calculate and print the share of stations at each zone (the total number of stations equals to 100 %)
 

## Extra Problem - Nested `for` loops (optional, does not affect grading)

**Warning:** This is a difficult problem. Try to do this task only if you have confidence in programming, and you are up for a little challenge. :) 

In addition to having single `for` loops that iterate across some variable range, it is possible to *nest* `for` loops within one another.

Consider the example below:

```python
>>> for char in 'dog':
...     for char2 in 'cat':
...         print (char, char2)
    d c
    d a
    d t
    o c
    o a
    o t
    g c
    g a
    g t
```

Here, you can see that in the first pass through the first `for` loop, the value of `char` is `d`.
Entering the inner (or nested) loop, `char2` is set to `c`.
After this, the output is written to the screen and since there are more letters to loop over in the inner `for` loop, the value of `char2` will be updated upon the next pass.
The second time through the inner loop, `char2` is set to `a` while `char` remains `d`.
Like this, the inner loop will run through all of the letters in `cat` for each time that `char` is updated in the outer loop.
It doesn't take too much imagination to figure out this is a very useful concept.

For this problem you should do following:

1. Create a variable `star` with text `"*"` and an empty string variable `text`. Recall, you can created empty string variables by assigning `""` as their value.
2. Use nested `for` loops and the variables above to produce the text formation below when `print(text)` is run at the end of your script.

    ```
    *******
    *******
    *******
    ```
3. Create a variable `line` with text `"-"` and an empty string variable `flag`.
4. Use nested `for` loops and the variables above to produce the text formation below when `print(flag)` is run at the end of your script. **Note**: You will need to use conditional statements to produce the desired output.

    ```
    *******------------
    *******------------
    *******------------
    -------------------
    -------------------
    ```
       
    
### Start assignment (optional)

Start working on Problem 4 (optional) by opening [**Exercise-3-problem-4.ipynb**](Exercise-3-problem-4.ipynb) in JupyterLab. 

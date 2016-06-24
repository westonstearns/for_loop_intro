---
title       : For loops
description : A brief intro to writing for loops

--- type:NormalExercise lang:r xp:100 skills:1 key:e20287ea44
## For loop

In this tutorial we will have a look at how you can write a basic for loop in R. It is aimed at beginners, and if you’re not yet familiar with the basic syntax of the R language we recommend you to first have a look at this <a href = "https://www.datacamp.com/courses/free-introduction-to-r">introductory R tutorial</a>.

Conceptually, a loop is a way to repeat a sequence of instructions under certain conditions. They allow you to automate parts of your code that are in need of repetition. 

Suppose you want to make several printouts of the following form: The year is [year] where [year] is equal to 2010, 2011, up to 2016. 

The following exercises will walk you through step by step.

Let's begin by printing the form manually. 

*** =instructions
- Use `print()`, `paste()` and the combination of the text string `"The year is"` and a numerical year to achve the desired print outs
- Your code should follow the format ```print(paste("Text",Year))```


*** =hint
- There should be a total of 7 lines of code

*** =pre_exercise_code
```{r}

```

*** =sample_code
```{r}
# Print out the 7 text stirngs
# 2010
print(paste(___, ___))

# 2011
___(___("___", ___))

# 2012
___(___("___", ___))

# 2013
___(___("___", ___))

# 2014
___(___("___", ___))

# 2015
___(___("___", ___))

# 2016
___(___("___", ___))

```

*** =solution
```{r}
# Print out the 7 text strings
# 2010
print(paste("The year is", 2010))

# 2011
print(paste("The year is", 2011))

# 2012
print(paste("The year is", 2012))

# 2013
print(paste("The year is", 2013))

# 2014
print(paste("The year is", 2014))

# 2015
print(paste("The year is", 2015))

# 2016
print(paste("The year is", 2016))

```

*** =sct
```{r}
# SCT written with testwhat: https://github.com/datacamp/testwhat/wiki

test_output_contains('print(paste("The year is", 2010))', incorrect_msg = 'Your output did not contain `"The year is 2010"`, look at the instructions for help.')

test_output_contains('print(paste("The year is", 2011))', incorrect_msg = 'Your output did not contain `"The year is 2011"`, look at the instructions for help. ')

test_output_contains('print(paste("The year is", 2012))', incorrect_msg = 'Your output did not contain `"The year is 2012"`, look at the instructions for help.')

test_output_contains('print(paste("The year is", 2010))', incorrect_msg = 'Your output did not contain `"The year is 2013"`, look at the instructions for help.')

test_output_contains('print(paste("The year is", 2010))', incorrect_msg = 'Your output did not contain `"The year is 2014"`, look at the instructions for help.')

test_output_contains('print(paste("The year is", 2010))', incorrect_msg = 'Your output did not contain `"The year is 2015"`, look at the instructions for help.')

test_output_contains('print(paste("The year is", 2010))', incorrect_msg = 'Your output did not contain `"The year is 2016"`, look at the instructions for help.')

test_function("print", 
              args = NULL, index = 1, 
              not_called_msg = "Did you remember to include the `print` function?", 
              args_not_specified_msg = "The `print` function doesn't have the correct arguments.", 
              incorrect_msg = "The `print` function is not correct. Look at the instructions for help!")
test_function("print", 
              args = NULL, index = 2, 
              not_called_msg = "Did you remember to include the `print` function?", 
              args_not_specified_msg = "The `print` function doesn't have the correct arguments.", 
              incorrect_msg = "The `print` function is not correct. Look at the instructions for help!")
test_function("print", 
              args = NULL, index = 3, 
              not_called_msg = "Did you rremember to include the `print` function?", 
              args_not_specified_msg = "The `print` function doesn't have the correct arguments.", 
              incorrect_msg = "The `print` function is not correct. Look at the instructions for help!")
test_function("print", 
              args = NULL, index = 4, 
              not_called_msg = "Did you remember to include the `print` function?", 
              args_not_specified_msg = "The `print` function doesn't have the correct arguments.", 
              incorrect_msg = "The `print` function is not correct. Look at the instructions for help!")
test_function("print", 
              args = NULL, index = 5, 
              not_called_msg = "Did you remember to include the `print` function?", 
              args_not_specified_msg = "The `print` function doesn't have the correct arguments.", 
              incorrect_msg = "The `print` function is not correct. Look at the instructions for help!")
test_function("print", 
              args = NULL, index = 6, 
              not_called_msg = "Did you remember to include the `print` function?", 
              args_not_specified_msg = "The `print` function doesn't have the correct arguments.", 
              incorrect_msg = "The `print` function is not correct. Look at the instructions for help!")
test_function("print", 
              args = NULL, index = 7, 
              not_called_msg = "Did you remember to include the `print` function?", 
              args_not_specified_msg = "The `print` function doesn't have the correct arguments.", 
              incorrect_msg = "The `print` function is not correct. Look at the instructions for help!")


test_error(incorrect_msg = "Fill in the blank spaces with R code. Follow the example in the instrucitons and simply add the desired text and a year")
success_msg("Good work!")
```

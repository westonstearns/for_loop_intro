---
title       : For loops
description : A brief intro to writing for loops

--- type:NormalExercise lang:r xp:100 skills:1 key:e20287ea44
## Manual Print

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

test_output_contains('print(paste("The year is", 2013))', incorrect_msg = 'Your output did not contain `"The year is 2013"`, look at the instructions for help.')

test_output_contains('print(paste("The year is", 2014))', incorrect_msg = 'Your output did not contain `"The year is 2014"`, look at the instructions for help.')

test_output_contains('print(paste("The year is", 2015))', incorrect_msg = 'Your output did not contain `"The year is 2015"`, look at the instructions for help.')

test_output_contains('print(paste("The year is", 2016))', incorrect_msg = 'Your output did not contain `"The year is 2016"`, look at the instructions for help.')

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

--- type:NormalExercise lang:r xp:100 skills:1  key:099f1482c3
## For() loop

You immediately see this is rather tedious: you repeat the same code chunk over and over. 

This violates the DRY principle, known in every programming language: Don’t Repeat Yourself, at all cost. 

In this case, by making use of a for loop in R, you can automate the repetitive part:

```for (variable in c(sequence)){```
<p>```print(paste("Text", number))```</p>
<p>```}```</p>

*** =instructions
- Use a `for()` loop to print out the list of 7 phrases.


*** =hint
- Make sure the for loop {} are closed!

*** =pre_exercise_code
```{r}

```

*** =sample_code
```{r}
# Write for loop here
for (___ in c(___,___,___,___,___,___,___)){
  print(paste("The year is", year))
}

```

*** =solution
```{r}
# Write for loop here
for (year in c(2010,2011,2012,2013,2014,2015,2016)){
  print(paste("The year is", year))
}


```

*** =sct
```{r}
test_for_loop(index = 1, 
              cond_test = test_student_typed("year in c(2010,2011,2012,2013,2014,2015,2016)", 
                      not_typed_msg = "Make sure you use ```year in c(2010,2011,2012,2013,2014,2015,2016)``` to define your for loop."),
              not_found_msg = "Did you run your `for()` loop.")

test_output_regex("The year is 201[0-6]{1}",
                  incorrect_msg = "You didn't print out all of the text forms. Make sure all the years are included.")

test_error()
success_msg("Good work!")
```

--- type:NormalExercise lang:r xp:100 skills:1  key:ba6e1a41f2
## For() loop improved

You can even simplify the code even more: <p>```c(2010,2011,2012,2013,2014,2015,2016)```</p> <p>can also be written as `2010:2016`;</p> this creates the exact same sequence. 



*** =instructions
- Replace the ```c(2010,2011,2012,2013,2014,2015,2016)``` with `2010:2016`.

*** =hint
- Make sure the for loop {} are closed!

*** =pre_exercise_code
```{r}

```

*** =sample_code
```{r}
# Write for loop here
for (___ in c(___:___)){
  print(paste("The year is", year))
}

```

*** =solution
```{r}
# Write improved for loop here
for (year in c(2010:2016)){
  print(paste("The year is", year))
}

```

*** =sct
```{r}
test_for_loop(index = 1, 
              cond_test = test_student_typed("year in c(2010:2016)", 
                      not_typed_msg = "Make sure you use ```year in c(2010:2016)``` to define your for loop."),
              not_found_msg = "Did you run your `for()` loop.")

test_output_regex("The year is 201[0-6]{1}",
                  incorrect_msg = "You didn't print out all of the text forms. Make sure all the years are included.")

test_error()
success_msg("Good work!")
```

--- type:NormalExercise lang:r xp:100 skills:1  key:aa6c7aff9d
## If statements

You can further refine the for loop with `if` statements. This allows you to add conditions varrying the output of your loop. 

Here you will ad an `if` statement restricting the output to just even years.

An `if` statement follows the following pattern,
```

```

*** =instructions
- Ad the `if` command to the for loop
- Use the modulo division operator to resrict the out put to even years

*** =hint
- Make sure the for loop {} are closed!

*** =pre_exercise_code
```{r}

```

*** =sample_code
```{r}
# Write for loop here
for (___ in c(___:___)){
  print(paste("The year is", year))
}

```

*** =solution
```{r}
# Write improved for loop here
for (year in c(2010:2016)){
if(year %% 2 == 0)
  print(paste("The year is", year))
}
```

*** =sct
```{r}
test_for_loop(index = 1, 
              cond_test = test_student_typed("year in c(2010:2016)", 
                      not_typed_msg = "Make sure you use ```year in c(2010:2016)``` to define your for loop."),
              not_found_msg = "Did you run your `for()` loop.")

test_output_regex("The year is 2010|The year is 2012|The year is 2014",
                  incorrect_msg = "You didn't print out all of the text forms. Make sure all the years are included.")

test_error()
success_msg("Good work!")
```




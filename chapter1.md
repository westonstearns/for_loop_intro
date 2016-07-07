---
title       : For loops
description : A brief intro to writing for loops

--- type:NormalExercise lang:r xp:100 skills:1 key:e20287ea44
## Manual Print

In this tutorial we will have a look at how you can write a basic for loop in R. It is aimed at beginners, and if you’re not yet familiar with the basic syntax of the R language we recommend you to first have a look at this <a href = "https://www.datacamp.com/courses/free-introduction-to-r">introductory R tutorial</a>.

Conceptually, a loop is a way to repeat a sequence of instructions under certain conditions. They allow you to repeat parts of your code. 

Suppose you want to make several printouts of the following form: The year is [year], where [year] is equal to 2010, 2011, up to 2016. 

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

```
for (variable in c(sequence)){ 
    print(paste("Text", number))}
```

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

The last exercise shows the value of a for loop when you need to print out many forms of the same string. The higher the number of outputs the more useful the loop is. Imagin printing thousands of lines manually. It would be far too time consuming to complete. 

Nonetheless, there are still ways we can improve our loop.

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

Not that you've seen the basic syntax for a loop, there are other ways you can manipulate or refine the outputs of the loop.

You can further refine the for loop with `if` statements. This allows you to add conditions varrying the output of your loop. 

Here you will ad an `if` statement restricting the output to just even years.

An `if` statement follows the following pattern,
```
if(condition)
    expression
```
An `else` condition can be added detailing what to do given the `if` condition is not satisfied,
```
if(condition)
    expression
    else
      expression
```

*** =instructions
- Complete the `if` command to the for loop but adding a `2 == 0` after the modulus division operator `%%`. 
- Note: The `%%` operator finds the remainder following the division of two numbers. In this case the `year` is being divided by `2` so any even year would have a remainder of `0` or `%% 2 == 0`.

*** =hint
- Make sure the for loop {} are closed!

*** =pre_exercise_code
```{r}

```

*** =sample_code
```{r}
# Write for loop here

for (___ in c(___:___)){
if(year %% ____ )
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

test_output_regex("The year is 2010|The year is 2012|The year is 2014|The year is 2016",
                  incorrect_msg = "You didn't print out all of the text forms. Make sure all the years are included.")

test_or(test_output_contains("The year is 2010"),
        test_output_contains("The year is 2012"),
        test_output_contains("The year is 2014"),
        incorrect_msg = "Just print out the even years.")                                                                                                                                      
test_output_contains("The year is 2012",
                  incorrect_msg = "You didn't print out all of the text forms. Make sure all the years are included.")
test_output_contains("The year is 2014",
                  incorrect_msg = "You didn't print out all of the text forms. Make sure all the years are included.")
test_output_contains("The year is 2016",
                  incorrect_msg = "You didn't print out all of the text forms. Make sure all the years are included.")

test_error()
success_msg("Good work!")
```

--- type:NormalExercise lang:r xp:100 skills:1  key:8574335401
## For() loop application 

Now you have seen a few of the possibilities of the for loop, however, there are many more useful applications for the for loop than to print out a series of repeated strings telling you what year it is. 

One applicaiton that is seen quite often is using a loop to simulate data or events. So let's give that a try.

A function `modified_war` was created that simulates a the card game war. If you are not familiar with this game is it quite simple. a full deck of cards are shuffeled and divied between two players. The two players do not look at their cards and simply draw the top card in their stack revealing its value, whichever player has the highest card wins that round. 

If the two players draw cards of the same value that is called war! They then draw three cards which are discarded and then the fourth card decides the winner of the "war" round. The winner collects both cards adding to their stack. The game continues until one player is out of cards!

The `modified_war()` function creates a vitrual deck of cards, shuffels it and then deals the cards to two hypothetical players. Then it exectues the game collecting the winner of each round and whether the round was a "war". The function collects the results of the game for 26 rounds. 

We can use this fucntion to simulate as many games as we would like and calculate the porportion of each player winning and the proportion of "wars".

*** =instructions
- Use a `for()` loop to simulate 1000 games.
- Print a table of one of the results.

*** =hint
- Make sure the for loop {} are closed!

*** =pre_exercise_code
```{r}
modified_war <- function(){
  
  # Creating cards
  deck_of_cards <- rep(2:14,4)
  shuffled_cards <- sample(deck_of_cards,52,replace = FALSE)
  odds <- c(1:52)[c(T,F)]
  sallys_cards <- shuffled_cards[odds]
  evens <- c(1:52)[c(F,T)]
  timmys_cards <- shuffled_cards[evens]
  
  # game results
  results_vector <- vector("numeric", 26)
  for(i in 1:26) {
    results <- sallys_cards[i] == timmys_cards[i]
    if(results == FALSE){
      if(sallys_cards[i] > timmys_cards[i]){
        results_vector[i] <- c("Sally wins")
      } else{
        results_vector[i] <- c("Timmy wins")
      }
    }
    if(results == TRUE){
      if(i+5 > 25){
        results_vector[i] <- c("War")
        next
      }
      results <- sallys_cards[i+4] == timmys_cards[i+4]
      if(results == TRUE){
        results_vector[i] <- c("War")
      } else{
        results_vector[i] <- c("War")
      }
    }
  }
  results_vector
}

```

*** =sample_code
```{r}
# Simulate 1000 games of war

# Print a table of one of the results


```

*** =solution
```{r}
# Simulate 1000 games of war
war_sim <- vector("list",1000)
#
# run a 100 iteration simulation of a modified game a war
for (i in 1:1000)
{
  war_sim[[i]] <- modified_war()
}

# Print a table of one of the results
table(war_sim[1])

```

*** =sct
```{r}

test_error()
success_msg("Good work!")
```

--- type:NormalExercise lang:r xp:100 skills:1  key:ab048a3807
## For() loop application 

You completed the simulation of 1000 games of war. Now take a look at the results. If you want to find the the proportions of wins by each player and the number of "war" rounds, you first need to count the number of each outcome. 

Follow the inctructions to count the different outcome types and then calculate the three proportions. 

*** =instructions
- Use thee the number of wars in the simulated games.
- Calculate the proprotion of wins by Sally. 
- Calculate the proprotion of wins by Timmy.
- Calculate the proportion of wars.


*** =hint
- Make sure the for loop {} are closed!

*** =pre_exercise_code
```{r}
load(url(...))
```

*** =sample_code
```{r}
# Count the number of wars in the simulated games

# Calculate the proprotion of wins by Sally

# Calculate the proprotion of wins by Timmy

# Calculate the proportion of wars


```

*** =solution
```{r}
# Counting the number of wars in the simulated games
wars <- unlist(regmatches(unlist(war_sim),gregexpr("War",unlist(war_sim),perl = TRUE)))
Sally_wins <- unlist(regmatches(unlist(war_sim),gregexpr("Sally wins",unlist(war_sim),perl = TRUE)))
Timmy_wins <- unlist(regmatches(unlist(war_sim),gregexpr("Timmy wins",unlist(war_sim),perl = TRUE)))

# Calculate the proprotion of wins by Sally

# Calculate the proprotion of wins by Timmy

# Calculate the proportion of wars




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


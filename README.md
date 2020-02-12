# STA 323 :: Homework 3

## Introduction

The stop-question-and-frisk (sqf) program, in New York City, is a practice of 
temporarily detaining, questioning, and at times searching civilians and 
suspects. In 2011, the program peaked with a total of 685,724 sqf events.

The NYPD contains data records on every sqf event throughout the program's
history. In this exam we will work with the 2011 sqf data. 
All yearly data and more information about the stop-question-and-frisk 
program can be found at 
https://www1.nyc.gov/site/nypd/stats/reports-analysis/stopfrisk.page.

## Data

To get started, read in the data. Each row represents a single sqf event in 
2011. This code is provided in your `hw3.Rmd` file.

```r
sqf <- readRDS("data/sqf_2011.rds")
```

Use object `sqf` to complete the following tasks.

Consult the data dictionary in folder `data_dictionary` of your repo. 
The xlsx file has two tabs with variable descriptions and encoding for every 
variable.

## Tasks

#### Task 1

You must use functions in package `tidyverse` unless there is no Base-R
equivalent. Your code should output only the necessary rows and variables from 
the data frame to answer the question or complete the task. If the answer is
a single number, the result in vector format is fine.
**Each answer should include a 1-2 sentence write up.**

1. How many individuals were frisked or searched in the month of August
   by precinct 40?

2. Create a new variable called `season` according to the following rule
      - spring - March through May
      - summer - June through August
      - fall   - September through November
      - winter - December through February
      
   for when an sqf event occurred. Using this new variable, for each season,
   what proportion of individuals were frisked for inappropriate attire?
   
3. Compute the probability of being involved in an sqf incident for each
   race. Compute the conditional probability of being arrested given each
   race. For each result, sort the probabilities in descending order.
   
4. What was the most common "reason for stop"?

5. Compute the median age for those involved in an sqf event for each day of the
   week (Sunday - Saturday). *Hint:* Look at functions `mday()`, `month()`,
   `day()`, and `wday()` in package `lubridate`. Make a reasonable decision on
   how to deal with the obvious incorrect age values.
   
6. Based on the characteristics of sex, race, age, and build, what were the
   three most typical individuals involved in an sqf incident?
   
7. How does police finding at least a pistol, rifle, assault weapon or machine 
   gun on a suspect vary with time of day for the month of January?
   
#### Task 2

1. Based on your initial, and possibly further, analysis, form a narrative of 
   what can be conveyed to a reader using the data and possibly 
   supplementary data. You may pose this as question in which you hope to find
   a data driven answer. If you use supplementary data, make sure your work is
   reproducible - add the data to your repo or have code that reads it in
   from a remote host location.

2. Create a visualization or set of visualizations that depict this narrative. 
   They should tell an interesting story and / or provide insights into the 
   underlying data. There is no single correct answer for these data and your 
   visualization should depend on what your narrative is for the reader. 
   All visualizations should use functions in `ggplot2` or similar packages
   we discussed - `ggiraph`, `plotly`, `patchwork`, `gganimate`, etc. Be sure
   to follow best visualization practices.

3. Provide a write-up describing your design choices for your visualization(s). 
   Explain why your visualization(s) is effective at elucidating 
   your narrative.
   
*A portion of the total points for this task will be allocated to the*
*creativity level of your narrative and visualizations.*

#### Task 3

Tidy up or decorate your Rmd file. Incorporate some of the features I used in
labs this semester. Feel free to expand beyond these features. Check out the
Rmarkdown cheat sheet and Holtz's 
[Pimp my RMD](https://holtzy.github.io/Pimp-my-rmd/) website.

## Essential details

#### Deadline and submission

**The deadline to submit Homework 3 is 11:59pm on Wednesday, February 19.** Only
your final commit and code in the master branch will be graded. 
To get your work into branch master (the only branch that will be graded), 
initiate a pull request on GitHub. This will then merge your work into the 
master branch upon approval by one of your teammates.

#### Help

- Post your questions in the #hw3 channel on Slack. Explain your error / problem
  in as much detail as possible or give a reproducible example that generates 
  the same error. Make use of the code snippet option available in Slack.

- Visit the instructor or TAs in office hours.

- The instructor and TAs will not answer any questions unrelated to directions
  and interpretation within the first 12 hours of this homework being assigned, 
  and they will not answer questions within 6 hours of the deadline.

#### Academic integrity

This is a team assignment. You should not communicate with other
teams. As a reminder, any code you use directly or as inspiration must be cited.

To uphold the Duke Community Standard:

- I will not lie, cheat, or steal in my academic endeavors;
- I will conduct myself honorably in all my endeavors; and
- I will act if the Standard is compromised.

#### Grading

| **Topic**                                     | **Points** |
|-----------------------------------------------|------------|
| Task 1                                        | 16         |
| Task 2                                        | 8          |
| Task 3                                        | 2          |
| at least 1 significant commit per team member | 2          |
| Code style and format (named code chunks)     | 2          |
| **Total**                                     | **30**     |

*Documents that fail to knit after minimal intervention will receive a 0*.

## References

1. Publications, Reports - NYPD. (2020). www1.nyc.gov. Retrieved 12 February 
   2020, from 
   https://www1.nyc.gov/site/nypd/stats/reports-analysis/stopfrisk.page

2. 2018, Y. (2020). Pimp my RMD: a few tips for R Markdown. Holtzy.github.io. 
   Retrieved 10 February 2020, from https://holtzy.github.io/Pimp-my-rmd/
---
title: "Test1Rstudio"
date: 2016-08-25
author: davidwdenton
output: html_document
---

```{r}
#1 RStudio Practice Script----

##General things to do----

###Preloaded packages----
sessionInfo() #see packages preloaded
library(help="stats" ) #see functions loaded with a package, frequent analysis descriptives, aov, cor, t
data() #preloaded data sets, further description

###Use ? to get help----
?NULL # NULL means different things, here it means “empty” or fill-in with something, also try ??

###Install a new package----
install.packages("car") #add packages car and carData, Companion to Applied Regression
library(car) #loads packages and also carData package

###Data screening----
View(States) #shows data set as data frame (i.e. table), let’s View(States)
str(States) #shows a simple summary of data, the structure, such as a little info about variables 

##Descriptive statistics----

?iris

###Measures of central tendency----
median(iris$Petal.Length) #data file name followed by dollar sign, $, and data file heading/variable
median(volcano) #depending on object for data file may not need to designate variable (i.e. heading)
mean(cars$speed) #mean function is in base, cars is a preloaded data set, not to be confused with car
mode() #mode is storage mode of an object, in base, not a measure of central tendency
max() #or min()
stem(iris$Petal.Length) # makes a stem and leaf plot, still printed info, see hist() for comparison

?States #in carData package, inspect States with View() and str()
hist(States$dollars) # histogram, look for normal distribution/bell shape
boxplot(States$pay) # boxplot, look for outliers or extreme cases
plot() # plot(States$SATV, States$dollars)

#Element, atomic vector, vector, matrix, data frame; functions (several hundred in R), expression
#assign symbols, <-, info on the right to a label on the left, such as x <- 2, read x gets 2, = subs for <-
x <- 2 #x gets or is assigned the number 2, stored in the workspace, called by typing x, x is atomic vector
x <- 1:12 #x gets a list of numbers 1 to 12, x contains elements, x is also a vector
x <- c('faith', "hope", "love") #x is a vector, c is a function and it combines elements
x
x <- 5 # lets also assign 5 to y with y <- 5
y <- 5
z <- x == y #x, y, and z are objects, z is a logical atomic vector or element, == is a logical operator
z
volcano #volcano is a matrix try View(volcano), States is a data frame, try View(States)
volcano <- volcano

```

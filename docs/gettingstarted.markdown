---
layout: page
title: Getting Started
permalink: /notebooks/gettingstarted/
---


Download the ipynb file at <https://introtobibliometrics-clarkeiakovakis.notebooks.azure.com/j/notebooks/Getting%20Started%20with%20Jupyter%20Notebooks%20and%20R.ipynb>

# Introduction

The Jupyter Notebook is an open-source web application that allows you to create and share documents that contain live code, equations, visualizations and narrative text. 

Azure Notebooks is a free hosted service to develop and run Jupyter notebooks in the cloud with no installation.

We are using these platforms to avoid having to install R and R Studio onto your own computer. Furthermore, by interacting with R in this notebook, you will be able to execute code that I have already written, and see explanations of it first hand. Because this is such a brief session, we cannot go into detail about learning the R language, but I have provided some resources at the end of this document.
If you plan on using `rcrossref` more extensively, I would recommend downloading R and R Studio to your own computer and using it there. Also, the Crossref team encourages requests with appropriate contact information, and will forward you to a dedicated API cluster for improved performance when you share your email with them. We cannot do that in this notebook, but you can do that in R.

For a more detailed walkthrough of this entire lesson, including instructions for downloading R and R Studio, sharing your email with Crossref, and much more, please visit the set of tutorials at https://ciakovx.github.io/fsci_syllabus.html.

# Licensing

This walkthrough is distributed under a [https://creativecommons.org/licenses/by/4.0/](Creative Commons Attribution 4.0 International (CC BY 4.0) License). 


# Jupyter Notebooks


Jupyter Notebooks have two different keyboard input modes:

* **Command Mode** - Make changes on the Notebook level. Indicated by a grey cell border with a blue left margin. 
* **Edit Mode** - Make changes to an individual cell. Indicated by a green cell border

A new cell will always start as a **Code** cell, where you can type in R code and execute it here in your Jupyter notebook. All code in this notebook is R, but in Azure Notebooks you can create Notebooks that are F# or Python.

Please feel free to add your own notes in a Markdown cell during this workshop, or write your own R code! 

Useful keyboard shortcurts when you are in Command Mode:
* **Enter** to enter Edit Mode to edit the cell
* **B** to create new cell below the current cell
* **A** to create new cell above the current cell
* **Y** to change a Markdown cell to Code
* **M** to change a Code cell to Markdown
* Press **D** twice to delete the cell
  
Shortcuts when you are in Edit Mode:
* **Esc** to enter Command Mode
* **Ctrl + Enter** to Run cell and stay in the cell
* **Shift + Enter** to Run cell and select the next cell
* **Alt (or option on Mac) + Enter** to Run cell and insert a new cell below.
* **Ctrl (or Cmd on Mac) + Z**: Undo

---
**TRY IT YOURSELF**

Select the below cell in Edit Mode by double clicking in it, or by clicking it on the margin and pressing **Enter**. It should have a green border. Notice that this is a **Code** cell. Press Shift + Enter to execute the code. This will print the output and select the next cell.

Then, when you are in the next cell, press Ctrl + Enter. This will print the output and stay in the same cell.

Then, press the down arrow on your keyboard to to to the next cell. Enter Edit Mode (green border) by pressing Enter. Press Alt (or option on Mac) + Enter. This will print the output and create a new cell.

Then press the down arrow or select the new empty cell. Make sure you are in Command Mode (blue border). Press D twice to delete the new cell.


```R
# press Shift + Enter
print("You just ran the cell and selected the next cell")
```


```R
# press Ctrl + Enter
print("You just ran this cell and the focus stayed here in this cell")
```


```R
# press Alt (or option on Mac) + Enter
print("You just ran the cell and inserted a new cell below it")
```

Notice the text in the above cells that starts with a hash **#** character. The hash indicates a **comment**. Anything following the hash symbol will not be evaluated. 

# R Basics

R is more of a programming language than a statistics program. It was started by Robert Gentleman and Ross Ihaka from the University of Auckland in 1995. They described it as “a language for data analysis and graphics.”1 You can use R to create, import, and scrape data from the web; clean and reshape it; visualize it; run statistical analysis and modeling operations on it; text and data mine it; and much more.

If you intend on continuing your R journey after this workshop, I recommend installing R and R Studio and doing your scripting there. To install R, go to https://www.r-project.org/. Click on CRAN (Comprehensive R Archive Network) under Download, and scroll down to your country. Select the download link corresponding to the city that is geographically closest to you. Go to https://www.rstudio.com/products/RStudio/#Desktop to download the RStudio desktop software.


We don't have enough time in today's workshop to learn much about R. There are many excellent R tutorials at the end of this document. To get help on R functions within Jupyter Notebooks, type `help()` with the function name in parentheses. For example, `help(sum)` or `help(which)`. This will provide a description of the function, its usage, and the arguments the function takes.

## Writing &amp; Evaluating Expressions

The *prompt* is the blinking cursor in a Code cell prompting you to take action. We type *expressions* into the prompt, and press Ctrl + Enter to *evaluate* those expressions.

Evaluate this expression:


```R
# Press Ctrl + Enter or click the Run button to evaluate 2 + 2
2 + 2
```

## Assigning values

The first operator you're going to come across is the assignment operator. This is the angle bracket (AKA the "less than"" symbol): `&lt;`, which you'll get by pressing **Shift + comma** and the hyphen `-` which is located next to the zero key. There is no space between them, and it is designed to look like a left pointing arrow `&lt;-`. 




```R
# assign 5 to y
y <- 5
```

Here I am creating a symbol called `y` and I'm *assigning* it the numeric value 5. Some R users would say "y *gets* 5." Lowercase `y`, is now a *numeric vector* with one element. Or you could say `y` is a numeric vector, and the first element is the number 5. When you assign something to a symbol, nothing happens in the console, but in the Environment pane in the upper right, you will notice a new object, y.

If you now type y into the console, and press Enter on your keyboard, R will evaluate the expression. In this case, R will print the elements that are assigned to y (the number 5). We can do this easily since y only has one element, but if you do this with a large dataset loaded into R, it will obliterate your console because it will print the entire thing. The [1] indicates that the number 5 is the first element of this vector.


```R
# evaluate y
y
```

As we saw above, you can also use the `print()` function:


```R
# using print() will do the same thing as just typing the variable in, it just makes it explicit
print(y)
```

---
**TRY IT YOURSELF**

1. Use the new code cells below. Make sure that 5 is assigned to `y` by typing in `y &lt;- 5`
2. Assign the number 10 to variable `x`. Add `x` and `y` and evaluate the expression.
3. Assign `x + y` to variable `myTotal`. 


```R
# assign 5 to y
y <- 5
```


```R
# assign 10 to x
x <- 10
```


```R
# assign the sum of x and y to myTotal. Print myTotal to the console.
myTotal <- x + y
myTotal
print(myTotal)


```

### Tips for assigning values

* **Do not use names of functions that already exist in R:** The assignment operator assigns a value to a symbol. We can pretty much pick any symbol, or name, for that variable, as long as it is not already a function in R. For example, you wouldn't want to name a variable `sum` because if you might end up in a confusing situation writing `sum(sum)`
* **R is case sensitive**: It is important to note that R is *case sensitive.* If you try evaluating a capital `Y`, you will be told `Error in eval(expr, envir, enclos): object 'Y' not found`.
* **No blank spaces or symbols other than underscores**: R users get around this in a couple of ways, either through capitalization (e.g. `myData`) or underscores (e.g. `my_data`). 
* **Do not begin with numbers or symbols**: Try to evaluate `1z &lt;- 4` or `%z &lt;- 4` and read the error message.
* **Be descriptive, but make your variable names short**: It's good practice to be descriptive with your variable names. If you're loading in a lot of data, choosing `myData` or `x` as a name may not be as helpful as, say, `ebookUsage`. Finally, keep your variable names short, since you will likely be typing them in frequently.



## Calling a function

R is a “functional programming language,” meaning it contains a number of functions you use to do something with your data. Call a function on a variable by entering the function into the console, followed by parentheses and the variables. 


```R
# take the square root of the sum of 2 + 2
sum(2, 2)
?sum
```

Typing a question mark before a function will pull the help page up in the Navigation Pane in the lower right. Type `?sum` to view the help page for the `sum` function. You can also call `help(sum)`. This will provide the description of the function, how it is to be used, and the arguments. 

In the case of `sum()`, the ellipses `. . .` represent an unlimited number of numeric elements. `sum()` also takes the argument `na.rm`. This is a logical (`TRUE/FALSE`) argument specifying if NA values (missing data) should be removed when the argument is evaluated.

The function `is.function()` will check if an argument is a function in R. If it is a function, it will print `TRUE` to the console.



```R
# confirm that sum is a function
is.function(sum)
```


```R
# sum takes an unlimited number (. . .) of numeric elements
sum(3, 4, 5, 6, 7)
```


```R
# evaluating a sum with missing values will return NA
sum(3, 4, NA)
```


```R
# look at the help file for sum
?sum
```


```R
# but setting the argument na.rm to TRUE will remove the NA
sum(3, 4, na.rm = TRUE)
```

Functions can be nested within each other. For example, `sqrt()` takes the square root of the number provided in the function call. Therefore you can run `sum(sqrt(9), 4)` to take the sum of the square root of 9 (3) and add it to 4. Or you could write the quadratic formula: `[(-b) + sqrt((b^2) - 4ac)] / (2*a)`.

# R Resources

## Learning R
1. `swirl` is a package you can install in R to learn about R and data science interactively. Just type `install.packages("swirl")` into your R console, load the package by typing `library("swirl")`, and then type `swirl()`. Read more at &lt;http: swirlstats.com=""&gt;.

2. [Try R](http://tryr.codeschool.com/) is a browser-based interactive tutorial developed by Code School.

3. Anthony Damico's [twotorials](https://www.youtube.com/playlist?list=PLcgz5kNZFCkzSyBG3H-rUaPHoBXgijHfC) are a series of 2 minute videos demonstrating several basic tasks in R.

4. [Cookbook for R](http://www.cookbook-r.com/) by Winston Change provides solutions to common tasks and problems in analyzing data

5. If you're up for a challenge, try the free [R Programming MOOC in Coursera](https://www.coursera.org/learn/r-programming) by Roger Peng.

6. Books:
    * [R For Data Science](http://r4ds.had.co.nz/) by Garrett Grolemund &amp; Hadley Wickham [free]
    * [An Introduction to Data Cleaning with R](https://cran.r-project.org/doc/contrib/de_Jonge+van_der_Loo-Introduction_to_data_cleaning_with_R.pdf) by Edwin de Jonge &amp; Mark van der Loo [free]
    * [YaRrr! The Pirate's Guide to R](https://bookdown.org/ndphillips/YaRrr/) by Nathaniel D. Phillips [free]
    * Springer's [Use R!](https://link.springer.com/bookseries/6991) series [not free] is mostly specialized, but it has some excellent introductions including Alain F. Zuur et al.'s [A Beginner's Guide to R](https://link.springer.com/book/10.1007/978-0-387-93837-0) and Phil Spector's [Data Manipulation in R](https://link.springer.com/book/10.1007/978-0-387-74731-6)

## Data

If you need some data to play with, type `data()` in the console for a list of data sets. To load a dataset, type it like this: `data(mtcars)`. Type `help(mtcars)` to learn more about it. You can then perform operations, e.g. 
```{r dataloading, comment=NA, eval=F}
head(mtcars)
nrow(mtcars)
mean(mtcars$mpg)
sixCylinder &lt;- mtcars[mtcars$cyl == 6, ]
```

See also rdatamining.com's [list of free datasets](http://www.rdatamining.com/resources/data).

## Cheat Sheets

* [Base R Cheat Sheet](https://paulvanderlaken.files.wordpress.com/2017/08/base-r-cheetsheat.pdf) by Mhairi McNeill
* [Data Transformation with dplyr Cheat Sheet](https://github.com/rstudio/cheatsheets/blob/master/data-transformation.pdf) by RStudio
* [Data Wrangling with dplyr and tidyr Cheat Sheet](https://paulvanderlaken.files.wordpress.com/2017/08/ddplyr-cheatsheet-data-wrangling-plyr.pdf) by RStudio
* [Complete list of RStudio cheatsheets](https://github.com/rstudio/cheatsheets/)

## Style guides
Use these resources to write cleaner code, according to established style conventions

* Hadley Wickham's [Style Guide](http://adv-r.had.co.nz/Style.html)
* Google's [R Style Guide](https://google.github.io/styleguide/Rguide.xml)
* Tip: highlight code in your script pane and press **Ctrl/Cmd + I** on your keyboard to automatically fix the indents&lt;/http:&gt;

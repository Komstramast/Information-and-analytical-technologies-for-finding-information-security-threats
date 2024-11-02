# Введение в R

## Произведём запуск задания:

**\> swirl::swirl()**

*Welcome to swirl! Please sign in. If you’ve been here before, use the same name as you did then. If you are new, call yourself something unique.*

**What shall I call you? Yaroslav**

*Thanks, Yaroslav. Let’s cover a couple of quick housekeeping items before we begin our first lesson. First of all, you should know that when you see ‘…’, that means you should press Enter when you are done reading and ready to continue.*

***… \<– That’s your cue to press Enter to continue***

*Also, when you see ‘ANSWER:’, the R prompt (\>), or when you are asked to select from a list, that means it’s your turn to enter a response, then press Enter to continue.*

***Select 1, 2, or 3 and press Enter***

***1: Continue.*** ***2: Proceed.3: Let’s get going!***

***Выбор: 3***

*You can exit swirl and return to the R prompt (\>) at any time by pressing the Esc key. If you are already at the prompt, type bye() to exit and save your progress. When you exit properly, you’ll see a short message letting you know you’ve done so.*

*When you are at the R prompt (\>):*

-   *Typing skip() allows you to skip the current question.*

-   *Typing play() lets you experiment with R on your own; swirl will ignore what you do…*

-   *UNTIL you type nxt() which will regain swirl’s attention.*

-   *Typing bye() causes swirl to exit. Your progress will be saved.*

-   *Typing main() returns you to swirl’s main menu.*

-   *Typing info() displays these options again.*

*Let’s get started!*

**…**

*To begin, you must install a course. I can install a course for you from the internet, or I can send you to a web page (<https://github.com/swirldev/swirl_courses>) which will provide course options and directions for installing courses yourself. (If you are not connected to the internet, type 0 to exit.)*

1.  **R Programming: The basics of programming in R**

2.  **Regression Models: The basics of regression modeling in R 3: Statistical Inference: The basics of statistical inference in R 4: Exploratory Data Analysis: The basics of exploring data in R 5: Don’t install anything for me. I’ll do it myself.**

**Выбор: 1** *\|==============================================================\| 100%*

*Course installed successfully!*

*Please choose a course, or type 0 to exit swirl.*

**1: R Programming 2: Take me to the swirl course repository!**

**Выбор: 1**

## Теперь запустим подкурсы и выполним их:

### 1. Базовые структурные блоки (Basic Building Blocks)

*Please choose a lesson, or type 0 to return to course menu.*

**1: Basic Building Blocks 2: Workspace and Files\
3: Sequences of Numbers 4: Vectors\
5: Missing Values 6: Subsetting Vectors\
7: Matrices and Data Frames 8: Logic\
9: Functions 10: lapply and sapply\
11: vapply and tapply 12: Looking at Data\
13: Simulation 14: Dates and Times\
15: Base Graphics**

**Выбор: 1**

*\| \| 0%*

*In this lesson, we will explore some basic building blocks of the R programming language.*

**…**

*\|== \| 3%*

*If at any point you’d like more information on a particular topic related to R, you can type help.start() at the prompt, which will open a menu of resources (either within RStudio or your default web browser, depending on your setup). Alternatively, a simple web search often yields the answer you’re looking for.*

**…**

*\|=== \| 5%*

*In its simplest form, R can be used as an interactive calculator. Type 5 + 7 and press Enter.*

``` r
5 + 7
```

```         
[1] 12
```

*Great job!*

*\|===== \| 8%*

*R simply prints the result of 12 by default. However, R is a programming language and often the reason we use a programming language as opposed to a calculator is to automate some process or avoid unnecessary repetition.*

**…**

*\|======= \| 11%*

*In this case, we may want to use our result from above in a second calculation. Instead of retyping 5 + 7 every time we need it, we can just create a new variable that stores the result.*

**…**

*\|======== \| 13%*

*The way you assign a value to a variable in R is by using the assignment operator, which is just a ‘less than’ symbol followed by a ‘minus’ sign. It looks like this: \<-*

**…**

*\|========== \| 16%*

*Think of the assignment operator as an arrow. You are assigning the value on the right side of the arrow to the variable name on the left side of the arrow.*

**…**

*\|=========== \| 18%*

*To assign the result of 5 + 7 to a new variable called x, you type x \| \<- 5 + 7. This can be read as ‘x gets 5 plus 7’. Give it a try now.*

``` r
x <- 5 + 7
```

*You’re the best!*

*\|============= \| 21%*

*You’ll notice that R did not print the result of 12 this time. When you use the assignment operator, R assumes that you don’t want to see the result immediately, but rather that you intend to use the result for something else later on.*

**…**

*\|=============== \| 24%*

*To view the contents of the variable x, just type x and press Enter. Try it now.*

``` r
x
```

```         
[1] 12
```

*Keep working like that and you’ll get there!*

*\|================ \| 26%*

*Now, store the result of x - 3 in a new variable called y.*

``` r
y <- x -3
```

*Excellent work!*

*\|================== \| 29%*

*What is the value of y? Type y to find out.*

``` r
y
```

```         
[1] 9
```

*Keep up the great work!*

*\|==================== \| 32%*

*Now, let’s create a small collection of numbers called a vector. Any object that contains data is called a data structure and numeric vectors are the simplest type of data structure in R. In fact, even a single number is considered a vector of length one.*

**…**

*\|===================== \| 34%*

*The easiest way to create a vector is with the c() function, which stands for ‘concatenate’ or ‘combine’. To create a vector containing the numbers 1.1, 9, and 3.14, type c(1.1, 9, 3.14). Try it now and store the result in a variable called z.*

``` r
z <- c(1.1, 9, 3.14)
```

*You are doing so well!*

*\|======================= \| 37%*

*Anytime you have questions about a particular function, you can access R’s built-in help files via the ? command. For example, if you want more information on the c() function, type ?c without the parentheses that normally follow a function name. Give it a try.*

``` r
?c
```

```         
запускаю httpd сервер помощи... готово
```

*You got it right!*

*\|======================== \| 39% Type z to view its contents. Notice that there are no commas separating the values in the output.*

``` r
z
```

```         
[1] 1.10 9.00 3.14
```

*That’s correct!*

*\|========================== \| 42% You can combine vectors to make a new vector. Create a new vector that contains z, 555, then z again in that order. Don’t assign this vector to a new variable, so that we can just see the result immediately.*

*Type c(z, 555, z). Don’t create a new variable. We just want to view the result.*

``` r
c(z,555,z) 
```

```         
[1]   1.10   9.00   3.14 555.00   1.10   9.00   3.14
```

*You are amazing!*

*\|============================ \| 45%*

*Numeric vectors can be used in arithmetic expressions. Type the following to see what happens: z \* 2 + 100.*

``` r
z*2+100
```

```         
[1] 102.20 118.00 106.28
```

*Your dedication is inspiring!*

*\|============================= \| 47%*

*First, R multiplied each of the three elements in z by 2. Then it added 100 to each element to get the result you see above.*

**…**

*\|=============================== \| 50%*

*Other common arithmetic operators are +, -, /, and \^ (where x\^2 means ‘x squared’). To take the square root, use the sqrt() function and to take the absolute value, use the abs() function.*

**…**

*\|================================= \| 53%*

*Take the square root of z - 1 and assign it to a new variable called my_sqrt.*

``` r
my_sqrt <- sqrt(z-1)
```

*You are doing so well!*

*\|================================== \| 55%*

*Before we view the contents of the my_sqrt variable, what do you think it contains?*

**1: a vector of length 0 (i.e. an empty vector)**

**2: a vector of length 3 3: a single number (i.e a vector of length 1)**

**Выбор: 2**

*You are doing so well!*

*\|==================================== \| 58%*

*Print the contents of my_sqrt.*

``` r
my_sqrt
```

```         
[1] 0.3162278 2.8284271 1.4628739
```

*That’s the answer I was looking for.*

*\|====================================== \| 61%*

*As you may have guessed, R first subtracted 1 from each element of z, then took the square root of each element. This leaves you with a vector of the same length as the original vector z.*

**…**

\|======================================= \| 63%

*Now, create a new variable called my_div that gets the value of z divided by my_sqrt.*

``` r
#my_div <- div(my_sqrt)
```

``` r
my_div <- my_sqrt/2
```

*Give it another try. Or, type info() for more options.*

*Enter my_div \<- z / my_sqrt. The spaces on either side of the `/` sign are not required, but can often improve readability by making code appear lesscluttered. In the end, it’s personal preference.*

``` r
my_div <- z/my_sqrt
```

*All that practice is paying off!*

*\|========================================= \| 66%*

*Which statement do you think is true?*

**1: my_div is a single number (i.e a vector of length 1)**

**2: The first element of my_div is equal to the first element of z divided by the first element of my_sqrt, and so on…**

**3: my_div is undefined**

**Выбор: 2**

*You got it!*

*\|========================================== \| 68%*

*Go ahead and print the contents of my_div.*

``` r
my_div 
```

```         
[1] 3.478505 3.181981 2.146460
```

*Your dedication is inspiring!*

*\|============================================ \| 71%*

*When given two vectors of the same length, R simply performs the specified arithmetic operation (`+`, `-`, `*`, etc.) element-by-element. If the vectors are of different lengths, R ‘recycles’ the shorter vector until it is the same length as the longer vector.*

**…**

*\|============================================== \| 74%*

*When we did z \* 2 + 100 in our earlier example, z was a vector of length 3, but technically 2 and 100 are each vectors of length 1.*

**…**

*\|=============================================== \| 76%*

*Behind the scenes, R is ‘recycling’ the 2 to make a vector of 2s and the 100 to make a vector of 100s. In other words, when you ask R to compute z 2 + 100, what it really computes is this: z c(2, 2, 2) + c(100, 100, 100).*

**…**

*\|================================================= \| 79%*

*To see another example of how this vector ‘recycling’ works, try adding c(1, 2, 3, 4) and c(0, 10). Don’t worry about saving the result in a new variable.*

*Enter c(1, 2, 3, 4) + c(0, 10) in the console to see how R adds two vectors of different length. Don’t assign the result to a variable.*

``` r
c(1,2,3,4)+c(0,10)
```

```         
[1]  1 12  3 14
```

*That’s correct!*

*\|=================================================== \| 82%*

*If the length of the shorter vector does not divide evenly into the length of the longer vector, R will still apply the ‘recycling’ method, but will throw a warning to let you know something fishy might be going on.*

**…**

*\|==================================================== \| 84%*

*Try c(1, 2, 3, 4) + c(0, 10, 100) for an example.*

``` r
c(1,2,3,4) + c(0,10,100)
```

```         
Warning in c(1, 2, 3, 4) + c(0, 10, 100): длина большего объекта не является
произведением длины меньшего объекта

[1]   1  12 103   4
```

*You got it right!*

*\|====================================================== \| 87%*

*Before concluding this lesson, I’d like to show you a couple of time-saving tricks.*

**…**

*\|======================================================= \| 89%*

*Earlier in the lesson, you computed z \* 2 + 100. Let’s pretend that you made a mistake and that you meant to add 1000 instead of 100. You could either re-type the expression, or…*

**…**

*\|========================================================= \| 92%*

*In many programming environments, the up arrow will cycle through previous commands. Try hitting the up arrow on your keyboard until you get to this command (z \* 2 + 100), then change 100 to 1000 and hit Enter. If the up arrow doesn’t work for you, just type the corrected command.*

``` r
z*2+1000
```

```         
[1] 1002.20 1018.00 1006.28
```

*You nailed it! Good job!*

*\|=========================================================== \| 95%*

*Finally, let’s pretend you’d like to view the contents of a variable that you created earlier, but you can’t seem to remember if you named it my_div or myDiv. You could try both and see what works, or…*

**…**

*\|============================================================ \| 97%*

*You can type the first two letters of the variable name, then hit the Tab key (possibly more than once). Most programming environments will provide a list of variables that you’ve created that begin with ‘my’. This is called auto-completion and can be quite handy when you have many variables in your workspace. Give it a try. (If auto-completion doesn’t work for you, just type my_div and press Enter.)*

``` r
my_div
```

```         
[1] 3.478505 3.181981 2.146460
```

You got it right!

*\|==============================================================\| 100%*

### 2. Рабочие пространства и файлы (Workspace and Files)

*\| \| 0%*

*In this lesson, you’ll learn how to examine your local workspace in R and begin to explore the relationship between your workspace and the file system of your machine.*

**…**

*\|== \| 3%*

*Because different operating systems have different conventions with regards to things \| like file paths, the outputs of these commands may vary across machines.*

**…**

*\|==== \| 5%*

*However it’s important to note that R provides a common API (a common set of commands) for interacting with files, that way your code will work across different kinds of computers.*

**…**

*\|====== \| 8%*

*Let’s jump right in so you can get a feel for how these special functions work!*

**…**

*\|======== \| 10%*

*Determine which directory your R session is using as its current working directory using getwd().*

``` r
getwd()
```

```         
[1] "D:/Учёба/7 семестр/Информационно-аналитические технологии поиска угроз информационной безопасности/Threat hunting!/Lab1"
```

*Your dedication is inspiring!*

*\|========== \| 13%*

*List all the objects in your local workspace using ls().*

``` r
ls()
```

```         
[1] "my_div"  "my_sqrt" "x"       "y"       "z"      
```

*You nailed it! Good job!*

*\|============ \| 15%*

*Some R commands are the same as their equivalents commands on Linux or on a Mac. Both Linux and Mac operating systems are based on an operating system called Unix. It’s always a good idea to learn more about Unix!*

**…**

*\|============== \| 18%*

*Assign 9 to x using x \<- 9.*

``` r
x <- 9
```

*That’s correct!*

*\|================ \| 21%*

*Now take a look at objects that are in your workspace using ls().*

``` r
ls()
```

```         
[1] "my_div"  "my_sqrt" "x"       "y"       "z"      
```

*You are doing so well!*

*\|================== \| 23%*

*List all the files in your working directory using list.files() or dir().*

``` r
dir()
```

```         
[1] "README.html"      "README.md"        "README.qmd"       "README.rmarkdown"
```

*Nice work!*

*\|===================== \| 26%*

*As we go through this lesson, you should be examining the help page for each new function. Check out the help page for list.files with the command ?list.files.*

``` r
?list.files
```

*You are doing so well!*

*\|======================= \| 28%*

*One of the most helpful parts of any R help file is the See Also section. Read that section for list.files. Some of these functions may be used in later portions of this lesson.*

**…**

*\|========================= \| 31%*

*Using the args() function on a function name is also a handy way to see what arguments a function can take.*

**…**

*\|=========================== \| 33%*

*Use the args() function to determine the arguments to list.files().*

``` r
args(list.files)
```

```         
function (path = ".", pattern = NULL, all.files = FALSE, full.names = FALSE, 
    recursive = FALSE, ignore.case = FALSE, include.dirs = FALSE, 
    no.. = FALSE) 
NULL
```

*You got it!*

*\|============================= \| 36%*

*Assign the value of the current working directory to a variable called “old.dir”.*

``` r
old.dir <- getwd()
```

*Excellent work!*

*\|=============================== \| 38%*

*We will use old.dir at the end of this lesson to move back to the place that we started. A lot of query functions like getwd() have the useful property that they return the answer to the question as a result of the function.*

**…**

*\|================================= \| 41%*

*Use dir.create() to create a directory in the current working directory called “testdir”.*

``` r
dir.create("testdir")
```

*Excellent job!*

*\|=================================== \| 44%*

*We will do all our work in this new directory and then delete it after we are done. This is the R analog to “Take only pictures, leave only footprints.”*

**…**

*\|===================================== \| 46%*

*Set your working directory to “testdir” with the setwd() command.*

``` r
setwd("testdir")
```

*You nailed it! Good job!*

*\|======================================= \| 49%*

*In general, you will want your working directory to be someplace sensible, perhaps created for the specific project that you are working on. In fact, organizing your work in R packages using RStudio is an excellent option. Check out RStudio at <http://www.rstudio.com/>*

**…**

*\|========================================= \| 51%*

*Create a file in your working directory called “mytest.R” using the file.create() function.*

``` r
file.create("mytest.R")
```

```         
[1] TRUE
```

*You are really on a roll!*

*\|=========================================== \| 54%*

*This should be the only file in this newly created directory. Let’s check this by listing all the files in the current directory.*

**list.files()**

$$1$$ “mytest.R”

*That’s the answer I was looking for.*

*\|============================================= \| 56%*

*Check to see if “mytest.R” exists in the working directory using the file.exists() function.*

``` r
file.exists("mytest.R")
```

```         
[1] TRUE
```

*Excellent job!*

*\|=============================================== \| 59%*

*These sorts of functions are excessive for interactive use. But, if you are running a program that loops through a series of files and does some processing on each one, you will want to check to see that each exists before you try to process it.*

**…**

*\|================================================= \| 62%*

*Access information about the file “mytest.R” by using file.info().*

``` r
file.info("mytest.R")
```

```         
         size isdir mode               mtime               ctime
mytest.R    0 FALSE  666 2024-11-02 16:47:03 2024-11-02 16:47:03
                       atime exe
mytest.R 2024-11-02 16:47:03  no
```

*Excellent job!*

*\|=================================================== \| 64%*

*You can use the \$ operator — e.g., file.info(“mytest.R”)\$mode — to grab specific items.*

**…**

*\|===================================================== \| 67%*

*Change the name of the file “mytest.R” to “mytest2.R” by using file.rename().*

``` r
file.rename("mytest.R", "mytest2.R")
```

```         
[1] TRUE
```

*Perseverance, that’s the answer.*

*\|======================================================= \| 69%*

*Your operating system will provide simpler tools for these sorts of tasks, but having the ability to manipulate files programatically is useful. You might now try to delete mytest.R using file.remove(‘mytest.R’), but that won’t work since mytest.R no longer exists. You have already renamed it.*

**…**

*\|========================================================= \| 72%*

*Make a copy of “mytest2.R” called “mytest3.R” using file.copy().*

``` r
file.copy("mytest2.R", "mytest3.R")
```

```         
[1] TRUE
```

*Nice work!*

*\|=========================================================== \| 74%*

*You now have two files in the current directory. That may not seem very interesting. But what if you were working with dozens, or millions, of individual files? In that case, being able to programatically act on many files would be absolutely necessary. Don’t forget that you can, temporarily, leave the lesson by typing play() and then \| return by typing nxt().*

**…**

*\|============================================================== \| 77%*

*Provide the relative path to the file “mytest3.R” by using file.path().*

``` r
file.path("mytest3.R")
```

```         
[1] "mytest3.R"
```

*You are doing so well!*

*\|================================================================ \| 79%*

*You can use file.path to construct file and directory paths that are independent of the operating system your R code is running on. Pass ‘folder1’ and ‘folder2’ as arguments to file.path to make a platform-independent pathname.*

``` r
file.path('folder1', 'folder2')
```

```         
[1] "folder1/folder2"
```

*That’s correct!*

*\|================================================================== \| 82% Take a look at the documentation for dir.create by entering ?dir.create . Notice the ‘recursive’ argument. In order to create nested directories, ‘recursive’ must be set to TRUE.*

``` r
?dir.create
```

*Great job!*

*\|==================================================================== \| 85%*

*Create a directory in the current working directory called “testdir2” and a subdirectory for it called “testdir3”, all in one command by using dir.create() and file.path().*

``` r
dir.create(file.path("testdir2", "testdir3"), recursive = TRUE)
```

*That’s the answer I was looking for.*

*\|====================================================================== \| 87%*

*Go back to your original working directory using setwd(). (Recall that we created the variable old.dir with the full path for the orginal working directory at the start of these questions.)*

``` r
setwd(old.dir)
```

*You are quite good my friend!*

*\|======================================================================== \| 90%*

*It is often helpful to save the settings that you had before you began an analysis and then go back to them at the end. This trick is often used within functions; you save, say, the par() settings that you started with, mess around a bunch, and then set them back to the original values at the end. This isn’t the same as what we have done here, but it seems similar enough to mention.*

***…***

*\|========================================================================== \| 92%*

*After you finish this lesson delete the ‘testdir’ directory that you just left (and everything in it)*

**…**

*\|============================================================================ \| 95%*

*Take nothing but results. Leave nothing but assumptions. That sounds like ‘Take nothing but pictures. Leave nothing but footprints.’ But it makes no sense! Surely our readers can come up with a better motto . . .*

**…**

*\|============================================================================== \| 97%*

*In this lesson, you learned how to examine your R workspace and work with the file system of your machine from within R. Thanks for playing!*

**…**

*\|================================================================================\| 100%*

### 3. последовательности чисел (Sequences of Numbers)

*\| \| 0%*

*In this lesson, you’ll learn how to create sequences of numbers in R.*

**…**

*\|=== \| 4%*

*The simplest way to create a sequence of numbers in R is by using the `:` operator. Type 1:20 to see how it works.*

``` r
1:20
```

```         
 [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20
```

*You nailed it! Good job!*

*\|======= \| 9%*

*That gave us every integer between (and including) 1 and 20. We could also use it to \| create a sequence of real numbers. For example, try pi:10.*

``` r
pi:10
```

```         
[1] 3.141593 4.141593 5.141593 6.141593 7.141593 8.141593 9.141593
```

*You nailed it! Good job!*

*\|========== \| 13%*

*The result is a vector of real numbers starting with pi (3.142…) and increasing in increments of 1. The upper limit of 10 is never reached, since the next number in our sequence would be greater than 10.*

**…**

*\|============== \| 17%*

*What happens if we do 15:1? Give it a try to find out.*

``` r
15:1
```

```         
 [1] 15 14 13 12 11 10  9  8  7  6  5  4  3  2  1
```

*You are amazing!*

*\|================= \| 22% \| It counted backwards in increments of 1! It’s unlikely we’d want this behavior, but \| nonetheless it’s good to know how it could happen.*

**…**

*\|===================== \| 26%*

*Remember that if you have questions about a particular R function, you can access its documentation with a question mark followed by the function name: ?function_name_here. However, in the case of an operator like the colon used above, you must enclose the symbol in backticks like this: ?`:`. (NOTE: The backtick (\`) key is generally located in the top left corner of a keyboard, above the Tab key. If you don’t have a backtick key, you can use regular quotes.)*

**…**

*\|======================== \| 30%*

*Pull up the documentation for `:` now.*

``` r
?`:`
```

*Nice work!*

*\|=========================== \| 35%*

*Often, we’ll desire more control over a sequence we’re creating than what the `:` operator gives us. The seq() function serves this purpose.*

**…**

*\|=============================== \| 39%*

*The most basic use of seq() does exactly the same thing as the `:` operator. Try seq(1, 20) to see this.*

``` r
seq(1,20)
```

```         
 [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20
```

*All that hard work is paying off!*

*\|================================== \| 43%*

*This gives us the same output as 1:20. However, let’s say that instead we want a vector of numbers ranging from 0 to 10, incremented by 0.5. seq(0, 10, by=0.5) does just that. Try it out.*

``` r
seq(0,10,by=0.5)
```

```         
 [1]  0.0  0.5  1.0  1.5  2.0  2.5  3.0  3.5  4.0  4.5  5.0  5.5  6.0  6.5  7.0
[16]  7.5  8.0  8.5  9.0  9.5 10.0
```

*You are doing so well!*

*\|====================================== \| 48%*

*Or maybe we don’t care what the increment is and we just want a sequence of 30 numbers between 5 and 10. seq(5, 10, length=30) does the trick. Give it a shot now and store the result in a new variable called my_seq.*

``` r
my_seq <- seq(5, 10, length=30)
```

*You nailed it! Good job!*

*\|========================================= \| 52%*

*To confirm that my_seq has length 30, we can use the length() function. Try it now.*

``` r
length(my_seq)
```

```         
[1] 30
```

*Nice work!*

*\|============================================= \| 57%*

*Let’s pretend we don’t know the length of my_seq, but we want to generate a sequence of integers from 1 to N, where N represents the length of the my_seq vector. In other words, we want a new vector (1, 2, 3, …) that is the same length as my_seq.*

**…**

*\|================================================ \| 61%*

*There are several ways we could do this. One possibility is to combine the `:` operator and the length() function like this: 1:length(my_seq). Give that a try.*

``` r
1:length(my_seq)
```

```         
 [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25
[26] 26 27 28 29 30
```

*All that hard work is paying off!*

*\|==================================================== \| 65%*

*Another option is to use seq(along.with = my_seq). Give that a try.*

``` r
seq(along.with = my_seq)
```

```         
 [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25
[26] 26 27 28 29 30
```

*You got it right!*

*\|======================================================= \| 70%*

*However, as is the case with many common tasks, R has a separate built-in function for this purpose called seq_along(). Type seq_along(my_seq) to see it in action.*

``` r
seq_along(my_seq)
```

```         
 [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25
[26] 26 27 28 29 30
```

*You are really on a roll!*

*\|========================================================== \| 74%*

*There are often several approaches to solving the same problem, particularly in R. Simple approaches that involve less typing are generally best. It’s also important for your code to be readable, so that you and others can figure out what’s going on without too much hassle.*

**…**

*\|============================================================== \| 78%*

*If R has a built-in function for a particular task, it’s likely that function is highly optimized for that purpose and is your best option. As you become a more advanced R programmer, you’ll design your own functions to perform tasks when there are no better options. We’ll explore writing your own functions in future lessons.*

**…**

*\|================================================================= \| 83%*

*One more function related to creating sequences of numbers is rep(), which stands for ‘replicate’. Let’s look at a few uses.*

**…**

*\|===================================================================== \| 87%*

*If we’re interested in creating a vector that contains 40 zeros, we can use rep(0, times = 40). Try it out.*

``` r
rep(0, times = 40)
```

```         
 [1] 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
[39] 0 0
```

*Keep up the great work!*

*\|======================================================================== \| 91%*

*If instead we want our vector to contain 10 repetitions of the vector (0, 1, 2), we can do rep(c(0, 1, 2), times = 10). Go ahead.*

``` r
rep(c(0, 1, 2), times = 10)
```

```         
 [1] 0 1 2 0 1 2 0 1 2 0 1 2 0 1 2 0 1 2 0 1 2 0 1 2 0 1 2 0 1 2
```

*You are amazing!*

*\|============================================================================ \| 96%*

*Finally, let’s say that rather than repeating the vector (0, 1, 2) over and over again, we want our vector to contain 10 zeros, then 10 ones, then 10 twos. We can do this with the `each` argument. Try rep(c(0, 1, 2), each = 10).*

``` r
rep(c(0, 1, 2), each = 10)
```

```         
 [1] 0 0 0 0 0 0 0 0 0 0 1 1 1 1 1 1 1 1 1 1 2 2 2 2 2 2 2 2 2 2
```

*You got it right!*

*\|===============================================================================\| 100%*

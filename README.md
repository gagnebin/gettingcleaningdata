Peer Assignment Course Project for Getting and Cleaning Data on Coursera
===========

The goals of this document are to provide some instruction on the best way to quickly evaluate the course project.


What is delivered in the repository
====================

The following information are passed to the evaluator:

1. The raw data.
2. A [tidy data set](http://vita.had.co.nz/papers/tidy-data.pdf) 
3. A code book markdown document describing each variable and its values in the tidy data set.  
4. An explicit and exact recipe you used to go from 1 -> 2,3 

Let's look at each part of the data package you see in the assignment webpage on coursera and in the repository. 


### The raw data

The raw dat can be found [here](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)

I certify that: 

1. Ran no software on the raw data
1. Did not manipulate any of the numbers in the raw data
1. Did not remove any data from the raw data set
1. Did not summarize the raw data in any way

### The tidy data set

The tidy data set in text file format can be found on the the assignment webpage on coursera that you have to evaluate or in the current repository.

The general principles of [tidy data](http://vita.had.co.nz/papers/tidy-data.pdf) has been applied:

1. Each variable you measure is in one column
2. Each different observation of that variable is in a different row
3. There is one table for each "kind" of variable

To see the tidy data set on R, download the "tidydataset.txt"" file and use the following command lines:

data <- read.table("tidydataset.txt", header = TRUE)
View(data)

Assuming that "tidydataset.txt" is in your working directory in R.

### The code book

The code book markdown document can be found in the repository "CodeBook.md" which contains information about the variables (including units!) in the tidy data set, summaries calculations and any other relevant information.

### The instruction script

You should be able to exactly replicate
the analyses from raw data all the way to final results (tidy data set).  

The computer script (in `R`) "run_analysis.R" takes the raw data as input and produces the tidy data I am sharing as output. You can try running the script
and see if the code produces the same output. 

To make it quick and easy to evaluate each steps of the assignment (5 in total) is annotated as "STEP 1", "STEP 2", etc. along the script. Also the script is fully commented to explain each command lines.

Here is a pseudocode to replicate the analysis :

1. Step 1 - take the [raw file](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip), save it locally on your R woking directory. 1. Step 2 - take the analysis file "run_analysis.R", save it locally on your R woking directory.
1. Step 3 - run "run_analysis.R" with the following command line:
source('~/run_analysis.R', echo=TRUE)
1. Step 4 - read the result with the following command line:
data <- read.table("tidydataset.txt", header = TRUE)
View(data)



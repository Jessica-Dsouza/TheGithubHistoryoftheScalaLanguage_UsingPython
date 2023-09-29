30k Commits, Scala is a programming language, popular among data scientist, it's an open source project. Which means we can see the entire development history. - who made changes, what changes were made, code reviews, etc.

pulls_2011-2013.csv contains the basic information about the pull requests, and spans from the end of 2011 up to (but not including) 2014.
pulls_2014-2018.csv contains identical information, and spans from 2014 up to 2018.

pull_files.csv contains the files that were modified by each pull request.

Datacamp mined the data from github

1. Preparing and Cleaning : In total there are 3 files pulls_2011-2013,pulls_2014-2018, pull_files. We have to combine first 2 datasets and convert the date column to datetime. Merging all 3 files together


2. Analyzing the data:
    2.1 Is the project still actively maintained? : we will do this by plotting a chart of the project's activity. We will calculate the number of pull requests submitted each (calendar) month during the project's lifetime. We will then plot these numbers to see the trend of contributions.

    2.2 Is the community or contributors small or large? : we will plot a histogram of the number of pull requests submitted by each user. A distribution that shows that there are few people that only contribute a small number of pull requests can be used as in indicator that the project is not welcoming of new contributors


    2.3  What files were changed in the last ten pull requests? : Get nlargest from pulls, create a new dataframe which is merged with pull_files (to get file names)

    2.4  Who made the most pull requests to a given file? Identify the pull requests that changed the file by filtering.Count the number of changes made by each developer by using groupby() and count()

    2.5  Who made the last ten pull requests on a given file?

    2.6  The pull requests of two special developers : Used groupby(), nlargest(), agg(), draw bar graph to compare two developers

    2.7  Visualizing the contributions of each developer: Same as above but this time we are looking at file contribution

---
layout: post
title:  "Assignment 1: Data Manipulation and Visualization"
categories: posts
---

In this assignment we will work with a dataset of The Museum of Modern Art (MOMA) in New York's collection. The data is fully described [here](https://github.com/MuseumofModernArt/collection) and a short description is provided below

> This research dataset contains more than 120,000 records, representing all of the works that have been accessioned into MoMA’s collection and cataloged in our database. It includes basic metadata for each work, including title, artist, date made, medium, dimensions, and date acquired by the Museum. Some of these records have incomplete information and are noted as “not Curator Approved.” 

The assignment has to be completed by **October 8**. 

You hand in the assignment by opening an issue [here](https://github.com/sebastianbarfort/sds/issues). You press the green *New Issue* button in the top right corner. The Title of your issue should be "Group xxx: Assignment 1", where *xxx* is your group number. Then you copy your *R* code in the text box below. I'll show you how this is done in the lecture on Monday. 

You can load the data used in the assignment by running the following piece of code


{% highlight r %}
library("readr")
df = read_csv("https://raw.githubusercontent.com/MuseumofModernArt/collection/master/Artworks.csv")
{% endhighlight %}

Create an `R` script that answers the eight questions below. Please use comments to mark what questions are answered by each code block. Use comments to explain what each code block does. 

An example is provided below


{% highlight r %}
# Question 1 ---------------
# read the data
df = read_csv("https://raw.githubusercontent.com/MuseumofModernArt/collection/master/Artworks.csv")

# prepare data: first we do this, then we do this...
...

# Question 2 ---------------

...
{% endhighlight %}

1. Create a new dataframe of the stock of paintings at MOMA for each month in the year. 
2. Use `ggplot2` and your new data frame to plot the the stock of paintings on the y-axis and the date on the x-axis. 
    - what kind of geom do you think is appropriate? why?
    - color the geom you have chosen red
    - add a title and custom axis labels 
3. Create the same plot but this time the color should reflect the stock of paintings for curator approved and non-curator approved paintings, respectively
4. Create a new data frame of the stock of paintings grouped by what department the painting belongs to.
5. Plot this data frame using `ggplot2`. Which department has had the highest increase in their stock of paintings?
6. Write a piece of code that counts the number of paintings by each artist in the data set. List the 10 painters with the highest number of paintings in MOMA's collection. 
7. The variable `ArtistBio` lists the birth place of each painter. Use this information to create a world map where each country is colored according to the stock of paintings in MOMA's collection. 
8. The `Dimensions` variable lists the dimensions of each painting. Use your data manipulation skills to calculate the area of each painting (in cm's). Create a data frame of the five largest and five smallest paintings in MOMA's collection. 


# Non-mandatory Guldøl Exercise

For those who have some extra time on your hands I have an extra assignment. It is not mandatory and you do not have to complete it unless you want to. However, by completing this assignment you have the opportunity to *win a great price* and write your name in the hall of fame of Social Data Science data visualization experts. 

The task is relatively simple: **I want you to do an interesting data visualization of the Danish federal budget proposal for 2016**. The Danish newspaper Berlingske did a [static visualization](http://www.b.dk/nationalt/grafisk-se-finansloven-i-hovedtraek) and based on what you know from the last couple of lectures it should be immediately clear that this can be done better. I'm asking you to do exactly that! 

I have scraped the data and made it available in a tidy data format [here](https://raw.githubusercontent.com/sebastianbarfort/sds/gh-pages/data/finanslov_tidy.csv). The script that converts the data is available [here](https://github.com/sebastianbarfort/sds/blob/gh-pages/scripts/tidy_finanslov.R) in case you're interested. 

It's up to you to decide what you feel is interesting about the Danish federal budget proposal. Send me an email with 

1. an interesting data visualization
2. 3-10 lines about what the visualization communicates
3. the R script

The best data visualization will be rewarded with a Danish "guldøl", and I will send your proposal to Berlingske as an alternative to what they decided to do. 

![](http://www.olfabrikken.dk/~/media/Images/Corporate/Product%20Images/Product%20Image%20181x400/Guldoel%20flaske.ashx)



  

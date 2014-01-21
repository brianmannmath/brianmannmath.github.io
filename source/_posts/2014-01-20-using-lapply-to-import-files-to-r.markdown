---
layout: post
title: "Using lapply to import files to R"
date: 2014-01-20 18:22:42 -0700
comments: true
published: true
categories: 
---

One of the trickest parts, for me, of learning a new language is figuring out how it interacts with the outside world (i.e. the rest of your computer). This post might seem dumb to people with even a few months of R experience, but I decided to post it anyway, if only to document my learning process. When I started learning R I was given the following task: you have a directory which stores several .csv files, say 001.csv, 002.csv, ... 332.csv and a task which requires you to do something with all of them. The task itself is irrelevant, so we'll ignore it. How do you import all these files efficiently? 

My first instinct (probably because the file names were all numbers) was to loop over all of the names. But, of course, I needed to ensure all of the zeroes were still there. So I needed to do something like

{%codeblock lang:r%}
for (id in 1:332){
    num = formatC(id, width = 3, flag = "0") #creates a 3-digit string represent	ing an integer
    D <- paste(directory, paste(num, "csv", sep = "."), sep = "/") #D is the fil	e name string
    x <- read.csv(D)
    data <- c(data,x) #data is a list of all the data frames we needed to import
}
{%endcodeblock%}

But that's gross, and in any case, it doesn't work if the names of the files don't live in some list you can easily access (like 1:332). Recall, though, that R has some nice "map" functions, namely 'lapply'. Also

{%codeblock lang:r%}
dir()
{%endcodeblock%}

returns a list of the names of files in the working directory. So

{%codeblock lang:r%}
setwd("where your .csv files are")
data <- lapply(dir(),read.csv)
{%endcodeblock%}

returns a data frame consisting of all the .csv files you needed to import. Voila. 
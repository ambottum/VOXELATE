---
author: Anna Bottum
title: Hello and Navigating Terminal
date: 2018-07-06
tags: []
categories: []
---

#### Hello!

If you are reading this, you likely have some remote interest in programming/computer development or art. A short background on me: while in college I worked in an air quality research lab. Most of my work consisted of navigating between computers via Linux terminal and performing analyses on model output using the NCAR Command Language, or NCL. After a two year hiatus from computers, I am taking online courses in Python & R, and self-teaching web design with the help of a few computer-literate family members (community is everything when it comes to learning to code).

As a result, I have arrived at this project with a foggy but existent understanding of computers & how to communicate with them, & every day my knowledge base grows in capacity & excitement for the possibilities that are uncovered. In these blog posts, I will focus on the aspects of computers that I struggled with (& most likely still do) while embarking on this journey of digitalizing my work. Each post will be a consecutive step that I took in building this site, and I will emphasize points that I found to be most helpful, or things that seasoned programmers consider obvious & consequently forget to mention.

#### Introduction
This first post will focus on something fairly simple but absolutely crucial: navigating your computer through the terminal. Terminal is a Mac application, in short it is a direct interface between user and computer. Usually when we interact with a computer, we click buttons, enter info into text bars, etc. This type of activity, or communication, is through a graphical user interface, or GUI. A helpful comparison may be, communicating through a GUI is like touching or speaking to the face of an individual to give commands, whereas communicating through terminal is like bypassing the surface and interacting directly with the brain of the individual to give commands.

Because of this, Terminal is usually a great way to get a lot of work done very fast- like moving a large number of files or automating git commands so there is no room for fatal user error (something I will write on later). But heads up - while Terminal is incredibly useful, it can be incredibly dangerous for your computer or your work- deleting key components with just a few characters: http://www.lug.wsu.edu/node/414so Always make sure to fully understand where you are and what you are typing before you hit enter.

##### 1) Open Terminal:
Terminal in your finder, under applications, open Terminal
A screen will open, with a few lines of text that may look something like:  
<br>
`Last login: Wed Jul  4 09:51:37 on ttys002`  
`Annas-MacBook-Pro:~ annabottum$`  

##### 2) Check where we are:
On the command line, print `pwd` which stands for *print working directory*; hit enter  
`Last login: Wed Jul  4 09:51:37 on ttys002`  
`Annas-MacBook-Pro:~ annabottum$ pwd`  
`/Users/annabottum`  
Here we can see I am currently located in my account (**annabottum**) inside of the **Users** folder.  

##### 3) See what's inside:  
If you're opening a folder you haven't used for a while, you may want to see what it contains there are two ways to do this: if you are in the folder whose contents you wish to view, type `ls` *(list)* then hit enter.
Let's say, however, we know there is a file called **Desktop** inside **annabottum**, instead of moving into **Desktop** to list its contents, we can type  
`ls Desktop`  

##### 4) Move around:
The base command to move through your file system is `cd`, *change directory*: simply `cd` will move you to the root directory, so in addition we need to make some specifications.
Say we'd like to move *down* into **Desktop** from **annabottum**, since **annabottum** has multiple folders inside, or below it, we must specify where we want to jump down to:  
`cd Desktop/`  
Just to be sure we did what we wanted to, type  
`pwd`  
Terminal should return  `/Users/annabottum/Desktop`  
If there were a folder in **Desktop** called **test_1**, we could jump into it from **annabottum** (two levels above) by typing the following:  
`cd Desktop/Lesson_1/`  
Now, if we want to move back up into **Desktop**, since there is only one direct *up* from **Lesson_1**, we can simply type  
`cd ..`
To move up *two* levels to **annabottum**, we type  
`cd ../../`  

##### 5) Create a folder:  
Let's make a folder in Desktop that will contain your first file. `cd` int **Desktop** and enter  

`mkdir Lesson_1`  `mkdir` stands for make directory, and will create a folder called Lesson_1

##### 5) Create a file:  
`cd` into **Lesson_1**
 and create a file named **Script_1**:  
 `vi Script_1`  
 To enter text, hit *i* on the keyboard; you are now in *insert* mode.
 After editing or adding to your file, you will want to save your changes. To leave *insert* mode, hit *esc* on the keyboard.
 There are mulitple ways to do the next step, but I like  
 `:wq`  
 which signifies *write*, then *quit*. After hitting enter, you will find yourself back on the command line, outside the file.

 A quick note: On the command line, a space is considered a boundary between one element and the next, so when naming files and folders, be sure to replace spaces with underscores.

##### 6) Move file:
We want to move **Script_1** from **Lesson_1** to **Desktop**.  
`mv`  
 is the move command, and its syntax is as follows:  
 `mv file_name destination_folder`  
So here we type  
`mv Script_1 ~/Desktop`  
`cd` up to **Desktop** and do a quick `ls` to be sure it moved.

Quick note: `~` signifies *home directory*, so with `~/Desktop`, you are telling your computer to point home, then look for **Desktop**   

##### 7) Delete file:
Since our skillset is growing by the minute, we need to delete **Script_1** to make room for our next project.
`rm file_name`  where `rm` stands for *remove*

These are a few basic terminal commands to help you begin navigating the inner mind of your computer :)

Anna

---
layout: post
description: Using code.org to make a quiz
author: Vivian Ni
categories: [markdown, week3]
title: Blogging my Code.org Quiz 
comments: true
---

Press this <a href="https://studio.code.org/projects/applab/lRDbJP_aMc_8eQXMMqe3UkFvSjWGQMvXnGVgDJq_EHU/edit"> link </a> to play my quiz!

## 1. Program Purpose and Function
**Purpose:** The purpose of my program is to create a quiz that tests the user on their knowledge. The code consists of user input as well as answers that can be selected. These answers are either correct or incorrect and depending on the answer selected or input given, the code will take the user to the next question or the incorrect screen.

**Function:**
- Here is an example of my code for selectable answers. I used the blocks "on event" and "set screen" to change the screen off my game to the next question depending on the answer chosen.

<img src ="https://github.com/vivianknee/FastPages/blob/master/images/code1.png?raw=true" width="370" height="270">

- Here is an example of my code for questions that take user input.  

<img src ="https://github.com/vivianknee/FastPages/blob/master/images/input.png?raw=true" width="415" height="270">

## 2. Data Abstraction

## 3. Managing Complexity

## 4. Procedural Abstraction

## 5. Algorithm Implementation

## 6. Testing/Debugging
One problem that I ran into was getting my code to output the final number of attempts the user needed to complete the quiz. At first, I wasn't sure how to print strings as well as variables in one block. I also wasn't sure how to change the text every time depending on different user performance. To solve this problem, I used multiple addition operator blocks to put multiple variables into one block. I set each variable to either a string or my "attempts" variable. My final code was this:

<img src ="https://github.com/vivianknee/FastPages/blob/master/images/finalscore.PNG?raw=true" width="440" height="270">

Another problem I ran into was some error in my code that was not letting me output what I wanted to. The error that I was getting was that no matter how many incorrect attempts I made during testing, the final text always said 0. I then identified that the problem lied in the block "var = attempts + 1". Somehow this block was not adding anything to the number of attempts causing it to always remain at 0.

But why?

I started searching google for the error as well as javascript syntax. The reason why my previous code wasn't working was due to global variable shadowing which means that one variable shares a name with another, resulting in confusion. Since I defined the variable "attempts" as 0 in the beginning but then used the same name to add 1 to the variable, my initial variable shadowed the new one causing the variable to be lost when the function returned. After searching some more, I found that another method to add to a score variable was to use the syntax "++" in front of the variable. This is what my code looked like after the changes. 

<img src ="https://github.com/vivianknee/FastPages/blob/master/images/finalworking.PNG?raw=true" width="400" height="270">

## Design
First I decided on the content of my quiz: Are you smarter than a 5th grader? This theme is inspired by the popular game "Are you smarter than a 5th grader?" It consists of simple questions testing the range of your knowledge.

The next thing I decided to do was design the GUI/looks of my game. I decided on 5 questions, each question would have 4 answers and each answer would have an image to go along with it. This was my initial draft of the game looks.

<img src ="https://github.com/vivianknee/FastPages/blob/master/images/GUI.png?raw=true" width="270" height="360">

This is what my design looked like when it was finalized

<img src ="https://github.com/vivianknee/FastPages/blob/master/images/guidone.png?raw=true" width="270" height="360">

I also made a screen for incorrect answers and completing the entire quiz. When the user clicks a wrong answer, the code will take them to the incorrect screen and let them go to the beginning of the quiz.






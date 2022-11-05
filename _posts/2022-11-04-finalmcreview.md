---
layout: post
author: Vivian Ni
categories: [final]
title: CollegeBoard Final MC
comments: true
---

![]({{ site.baseurl }}/images/final.JPG)

## Takeaways
- On my collegeboard Final MC, my score was 43/50
- The skills that I got wrong were:
    - 4.B: determine the result of code segments (3 wrong)
    - 2.B: implement and apply an algorithm (2 wrong)
    - 3.C: explain how abstraction manages complexity (1 wrong)
    - 4.A: explain how a code segment or program functions (1 wrong)

## Questions
##### **Q47**: What is displayed as a result of executing the code segment?

![]({{ site.baseurl }}/images/final1.JPG)

- I chose "21 40 30 40" but the answer was "21  40 30 50"
- Notes
    - I forgot about PEMDAS (order of operations) and I also just misread the question
    - I thought it wanted me to compute (c+d)/2 but it actually wanted me to solve c + (d/2)

#### **Q45**: What are the values of count1 and count2 as a result of executing the code segment?

![]({{ site.baseurl }}/images/final2.JPG)

- I chose "count1=3, count2=2" but the answer was "count1=2, count2=3"
- Notes
    - I overlooked the fact that the value had to be >0 not >=0 so I thought there were 3 positive integers instead of 2. This mistake also messed up my result for count2

#### **Q43**: What is the value of result after the code segment is executed?

![]({{ site.baseurl }}/images/final3.JPG)

- I chose "6" but the answer was "15"
- Notes
    - I misread the question as asking what the result would be when "result" was >5, but in actuality it was asking for the result when "x" became >5

#### **Q36**: Consider the following code segment, which is intended to store ten consecutive even integers, beginning with 2, in the list evenList. Assume that evenList is initially empty. Which of the following can be used to replace "<"MISSING CODE" so that the code segment works as intended?

![]({{ site.baseurl }}/images/final4.JPG)

- I chose "i  ←  i + 1 APPEND(evenList, 2 * i)" but the answer was "APPEND(evenList, 2 * i) i  ←  i + 1" 
- Notes
    - This question, I understood the code but what I got wrong was the order of the lines.
    - If i wanted to include "2" in my eveList, I would have to have the APPEND line come first otherwise "2" would be skipped and absent from evenList

#### **Q35**: what is displayed as a result of executing the code segment?
- Notes
    - I literally forgot to select two answers so I got the whole problem wrong

#### **Q23**: The position of a runner in a race is a type of analog data. The runner’s position is tracked using sensors. Which of the following best describes how the position of the runner is represented digitally?
- I chose "The position of the runner is determined by calculating the time difference between the start and the end of the race and making an estimation based on the runner’s average speed."
- The correct answer was "The position of the runner is sampled at regular intervals to approximate the real-word position, and a sequence of bits is used to represent each sample."
- Notes
    - While a runner’s position could be estimated using the runner’s average speed, a more accurate representation of the position over time can be achieved using a sampling technique.
    - Analog data, like the runner’s position, have values that change smoothly, rather than in discrete intervals. Analog data can be approximated digitally by measuring values of the analog signal at regular intervals called samples

#### **Q6**: In the following procedure, the parameter max is a positive integer. Which of the following is the most appropriate documentation to appear with the printNums procedure?

![]({{ site.baseurl }}/images/final5.JPG)

- I chose "Prints all positive odd integers that are greater than max." but the answer was "Prints all positive odd integers that are less than or equal to max."
- Notes
    - The function says it repeats *until* count > max so it doesn't make sense that printNums would display numbers greater than max.
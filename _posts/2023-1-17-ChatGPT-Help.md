---
layout: post
title: A Little Help from ChatGPT
date: 2023-1-17
preview: true
---

## Project Context
I’m working on a new personal project exploring nearly 10 years of auto accident data from my city. It’s highly detailed, with 142 columns and over 74,000 rows. I picked the dataset because I wanted to explore something larger than my previous project, and liked the complexity of so many features. 

The benefits of understanding traffic accident data are also very practical. If we can better understand what contributes to accidents, especially the most severe ones, we can take practical steps to reduce the likelihood of accidents, such as improved intersection and signal design, improved auto safety features, or better driver’s training. This can mean saved lives, reduced injuries, and reduced costs of vehicle repairs or replacement.

I’m still pretty early in the project, exploring and cleaning the data. Many of the features need to be converted from categorical values to numerical format, so that eventually I can model on the data. For example, the data indicates whether a bicycle was involved, with values of ‘yes’ or ‘no’. This is a simple enough update using ‘replace’ but I was going to do it in two steps, first converting the ‘no’ values to 0 and then the ‘yes’ values to 1. 

## Code Support

However, wanting to improve and simplify my code, I decided to have a little fun with ChatGPT. There is of course a lot of ongoing conversation about the tool, including using it to support coding. I provided ChatGPT some very basic information specific to my data and request, and it returned a very solid answer. 

![_config.yml](/images/ChatGPTreplacecode.png)

Sometimes I overlook dictionaries, but this is a great use case. Instead of doing two lines of code with ‘replace’, I can do it in one line (for reference, this part of my code that changes the values to numbers {‘no’ : 0, ‘yes’ : 1}  is what I mean by dictionary). I made a slight tweak to my code by changing the values in place, instead of redefining the column as ChatGPT suggested. You can see my code here:

![_config.yml](/images/myreplacecode.png)

## Conclusion

Using ChatGPT showed me an easier way to write my code and reminded me of how useful dictionaries are. It was also way less of a headache than trying to dig through Stack Overflow to find someone who had my same question and search through answers. Moving forward, I’ll definitely keep using ChatGPT as one of my resources when I get stuck. Rather than replacing this new skillset I am developing, I hope ChatGPT will enable me to do more, more quickly - more data exploration, cleaning, analysis, modeling and so on because I can spend less time digging for answers or stuck on syntax, and more time exploring interesting questions. 







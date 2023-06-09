# DataBias
This project was done for the class Intro To Human Centered Data Science, at the University of Texas at Austin.

Hypothesis - Perspective API is more likely to make mistakes on toxic comments that use words that are less common in insults

I created separate dataframes out of the original dataset given. I used Perspective API to find the toxicity values for the values of each dataframes. After examining the scores of these dataframes of original data, I determined the threshold for toxicity to be 0.56; anything above this value is toxic.

I created a new dataset by taking a sample of comments from the original data. However, I changed singular words in some of the comments - I replaced words that commonly used for insults, with words that have the same meaning, but are less commonly used in negative ways.

I found that my hypothesis was right. For example, while a comment including 'rape' was considered toxic, this same comment was not toxic when the word 'molest' was used in place of 'rape', despite both of these words referring to sexual abuse. Similarly, a comment with the word 'kill' was considered toxic, while this same comment was not found to be toxic when it used the word 'execute', despite both of these words refer to causing someone to die. Another instance: a comment had a toxicity above the threshold when 'sex' was used but not when 'intercourse' was put in place of 'sex'.

I think this bias exists because of the connotations behind certain words. Certain words may have a more proper or formal connotation - they may be used in more professional settings, making them seem less insulting or rude. Other words may have the same exact meaning but are used much more casually and crudely, due to the connotations that society has given them. People may use these crude words to have the intended effect of harassing or insulting with their toxic comment. So, a machine may be trained to more easily catch these words that have more negative connotations, as these may seem more harmful, even if they have the exact same meaning as another word.

This is a relevant and important problem, as it could give people a way to insult or harass others without getting caught. For example, take one of my findings, where Perspective API only scored a comment as having a toxicity above the threshold when it involved the word 'kill', but not when 'kill' was replaced with 'execute'. Someone could make a death threat using the word 'execute' instead of 'kill', as a way to avoid getting caught by a machine. It is important to address this to ensure that all toxic comments are eliminated, despite their wording.

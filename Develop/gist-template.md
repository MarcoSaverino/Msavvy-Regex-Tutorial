# Msavvy-Regex-Tutorial

Welcome to my Regex tutorial! Hope you have as much fun reading as i did writing it!

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.
For the purpost of this tutorial we will go over the following regular expression

Matching an Email: 
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components
Regexes have several different components that work together in order to define a search pattern. The components we will go over can be found in the table of contents above.

### Anchors
Anchors true to the name are what match the starting and ending points of a string or line.The symbol ^ can be used match the beginning of a string, and $ can be used to match the end of a string as an example of Anchors.

In the matching email code 
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
You can see that these anchors ^ and $ being used. 

What the anchor is doing in our matching email code is saying that we are specifically looking for something that starts  with ^([a-z0-9_\.-]+) and ends with .([a-z\.]{2,6})$ . 

We will define what everything means inside the parantheses later in the tutorial but for now all you need to know is that it must start and end with those given parameters wthin the code. If it doesnt then there will be no match

### Quantifiers
Quantifiers sets the parameters for how many characters you need for it to be a match. Here are some examples of Quantifiers

* — You have a match zero or more times

+ — You have match a minimum of one time

? — You can either have no match or one match

To use our matching email code as an example, if we used the code xyz+ in our regex then this will match any string xy followed by minnimum one z. 

([a-z0-9_\.-]+)

The result of this would be match any string that contains a-z, 0-9, _, ., or -. The quantifier + means that it has to contain at least one of these in order to find a match.

### OR Operator
Acts like a boolean OR. Matches the expression before or after the |. It is able to operate within a group, or with a whole expression. These patterns are tested in order. Just as in javascript it will match either set of characters. It will look for this OR that.

[a-f0-9]{3} it will match a 3 character long string that contains a combination of a-f letters and 0-9 numbers. 

If you look at our regex example.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

It is not present in our code. 

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

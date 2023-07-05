# Msavvy-Regex-Tutorial

Welcome to my Regex tutorial! Hope you have as much fun reading as i did writing it!

## Summary

For the purpost of this tutorial we will go over the following regular expression

Matching an Email: 
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

With this Regex code you are able use it for validation to make sure emails follow a correct format. 

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

- '*' You have a match zero or more times

- '+' You have match a minimum of one time

- '?'  You can either have no match or one match

To use our matching email code as an example, if we used the code xyz+ in our regex then this will match any string xy followed by minnimum one z. 

([a-z0-9_\.-]+)

The result of this would be match any string that contains a-z, 0-9, _, ., or -. The quantifier + means that it has to contain at least one of these in order to find a match.

### OR Operator
Acts like a boolean OR. Matches the expression before or after the |. It is able to operate within a group, or with a whole expression. These patterns are tested in order. Just as in javascript it will match either set of characters. It will look for this OR that.

[a-f0-9]{3} it will match a 3 character long string that contains a combination of a-f letters and 0-9 numbers. 

If you look at our regex example.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

You can see how it is not present in our code. 

### Character Classes
Character classes in a regex will define a set of characters any of which can happening in a input string to trigger a match.
Here are some examples of other character classes that are common

- [ABC] The Characters found inside the brakets  match any character in the set.
- [^ABC] Adding a caret will find any character not in the set.
- [A-Z] Adding a dash between the two characters will make it a Range selection.
- \w Matches any word character (alphanumeric & underscore). It matches the ASCII characters [A-Za-z0-9_] including Latin alphabets, digits, and the underscore (_).
- \W matches any character except a word character like non-Latin letter or space.
- \d Matches any digit character from 0 to 9.
- \p Matches a character in the specified unicode category.

We have \d  present in the email matching code and what it will do is match a single letter character, a-z, after the @ sign in the email address. Thus making sure that a letter is matched after the @ in the email and not a number or special character.

### Flags
A flag changes the default searching behavior of a regular expression making a regex search in a different way.

A flag is denoted with a single lowercase alphabetic character.

We have a total of 6 flags

 -  i= Ignores casing which makes the expression search without case sensitivity 
 - g= In a global search this makes the expression search for all occurences.
 - m=  Multiline flag means making the boundary characters ^ and $ we mentioned earlier match the beginning and ending of every single line instead of the beginning and ending of the whole string..
 - u= Unicode Makes the expression assume individual characters as code points but not code units, and will match the 32-bit characters as well.
 - y= Will make the expression start searching the index indicated in its lastIndex property.
 - s=Dot All Makes the wild character "." match the newlines as well.

In our matching email code that is being used for this turorial a regex flag is not used. But i put them in there because its important to know!

### Grouping and Capturing
But this next part we can continue with the code for matching an email:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Thats the code as a reminder now lets continue on to grouping and capturing...

After /^ we have ([a-z0-9_\.-]+) as the first group appearing in our regex. Before moving on to a "match" with the next part of the code that must be true. ([\da-z\.-]+) is the second group and then we have ([a-z\.]{2,6}) as the third and final group that appears in our regex.

Each group has everything enclosed and captured within the parenthesis(). This isolates part of the full match and then assignes it an ID that will later be referred to within the regex. 

### Bracket Expressions
A bracket expression (which is an expression enclosed in"[]" ) will match a specific set of single characters, and could match a specific set of multi-character elements, based on the non-empty set of list expressions contained within the bracket expression.

### Greedy and Lazy Match
- 'Greedy' is when you matching the longest string possible.

- 'Lazy' means matching the shortest string possible. 

This section doesn't apply to the email matching code we are using in our tutorial 

### Boundaries
The \b is an anchor similar the caret and the dollar sign. It matches at a position that is called the “word boundary”. This match is zero-length. A word boundary, given by the special character \b, is a position that bounds a word i.e a place where the word starts or ends. 

Boundaries are not used in the matching an email code. 

### Back-references
Backreferences match the same characters as previously matched by a capturing group. Lets say you want to match a pair of opening and closing HTML tags along with the characters between them. By putting the opening tag into a backreference, you are able to reuse the name of the tag for the closing tag.

So to sum up you use back references to match the same text again.

Back-references are specified with backslash and a single digit (' \1 '). The part of the regular expression they refer to is called a subexpression, and is designated with parentheses.

again this isnt used in the matching an email REGEX we have been using for this tutorial.

### Look-ahead and Look-behind

Lookahead and lookbehind which can also be refered to as a lookaround are zero-length assertions just like the start and end of line, and start and end of word anchors. The difference is that lookaround actually matches characters, but then returns only the result which is a match or no match. 

Lookaround is not used in the matching an email code.

## Author

This tutorial was written by Marco Saverino

Github account:
https://github.com/MarcoSaverino

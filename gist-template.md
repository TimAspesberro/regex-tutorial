# Regex Tutorial

The purpose of this tutorial is to shed light on what a regex is, and ways in which it is used today.

## Summary

Regex stands for regular expression, it is a string of characters whose purpose is to find a pattern in a body of text. The reason for is is because the characters are a search pattern that locate and even replace a section of text. It utilizes letters of the alphabet as well as special character who each have their own unique function. Regular expression is used widely in search algorithms. This tutorial will focus on regez as it pertains to finding emails.

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

### Anchors
The anchor it like a cover of a book, it is at the start and end. It encapsulates what pattern you are looking for. For matching an email:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

The ^ signifies the start of the search and the $ is the end. This gives the pattern finder some structure as it gives the intructions a perimeter.


### Quantifiers

A quantifier specifies the number of a character or group of characters must be present in order to have a match. In a snippet of the matching code above:

([a-z0-9_\.-]+)

This is indicating that it is looking to matchwith  any letter between A-Z and any digit between 0-9. The + sign means that at least one of them must be present in order to have a match.


### OR Operator

The Or operator is seen as |, and is used to give different condition to fulfill a match. It is not in the matching email regex above but in the following example from matching a hex value:

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

This regex is checking for two matches the first being #?([a-f0-9]{6} and the second [a-f0-9]{3}) seperated by the | operator. It will then try to find any matches that fit the first or second pattern.


### Character Classes

A character class encapsulates what letters to expect in its respective section. The character classes are present within brackets []. In our example, this appears three seperate times.

[a-z0-9_\.-] (Searches A through Z and 0 through 9)
[\da-z\.-] (Searches for a numerical digit and A through Z)
[a-z\.] (Searches A through Z)

This is essential for creating guidlines of what you want your regular expression to match.


### Flags

A regex flag is an optional component only found at the end. There are six types but the thre most popular ones are g (global search), i (Case-insensitive search) and m (multi-line search). Each have their own purpose that help define the parameters of the search. This is not present in the email match regex but an altered example of that regex is found here:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/g


### Grouping and Capturing

Grouping and capturing essentially breaks down the pattern matching into components. It will look at the first grouping and won't continue to the next until it has a match. In our example:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

This is divided into three groups, each encapsulated in paranthesis. 

([a-z0-9_\.-]+)     ([\da-z\.-]+)       ([a-z\.]{2,6})

It will look at each one individually to make sure it is a match and move on to the next all the way down the line.


### Bracket Expressions
These are used to contain character classes and use brackets to achieve this. In the first grouping from above, the bracket is found within the parenthesis.

[a-z0-9_\.-]


### Greedy and Lazy Match

Greedy and Lazy matches refer to the number of times you want your pattern to match. A lazy match will compare with as few matches as possible while a greedy one will match as many times as possible. The process to create a lazy match is by adding a ? in the beginning right after /^ . To create a greedy match, you would add a + in the same position. Adding lazy and greedy matches into our example above would look like this:

Lazy: /^?([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Greedy: /^+([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/


### Boundaries

Boundaries allow you to add a "whole words only" function to the regular expression. This checks to see that there are only "word characters" which simply put means the 26 letters of the alphabet. This is achieved by adding a \b , it qualifies as an anchor which is the position where the $/ are.

### Back-references

The purpose of a backreference is to match a previously matched piece of text again. It is helpful when looking to match repeated text and words. This is not included in our example snippet.


### Look-ahead and Look-behind

These are collectively known as "look arounds" and they assert whether or not a match is even possible. This is not included in our example as well.


## Author

Tim Aspesberro
GitHub Link: https://github.com/TimAspesberro/regex-tutorial


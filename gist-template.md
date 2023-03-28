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

The Or operator is seen as |, and is used to give different condition to fulfill a match. It is not in the matching email regex above but in the following example from

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

Tim Aspesberro
GitHub Link: https://github.com/TimAspesberro/regex-tutorial


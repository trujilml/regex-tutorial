# Matching an Email Address - Regex Tutorial

We will be demonstrating the regex expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` to match an email address. This tutorial will be useful when integrating this expression in applications such as Node.js (Inquirer), JavaScript, or MongoDB.

## Summary

Regex, also known as regular expressions, are a series of unique patterns that define a search pattern and describe it by its unique factors. The search identifies these characters and validate input from this unique pattern. In the case of an email address, this regex has the unique responsiblity to make sure a user enters an email address that starts with a set of characters prior to implementing the `@` symbol followed by a domain link. 

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
The characters `^` and `$` are considered anchors for this regex. `^` matches the beginning of the regex and signifies a string that starts with other characters following it. `$` matches the end of the regex and signifies a string that ends with the characters preceding it. The regex ends at `$` as `(m)` or multiline, is not allowed in consideration that an email submission only takes one line.

### Quantifiers

### OR Operator

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

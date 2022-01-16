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

Bracket Expressions `[]` are positive as they represent the characters that we must match for the entry, in this case the requirements necessary for a valid email address. This pattern is referred to as a positive character group as they outline the characters we want to include. Within the email address regex example, there are three sets demonstrating these requirements.

`[a-z0-9_\.-]` - This string represents the main name of the email address and can include case-sensitive lowercase letters, numbers, underscore symbols, hyphens, and period symbols. The string can contain any lowercase letters `a-z` and numbers between `0-9`. The underscore `_` and hyphen `-` allow for any special, non alphanumberic characters (like punctuation or symbols). `\.` represents an escaped character (from the alphanumeric characters) that also matches a period `.` which is housed between the underscore `_` and hyphen `-` symbol.

`[\da-z\.-]` - This string represents the domain name of the email address and matches case-sensistive lowercase letters, numbers, hypens, and period symbols. The `\d` matches any numeral digit and is equivalent to the `0-9` expression we used earlier for the first string representing the name of the email address. `a-z` follows to represent the case-sensitive letters. Following it is the `\.` that is an escaped character which matches a period `.` and the end character which is a hyphen `-` that can be used for the domain name.

`[a-z\.]` - This string represents the final part of the domain name of the email address, usually presented as `.com` or `.net`. Within the bracket, case-sensitive lowercase letters `a-z` are represented followed by the escape character `\.` which matches a period symbol `.` for the final domain name. 

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

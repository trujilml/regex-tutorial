# Matching an Email Address - Regex Tutorial

We will be demonstrating the regex expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` to match an email address. This tutorial will be useful when integrating this expression in applications such as Node.js (Inquirer), JavaScript, or MongoDB.

## Summary

Regex, also known as regular expressions, are a series of unique patterns that define a search pattern and describe it by its unique factors. The search identifies these characters and validate input from this unique pattern. In the case of an email address, this regex has the unique responsiblity to make sure a user enters an email address that starts with a set of characters prior to implementing the `@` symbol followed by a domain link. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

The characters `^` and `$` are considered anchors for this regex. `^` matches the beginning of the regex and signifies a string that starts with other characters following it. `$` matches the end of the regex and signifies a string that ends with the characters preceding it. The regex ends at `$` as `(m)` or multiline, is not allowed in consideration that an email submission only takes one line.

### Quantifiers

Quantifiers set the limit of a string that the regex matches, looking for the minimum and maximum number of characters that the regex is looking for. 

The `+` operator at the end of the first two brackets indicates the matching of the pattern one or multiple times. This connects the user's email name, the name of the email service, and the ending domain name (ex: `.net`). 

`{2,6}` for the last bracket expression appears prior to the '$' anchor. It is looking for a minimum of 2 characters to a maximum of 6 characters for the ending domain name (ex: `.com`) to attach on the domain address, making up the domain section of the email address. It allows the match range for `[a-z\.]`.

### Character Classes

In regex, a character class defines a set of characters which occurs in an input string to fulfill a match.

The character class used in this expression is `\d` which matches a single number between 0-9. It uses only one character, therefore presenting a single digit like `9` versus a double digit like `99` which cannot be used when present. 

### Grouping and Capturing

Multiple parts of a string require the need to breakup in order to convey their matching and character requirements. Grouping constructs are used to divide the sections out, by parentheses `()`, between three sections or subexpression in the case of our regex example. These constructs are capturing as they have matched characters sequences that are reused.

`([a-z0-9_\.-]+)` - The first capturing group that matches the name of the user's email address.

`([\da-z\.-]+)` - The second capturing group that matches the name of the email service.

`([a-z\.]{2,6})` - The third capturing group that matches the domain name (ex. `.org`).

### Bracket Expressions

Bracket Expressions `[]` are positive as they represent the characters that we must match for the entry, in this case the requirements necessary for a valid email address. This pattern is referred to as a positive character group as they outline the characters we want to include. Within the email address regex example, there are three sets demonstrating these requirements.

`[a-z0-9_\.-]` - This string represents the main name of the email address and can include case-sensitive lowercase letters, numbers, underscore symbols, hyphens, and period symbols. The string can contain any lowercase letters `a-z` and numbers between `0-9`. The underscore `_` and hyphen `-` allow for any special, non alphanumberic characters (like punctuation or symbols). `\.` represents an escaped character (from the alphanumeric characters) that also matches a period `.` which is housed between the underscore `_` and hyphen `-` symbol.

`[\da-z\.-]` - This string represents the service name of the email address and matches case-sensistive lowercase letters, numbers, hypens, and period symbols. The `\d` matches any numeral digit and uses a single number between 0-9. It only uses a single number (`9`) rather than a double digit number (`99`). `a-z` follows to represent the case-sensitive letters. Following it is the `\.` that is an escaped character which matches a period `.` and the end character which is a hyphen `-` that can be used for the service name.

`[a-z\.]` - This string represents the final part of the domain name of the email address, usually presented as `.com` or `.net`. Within the bracket, case-sensitive lowercase letters `a-z` are represented followed by the escape character `\.` which matches a period symbol `.` for the final domain name. 

### Greedy and Lazy Match

Quantifiers are 'greedy' as they match as many occuring patterns as possible. In this case of the regex matching an email address, `+` is used to match a pattern one or more times and `{}` is used to match the numerical requirements for the domain name. The latter is presented as `{2,6}` for the requirement of the last string.

## Author

Mekayla Trujillo 
[GitHub Page](https://github.com/trujilml)


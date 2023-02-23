# Regex Tutorial: Matching an Email

A regular expression, or regex, is a sequence of characters that specifies a search pattern in text. These patterns are used by string-searching algorithms for "find" or "find and replace" operations on stings, or for input validation. Regular expression techniques are developed in thoretical computer science and formal language theory.

## Summary

I will be breaking down the following regex for matching an email
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ into basic components. This regex would be useful for validating email input.

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

The characters ^ and $ are both anchors in this regex. The ^ anchor signifies a string that begins with the characters that follow it. The $ anchor signifies a string that ends with the characters that precede it.

### Quantifiers

Quantifiers sets the limits of the string that the regex matches. They frequently include the minimum and maximum number of characters the regex is looking for. In this regex, quantifiers includes the + operator, which means one or more. Another quantifier for this regex includes {2,6}, which will allow a match range of 2-6 characters for the character set of [a-z\.].


### OR Operator

The OR operator [] is used in this regex. For example, [a-z0-9_\.-] means any character a-z, any digit 0-9, _, ., or -. The backslash (\) in this regex escapes a character that otherwise would be interpreted literally.

### Character Classes

This regex uses the character class \d which matches which matches a single character that is a digit from 0-9. 

### Flags

Flags are placed at the end of a regex, after the second slash, and they define additional functionality or limits for the regex. In this regex, it is enclosed by two / characters, so there are no flags.

### Grouping and Capturing

The primary way to group a section of a regex is by using parentheses (()), which is used in this regex. Each section within parentheses is known as a subexpression. The first set of () captures the username of the email address, the second set captures the domain name, and the final set captures the top-level domain. Broken down, /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ means one or more characters a-z, 0-9, _, ., or -, followed by a literal @, followed by one or more characters of any digit 0-9, a-z, ., or -, followed by a literal ., followed by 2-6 characters a-z or .

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
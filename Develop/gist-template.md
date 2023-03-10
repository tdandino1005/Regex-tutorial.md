# Regex Tutorial: Matching an Email

A regular expression, or regex, is a sequence of characters that specifies a search pattern in text. These patterns are used by string-searching algorithms for "find" or "find and replace" operations on stings, or for input validation. Regular expression techniques are developed in theoretical computer science and formal language theory.

## Summary

I will be breaking down the following regex for matching an email
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ into basic components. This regex would be useful for validating email input in various applications and technologies.

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

The primary way to group a section of a regex is by using parentheses (()), which is used in this regex. Each section within parentheses is known as a subexpression. The first set of () captures the username of the email address, the second set captures the domain name, and the final set captures the top-level domain. Capturing the first group in this expression is ([a-z0-9_\.-]+) that matches the user email name. The second capturing group is ([\da-z\.-]+) which matches the domain. Then the third capture group is ([a-z\.]{2,6}) to capture the top-level domain(.com).

### Bracket Expressions

Bracket expressions for email validation includes the character sets of [a-z0-9_\.-], which is matching any letter a-z and is case senstive. It also matches a character 0-9 and matches the characters "_" , "." , and "-"; [\da-z\.-], which is matching a single digit from 0-9, any character a-z (case senstive), and the characters "." and "-".; [a-z\.] matches any character a-z(case senstive) and the character ".".

### Greedy and Lazy Match

This regex uses the greedy quantitfier since it includes the + and {}. The + quanitfier means it will match as many times as possible giving back as needed. The {} quantifier is used when matching {2,6} for the last capture group which will allow a match range of 2-6 characters for the character set.

### Boundaries

A regex Boundary \b matches positions where one side is a word character (usually a letter, digit or underscore???but see below for variations across engines) and the other side is not a word character (for instance, it may be the beginning of the string or a space character). This regex does not use any boundaries since the \b is never used.

### Back-references

Backreferences match the same text as previously matched by a capturing group. If you want to match a pair of opening and closing HTML tags, and the text in between. By putting the opening tag into a backreference, we can reuse the name of the tag for the closing tag. Since this regex does not back reference a previous character that was used, it is not relevant in this tutorial.

### Look-ahead and Look-behind

Look-ahead allows you to add a condition of what will follow. Look-behind allows to match a pattern only if there is something before it. Look-ahead and look-behind are useful when we want to match something depending on the context before/after it.

## Author

This was completed by Tony Dandino. Please feel free to view my projects at https://github.com/tdandino1005.

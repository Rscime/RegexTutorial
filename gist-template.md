# Title (replace with your title)

The following is a Regex, or Regular Function, tutorial for the Matching A Hex value function:
'/^#?([a-f0-9]{6}|[3])$/'
This assignment was completed as part of the UCF coding bootcamp

## Summary

This tutorial will go into depth on the different parts of a Regex expression including anchors, quantifiers, grouping constructs, bracket expressions, character classes, the OR operator, flags and character escapes. While we discuss these components we will use a regex expression that matches hex values to demostrate the meaning of each part:
'/^#?([a-f0-9]{6}|[a-f0-9]{3})$/'
Overall this code snippet will check that the inputted value is formated as a 6 or 3 character hex code only including the following chracters: a, b, c, d, e, f, 0, 1, 2, 3, 4, 5, 6, 7, 8, 9. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
Anchors occur at the start and end of the code and appear as a '^' or a '$'.
A '^' occurs at the start of the expression and identifies what the string should start with. Anything following the ^ indicates possible starting values
A '$' occurs at the end of the expression and identifies what the string should end with. Anything before the $ indicates possible ending values
In our Hex Value Regex : 
'/^#?([a-f0-9]{6}|[a-f0-9]{3})$/'
the code after the ^ is '#?', we will discuss the '?' next, but this essentially means the code may or may not start with a '#'. After the '#?' we se a chuck of code grouped by (): '([a-f0-9]{6}|[a-f0-9]{3})' indicating the string must start with either 6 or 3 characters from the following list: a, b, c, d, e, f, 0, 1, 2, 3, 4, 5, 6, 7, 8, or 9. This group of code is immediately followed by the closing anchor '$' meaning the string must also end with these values.

### Quantifiers
Quantifiers are there to quantify the number of timers the string must match the regex expression values. THere are a few different types of quantifiers: *, +, ?, {x}, {x, }, {x, y}.
Of these the ? and {x} quantifiers are found in out hex value expression : '/^#?([a-f0-9]{6}|[a-f0-9]{3})$/'
The '?' means the preceding code must match the string once or not at all. Meaning our hex values must start with one '#' or not include a '#' at all
The '{6}' and '{3}' set the exact number of times the preceding code must be matched, so the '[a-f0-9]' preceding the '{6}' must be matched exactly 6 times and the '[a-f0-9]' preceding the '{3}' must be matched 3 times

### Grouping Constructs
Grouping constructs are indicated by closed parentheses '()' these essentially group snippets of code together so you can check a string section by section. In the Hex matching Regex: '/^#?([a-f0-9]{6}|[a-f0-9]{3})$/' the entire interior code is grouped, so the entire string must match in order to pass.

### Bracket Expressions
Bracket expressions indicate the type of values we want to match within our string. Values within these brackets can be listed out individually or indicated as ranges with a hyphen (-). In our Hex Value Regex: '/^#?([a-f0-9]{6}|[a-f0-9]{3})$/'
Our bracket expressions '[a-f0-9]' indicated that any letter between a and f and any number between 0 and 9 (or values a, b, c, d, e, f, 0, 1, 2, 3, 4, 5, 6, 7, 8, or 9) will act as a successful match for the string

### Character Classes
Chracter classes are similar to bracket expressions in that they inidcate ranges of matchable values, but thier formatting  is a bit different. Some commonlt used character classes include: '.' , '\d' , '\w', '\s'.
The '.' will match anything except '\n'
The '\d' will match any number between 0 and 9
The '\w' will match and capital or lowercase letter and any digits between 0 and 9
The '\s' will match any form of white space

### The OR Operator
The OR operator is signified by the '|' character.
In the Hex Value Regex: '/^#?([a-f0-9]{6}|[a-f0-9]{3})$/' the '|' indicates that the hex value can be a 6 character hex value with chracters a-f and 0-9 OR it can be a 3 character hex value with chracters a-f and 0-9

### Flags
Flags are extra search criteria added on to the end of an expression telling it what to ignore. 
The 'g' flag stands for global and tells the expression to test all of the code.
The 'i' flag stands for case-insensitive and tells the expression to ignore cases when matching values
The 'm' flag stands for multi-line search and tells the expression to recognize and treat multi-line strings as nulti-line strings

### Character Escapes
CHaracter escapes are ways to use characters typically used in coding in strings. You do this by preceding it with a '\'.
No character escapes are present in the Hex Value REGEX

## Author
Rachel Scime
UCF Coding Bootcamp
GitHub: https://github.com/Rscime

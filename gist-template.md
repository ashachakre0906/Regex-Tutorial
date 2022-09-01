# Regex-Tutorial for Matching an Email
A regex, which is short for regular expression, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input.

## Summary

This tutorial is going to explain the use of regex to match emails using the expressions` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/g`.This tutorial will give you a walkthrough of each Regex components and how it applies to matching an email.This regex makes sure that the given string matches the template for an email address.

## Table of Contents

  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Grouping Constructs](#grouping-constructs)
    - [Bracket Expressions](#bracket-expressions)
    - [Character Classes](#character-classes)
    - [The OR Operator](#the-or-operator)
    - [Flags](#flags)
    - [Character Escapes](#character-escapes)
  - [Author](#author)

## Regex Components

### Anchors
Anchors have special meaning in regular expressions. They do not match any character. Instead, they match a position before or after characters.You will often need to use anchors `^` and `$` to check if a string fully matches a pattern.The default of the anchor `^` or `$` is the single-line mode. In the single-line mode, the anchor `^` and `$` matches the beginning and the end of a string.
 - Starts the check at the start of the email address and ends the check at the end of the string.
 - ^ – The caret anchor matches the beginning of the text.
 - $ – The dollar anchor matches the end of the text.


### Quantifiers

Our regex uses two quantifiers, 
`+` and `{2,6}`
`[a-z.]{2,6}` - means that 2 to 6 characters matching those inside the brackets are expected. The numbers inside the curly brackets specify the lower and upper limit of the number of characters expected.

### Grouping Constructs
Grouping and Capturing is done with parenthesis `()` in regex.
Anything within the parenthesis is considered as a single group,which allows all the information treated to be single unit.
Between `/^` and `$/`, there are three distinct character groups, `([a-z0-9_.-]+)`, `([\da-z.-]+)`, and `([a-z.]{2,6})`.
If we remove the logic, the regex can be expressed this way:`(1)@(2).(3)`. This is much easier to read, and corresponds to what we know about email addresses, which always follow the (string)@(website).(com) template.


### Bracket Expressions
The final piece necessary to our RegEx is bracket expressions. There are three within our code:
`[a-z0-9_.-]`, `[\da-z.-]`, and `[a-z.]`
So, for example, in [a-z0-9_.-], this character will be matched by any lowercase letters from a-z, any digits from 0-9, or a period.


### Character Classes

The character class in this expression is \d, which matches a single character that is a digit from 0-9. It will only match a single digit such as "4", but not "44".
`a-z` looks for any characters within the range of lowercase a-z.
`0-9` Looks for any characters within the range of 0 - 9.
`/d` Matches any digit character (0-9). Equivalent to 0-9.
`/.` Escape Character (period).

### The OR Operator

(`|`):The regex four|4 accepts strings "four" or "4".

### Flags
Our Regex: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/g`
Flags used: `g`-`g` is used as a Global search and will match all occurrences.
Without the g flag, it'll only test for the first.

### Character Escapes

Escape sequences can be used to insert, special, and unicode characters. All escaped characters begin with the \ character.
Within a character set, only \, -, and ] need to be escaped.
In this case, `\.` is a escaped character which matches a `'.'`character (char code 46).

### Author:
Asha Chakre <br>
Please follow me and view my projects here.
Github Profile : https://github.com/ashachakre0906
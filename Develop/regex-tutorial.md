# Regex Tutorial -- Hex Values

This tutorial touches on how to utilize regex expressions to streamline code for various functions. The purpose of this challenge is to explain a specific regex expression in order to demonstrate my own knowledge of the search pattern that regex defines. The table of contents outline the parts of the tutorial that will be covered and can be clicked for quick access.

## Summary

Before diving into the specific regex expression, it is important to understand what exactly a regex expression is. It can be defined simply as a pattern that describes some amount of text. The complex patterns - the ones we routinely work with as developers - describe a series of characters, made up of letters, numbers, dots, underscores, percentage signs, and hyphens.
<br><br>
Specific regex expression utilize specific characters, such as the email address using the `@` in the middle of the expression or the hex values using the `#` at the beginning of the expression - these are attached with the `+` symbol, as we've learned from past operations such as concatenation. While seemingly complicated, these expressions streamline processes in code and save time for the developer and can be quite simple to remember, once you understand the basic structure.
<br><br>
The expression I will focus on is the hex value expression, as I have a particular soft spot for the front end design component of web design and utilize hex values quite a lot myself.

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

The standard hex value regex is as follows: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`.  
<br>
This looks intimidating at first glance, but it's very simple when you break it up.<br>
<br> The first part is `[a-f0-9]{6}` - this part is searching for a hex value with letters `a-f` (or `A-F` if using flag) and numbers between 0-9 within 6 character spaces. For example, `#E6E6FA`.
<br> The second part is `[a-f0-9]{3}` - an expression that is doing the same as the first part but looking for only 3 character spaces this time. Some colors can have 3 hex character spaces if both the values are the same for each component - such as `#BB5588` can be `#B58`.

## Anchors

There are two anchors in this regex expression: `^` and `$`. The former represents the start of the string, the latter represents the end of the string. Everything in between the two symbols is what the regex looks for.

## Quantifiers

There are two quantifiers in this regex expression: `?` and `{ }`. In this particular expression, the `?` after the `#` indicates a boolean value of 0 or 1 that tells the expression to match a string whether it begins with a `#` or not. <br>
The other quantifier, `{ }`, wrapped around an integer simply indicate how many character values to look for.

## Grouping Constructs

The grouping construct is indicated by the `( )` - these simply group exressions inside of them. In the hex value, the `( )` enclose the entirety of the expression, treating it as a single pattern - the quantifiers (in the case of hex, `?`) is applied to entire grouping.

## Bracket Expressions

The bracket expressions contain everything within the `[ ]` which will be matched with the regex. In the case of the hex value regex, the brackets enclose the characters of letters and numbers.

## Character Classes

Character classes, or character sets, match a given character defined in a set of characters. In our hex value expression, the `-` indicates the range between the two characters, such as `a-z` or `0-9`. In either example, only one character from this range can be selected. These operations can be quite useful and time-saving. For example, instead of typing `[abcdefghijklmnopq]`, `[a-q]` does the same with much less typing and more readability.

## The OR Operator

As with many other operations, the OR operator is the `|` between the two components, it is simply telling the expression to look for either of the two components defined above.

## Flags

Flags are option parameters for regex expressions - there are 6 total flags: `i`, `g`, `s`, `m`, `y`, and `u`. The `i` flag ignores casing, an ideal flag to use with the hex value expression so that it can read both `#E6E6FA` and `#e6e6fa`. The `g` flag stands for global and makes the expression search for all occurences, another good one to use with hex. The `s` is dot all, which makes the character `.` match newlines as well. The `m` is multiline which makes the anchors, `^` and `$`, as covered above, match the beginning of every single line instead of the beginning and ending of the whole string. The `y` means sticky, which "makes the expression start its searching from the index indicated in its lastIndex property". And finally, the `u` which stands for unicode, simply "makes the expression assume individual characters as code points, not code units, and this match 32-bit characters as well".
[source](https://www.codeguage.com/courses/regexp/flags)

## Character Escapes

Finally, character escapes are denoted by the `\` symbol. If a character has a special meaning in regex, the `\` needs to be used to escape the character first. There is no need to escape anything in a typical hex value expression, but a good example would be if an expression needed to look for a `.` or `+`, as these two symbols are used quite a bit in building regex expressions. In order to search for one of these symbols, it would be written `\.` which would look for "." or `\+` which would look for "+".

## Author

The author is [me](https://github.com/JThorneX).

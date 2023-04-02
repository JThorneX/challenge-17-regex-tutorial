# Regex Tutorial -- Hex Values

This tutorial touches on how to utilize regex expressions to streamline code for various functions. The purpose of this challenge is to explain a specific regex expression in order to demonstrate my own knowledge of the search pattern that regex defines. The table of contents outline the parts of the tutorial that will be covered and can be clicked for quick access.

## Summary

Before diving into the specific regex expression, it is important to understand what exactly a regex expression is. It can be defined simply as a pattern that describes some amount of text. The complex patterns - the ones we routinely work with as developers - describe a series of characters, made up of letters, numbers, dots, underscores, percentage signs, and hyphens.
<br>
Specific regex expression utilize specific characters, such as the email address using the @ in the middle of the expression or the hex values using the # at the beginning of the expression - these are attached with the + symbol, as we've learned from past operations such as concatenation. While seemingly complicated, these expressions streamline processes in code and save time for the developer and can be quite simple to remember, once you understand the basic structure.
<br>
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

The standard hex value regex is as follows: <mark style="background-color: #E6E6FA">/^#?([a-f0-9]{6}|[a-f0-9]{3})$/</mark>.  
<br>
This looks intimidating at first glance, but it's very simple when you break it up.
<br> The first part is <mark style="background-color: #E6E6FA">[a-f0-9]{6}</mark> - this part is searching for a hex value with letters a-f (or A-F) and numbers between 0-9 within 6 character spaces. For example, #E6E6FA - the hex value of the highlighted text.<br> The second part is <mark style="background-color: #E6E6FA">[a-f0-9]{3}</mark> - an expression that is doing the same as the first part but looking for only 3 character spaces this time. Some colors can have 3 hex character spaces if both the values are the same for each component - such as #BB5588 can be #B58.

### Anchors

There are two anchors in this regex expression: <mark style="background-color: #E6E6FA">^</mark> and <mark style="background-color: #E6E6FA">$</mark>. The former represents the start of the string, the latter represents the end of the string. Everything in between the two symbols is what the regex looks for.

### Quantifiers



### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

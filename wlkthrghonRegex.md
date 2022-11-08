# Walkthrough on Regex!

* *Howdy Folks! Need a crash course on how to use Regexs? Well below you can find a series of understandings behind what a regex defines and how it's syntax is used*

### Summary

**The code below I will be using will be referenced throughout this walkthrough to give an idea of real regex components we can use. This is an example for validating the layout and structure of an email to follow a correct format.**

* *Email Validation:* `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

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

The `Anchor` is what begins and finishes the Regex.

For example: 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` has anchors of `^` and `$`.

The code signifies that we are looking for an email that starts with `^([a-z0-9_\.-]+)` and ends with `.([a-z\.]{2,6})$`.

I understand all of those characters look confusing but they will be broken down later on. But basically what anchor means is that we are looking for something to match the guidlines of our code.

And that something must follow our guidelines in order to match.

### Quantifiers

In short, a `Quantifier` is used to determine how many times a specific character or character group needs to be in our line of code to match correctly.

*Example:* If we were to use this snippet `xyz+` in our regex model, then this will match any string `xy` followed by at least one string `z`.

*Our Model:* `([a-z0-9_\.-]+)` will match any string containing `a-z`, `0-9`, `_`, `.`, or `-`. The Quantifier `+` just meamns that it must contain atleast one of these characters in order to match correctly.

### OR Operator

To explain what an `OR Operator`is for this walkthrough we are going to use a different snippet of code. The code above will unfortunately not be helpful in explaining.

*OR Op Code:* `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

This Regex is used to match a hex code using an OR Operator. 
What this expression will do is look for a match where the snippet starts with the `#` character. This character must come first in the match as well as be followed by one of the parameters below.

* `[a-f0-9]{6}` which will look for a match that must be a `6` character string containing a mix of `a-f` letters and `0-9` numbers.

* `|` OR Operator

* `[a-f0-9]{3}` which will look for a match that must be a `3` character string containing a mix of `a-f` letters and `0-9` numbers.

### Character Classes


### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

There is no greedy or lazy match included for the snippet of code for matching the email.

### Boundaries

If in a string we are looking for specific words, we can use `Boundaries` such as `^` and `$` which allow you to anchor the regex pattern to the beginning and end of the line.

There are no boundaries in the code snippets above.

### Back-references

There are no `Back-references` in the snippets above.

But to summarize, back-references are regular expression commands which refer to a previous part of the matched regular expression. Back-references are specified with backslash and a single digit.

*Example:* `('\1')`

The part of the regular expression they refer to is called a subexpression, and is designated with parentheses.

### Look-ahead and Look-behind

`Look-ahead`

*Example:* `(?=foo)`

Looks for what follows the current position in the expression `foo` using the `(? ...)` syntax. 

#

`Look-behind`

*Example:* `(?<=foo)`

Looks for what comes before the current position in the expression `foo` using the `(? ...)` syntax. 

## Author

**Charles Breven Glasgow**

- **[GitHub](https://github.com/Brevenn)**
- **[LinkedIn](https://www.linkedin.com/in/charles-glasgow-7b07a41a3/)**
- **[Portfolio](https://brevenn.github.io/Portfolio-Full-Stack/)**

#

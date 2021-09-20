# Regex Tutorial

Regex, or Regular expressions are patterns used to match character combinations in strings.  When used in JavaScript, regular expressions are also objects.  Regex can be expressed in one of two ways.  Either as a literal consisting of a pattern between slashes `( let re = /ab+c/;)` or as a constructor function of the regular expression object `(let re = new RegExp('ab+c');)`.

## Summary

I will be showcasing a tutorial on the use of Regex to validate an email address using the expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`.  This can be very useful when trying to validate an email and help filter out users entering incomplete information either on purpose or by mistake.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors
Anchors used in this regex email example are towards the start and the end of the expression `(/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/)`.  At the start we have the use of `^` which Regex will read as the beginning of a string (which is also case sensitive), and at the end we have the use of `$` which will be read as the ending of the expression.

### Quantifiers
Quantifers are used to show the number of characters or expressions to match.  In this email example, the quantifiers include the `+` as well as the `{2,6}`.  In the example expression `[a-z0-9_.-]+` will check that any character that matches the characters inside the brackets appears at least one time, without an upper limit.  We can read `[\da-z.-]+` in the same way.  `[a-z\.]{2,6}` will read in regex as expecting 2 to 6 characters to match in those brackets.  Numbers shown in the `{}` brackets set the upper and lower limits of expected characters. 

### Character Classes
Character classes match types of characters.  In this expression `/d` is used, which matches a single character that is a digit from 0-9.  The use of a backslash is necessary so that Regex doesn't read it as an everyday letter d.

### Grouping and Capturing
Regex uses `()` for grouping and capturing.  Regex will treat anything inside of these `()` as an individual group/unit.  In our example `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` the three individual groups may stand out more now (`([a-z0-9_.-]+)`,`([\da-z.-]+)`, and `([a-z.]{2,6})`). 

### Bracket Expressions
Regex uses `[]` as a container for what are called bracket expressions.  There are three of these within our example `[a-z0-9_.-]`, `[\da-z.-]`, and `[a-z.]`.  What a bracket expression does is represents an individual character string.  That character string can be anything that is contained within the `[]`.  If we use `[a-z0-9_.-]` from our example, this expresses that this character set will satisfy a match by any `lowercase letters (a-z)`, `any digit (0-9)`, or a `period (.)`.  When used in sync with the quantifier `+` in our example, it means any number of characters matching those expressions within the brackets will result in a match.

### Greedy and Lazy Match
In simplest terms Greedy means your expression will match as large a group as possible, lazy means it will match the smallest group possible.  Since our example uses the `+` and `{ , }` quantifier it will match as many times as it can, these are considered greedy quantifiers.

## Mason Cain
Mason Cain is currently a student in Case Western Reserve University's Boot Camp developing skills in full stack web development.
For any questions, please contact me with the information below:

GitHub: [@Mason021](https://api.github.com/users/Mason021)


GitHub Gist: [Gist](https://gist.github.com/Mason021/f752452116e54c15da840d0e907215ba#anchors)
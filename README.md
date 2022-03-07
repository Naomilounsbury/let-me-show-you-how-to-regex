# Let Me Show You How to Regex

In this short tutorial I will explain a matching email string in regex. As I am no expert in regex, I used several sites to do this. To get the basics of regex, I used [regex101](https://regex101.com/). I used stackoverflow find out whether or not my string had an [OR operator](https://stackoverflow.com/questions/8020848/how-is-the-and-or-operator-represented-as-in-regular-expressions) as well as to find out whether or not there was a [word boundary](https://stackoverflow.com/questions/1324676/what-is-a-word-boundary-in-regex). I used [regular-expressions.info](https://www.regular-expressions.info/backref.html) to find out if my string contained any back references and to find out if there were any [lookaheads or lookbehinds](https://www.regular-expressions.info/lookaround.html).

## Summary

In this tutorial, I will be examining how to match an email with regex. This is really useful because without regex you'd need at least a couple lines of code to match an email.
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ is the code snippet I will explain.

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

In my matching email string, there are two anchors. "^" denotes the start of a string and "$" denotes the end of a string.

### Quantifiers

In my chosen matching email string there are three quantifiers. The "+" after "[a-z0-9_\.-]" and"[\da-z\.-]" says that those characters may be matched as many times as needed.

Technically regex101.com says that it "matches the previous token between one and unlimited times" but if the previous token never shows up then wouldn't that be between zero and unlimited times. But their phrasing could also mean that at least one of those characters has to show up in the string and not that all the characters have to show up.

"{2,6}" is the third quantifier in this string because "+" was used twice.

### OR Operator

There is no OR operator in this string.

### Character Classes

"[a-z0-9_\.-]""[\da-z\.-]" and "[a-z\.]" all have character classes inside them but also there are parenthesis around them so I'll bring them up again in the grouping sub-heading.
As you can see [a-z] [0-9] are listed here as characters that can be used. Also "\d" here is a meta sequence that matches digits (similar to [0-9]).

### Flags

There are no flags in this piece of regex.

### Grouping and Capturing

There are three groups in this piece of regex. The first capturing group is ([a-z0-9_\.-]+)which is capturing the user name of the email, which can have letters, numbers, an underscore or a dash.
the second capturing group is for the email site which is ([\da-z\.-]+). This one can have numbers or letters or a dash.
The third capturing group is ([a-z\.]{2,6}), which is the final part of the email which can be only letters and a period, like .cn or .net.

### Bracket Expressions

Brackets indicate a set of characters to match.
In the email, we want to check to see if the email is made of letters and numbers and underscores so we put these into brackets to check [a-z0-9] like so. If I wanted an email composed entirely of 1234 and "a" and "f", then I would put ^([af1234]+)@([0-9a-z]+)\.([a-z\.]{2,6})$

### Greedy and Lazy Match

Any thing that matches as many times as needed is greedy and anything that matches with as few as things as possible is lazy.
In the email string there are three greedy quantifiers meaning that these are trying to match with as many characters as possible. The two "+" signs and {2,6} are my greedy quantifiers.

### Boundaries

There are no boundaries in this string

### Back-references

There are no back references in this string.

### Look-ahead and Look-behind

There are no look ahead or look behinds in this string.

## Author

Please feel free to check out [my github](https://github.com/Naomilounsbury) and this [regex repository](https://github.com/Naomilounsbury/let-me-show-you-how-to-regex) in particular.
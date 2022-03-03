# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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
In my chosen matching email string there are three quantifiers. The "+" after "[a-z0-9_\.-]" and"[\da-z\.-]" says that those characters may be matched as many times as needed. Technically regex101.com says that it "matches the previous token between one and unlimited times" but if the previous token never shows up then wouldn't that be between zero and unlimited times. But their phrasing could also mean that at least one of those characters has to show up in the string and not that all the characters have to show up.
"{2,6}" is the third quantifier in this string because "+" was used twice. 


### OR Operator

### Character Classes
"[a-z0-9_\.-]""[\da-z\.-]" and "[a-z\.]" all have character classes inside them but also there are parenthesis around them so I'll bring them up again in the grouping sub-heading.
As you can see [a-z] [0-9] are listed here as characters that can be used. Also "\d" here is a meta sequence that matches digits (similar to [0-9])

### Flags
There are no flags in this piece of regex. 

### Grouping and Capturing
([a-z0-9_\.-]+)
([\da-z\.-]+)
([a-z\.]{2,6})

### Bracket Expressions
Brackets just indicate a set of characters to match. 
In the email, we want to check to see if the email is made of letters and numbers and underscores so we put these into brackets to check [a-z0-9] like so. If I wanted an email composed entirely of 1234 and "a" and "f", then I would put ^([af1234]+)@([0-9a-z]+)\.([a-z\.]{2,6})$

### Greedy and Lazy Match
Any thing that matches as many times as needed is greedy and anything that matches with as few as things as possible is lazy. I find it funny that they are both sins: greed and sloth. But anyway in the email string I have three greedy quantifiers meaning that these are trying to match with as many characters as possible.

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
